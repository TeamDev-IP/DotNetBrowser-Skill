# Migrating from CefSharp to DotNetBrowser

## Migration from CefSharp to DotNetBrowser

This guide is for .NET developers who have existing CefSharp code and are
considering migrating to DotNetBrowser.

Each section of this guide focuses on a specific CefSharp feature and explains
how to replace it with DotNetBrowser.

This guide provides drop-in replacements for CefSharp calls and events,
highlights key differences between DotNetBrowser and CefSharp, and includes
helpful links to related documentation.

## Installing dependencies

The easiest way to add DotNetBrowser to your project is through NuGet. Just
install the package for your UI framework, and NuGet will take care of the rest.
It will also download the core library and the Chromium files you need.

Ensure that you select the correct configuration from the beginning—match
the architecture (x86, x64, or aarch64) and the UI framework (such as WPF 
or Avalonia).

Required packages:

* `DotNetBrowser.Wpf.x64` — WPF integration for Windows x64.
* (Pulled transitively) `DotNetBrowser.Win-x64` — core API.
* (Pulled transitively) `DotNetBrowser.Chromium.Win-x64` — bundled Chromium.

You can find the full list of NuGet packages for all supported UI frameworks and
platforms in the [installation guide][guide-nuget].

If you're not using NuGet, you can manually add DotNetBrowser to your project by
referencing [DLL files][guide-zip] or [VSIX packages][guide-vsix].

## Chromium engine

### Initializing

In CefSharp, you start by initializing the underlying Chromium Embedded
Framework (or simply CEF):

```csharp
Cef.Initialize(new CefSettings());
```

In WPF and WinForms, CefSharp automatically calls this method. However, if you
need custom settings, you call it manually first.

Note that this method **must** be called from the main thread and only once per
process lifetime. Both limitations stem from
CefSharp's [in-process architecture][blog-architecture], which runs the Chromium
engine in your .NET process and limits you to a single engine per process.

In DotNetBrowser, you also start by initializing the Chromium engine, but no
limitations apply:

```csharp
IEngine engine = EngineFactory.Create(RenderingMode.HardwareAccelerated);
```

DotNetBrowser has the [out-of-process architecture][guide-architecture] and
launches the Chromium engine in a separate process. That means you can create
more than one engine per process, at any time, from any thread in your
application.

We explore why you may need multiple engines in
the [Browser isolation][section-isolation] section of this guide.

### Shutting down

In CefSharp, you **must** shut down the Chromium engine when you don't need it
anymore, otherwise the application will hang.

Similarly, you **must** call this method in the main thread of the application.
If you're using WPF or WinForms, CefSharp will call this method for you.

In DotNetBrowser, you must always shut down the Chromium engine explicitly. You
may do it at any time, and from any thread. Failing to dispose of 
the `IEngine` leads to resource leaks but does not affect the .NET process:


**CefSharp**
```csharp
Cef.Shutdown();
```


**DotNetBrowser**
```csharp
engine.Dispose();
```



## Embedding the browser

### WPF

Both CefSharp and DotNetBrowser provide WPF components that you can add directly
to your XAML.

In fact, CefSharp provides two different components. If you need the off-screen
rendering, you're using the `WPF` implementation. If you need faster rendering,
you're using the `Wpf.HwndHost` implementation that re-parents the Chromium
window into your application.

DotNetBrowser provides a single component that can render the content in two
modes — roughly equivalent to those of CefSharp. They are
called `HardwareAccelerated` and `OffScreen` and you always choose the mode when
creating the `IEngine`.

**MainWindow.xaml:**


**CefSharp**
```xml
<Window xmlns:wpf="clr-namespace:CefSharp.Wpf;assembly=CefSharp.Wpf"
        x:Class="CefSharp.Wpf.MainWindow"
        Title="CefSharp" Width="800" Height="600">
    <Grid>
        <wpf:ChromiumWebBrowser x:Name="Browser" 
                                Address="https://www.teamdev.com" />
    </Grid>
</Window>
```


**DotNetBrowser**
```xml
<Window xmlns:wpf="clr-namespace:DotNetBrowser.Wpf;assembly=DotNetBrowser.Wpf"
        x:Class="DotNetBrowser.Wpf.MainWindow"
        Title="DotNetBrowser" Width="800" Height="600" Closed="Window_Closed">
    <Grid>
        <wpf:BrowserView Name="browserView" />
    </Grid>
</Window>
```



**MainWindow.xaml.cs:**


**CefSharp**
```csharp
public partial class MainWindow : Window
{
    static MainWindow()
    {
        CefSettings settings = new CefSettings();
        Cef.Initialize(settings);
    }  

    public MainWindow()
    {
        InitializeComponent();
    }
}
```


**DotNetBrowser**
```csharp
public partial class MainWindow : Window
{
    private readonly IEngine engine;

    public MainWindow()
    {
        // You configure the rendering mode here.
        engine = EngineFactory.Create(RenderingMode.HardwareAccelerated);
        IBrowser browser = engine.CreateBrowser();

        InitializeComponent();
        browserView.InitializeFrom(browser);
        browser.Navigation.LoadUrl("https://teamdev.com");
    }

    private void Window_Closed(object sender, EventArgs e)
    {
        engine?.Dispose();
    }
}
```



Read more about the rendering modes, their performance, and choosing between
them in the [`BrowserView` guide][guide-rendering-modes].

### WinForms

In WinForms, CefSharp always uses a heavyweight rendering, the same as
in `Wpf.Hwnd`.

In DotNetBrowser, the WinForms `BrowserView` control will use the rendering mode
you configured when creating the `IEngine`.

The rest is similar:


**CefSharp**
```csharp
using CefSharp.WinForms;
...

public partial class BrowserForm : Form
{
    private readonly ChromiumWebBrowser browser;

    public BrowserForm()
    {
        InitializeComponent();
        browser = new ChromiumWebBrowser("https://teamdev.com");
        Controls.Add(browser);
    }
}
```


**DotNetBrowser**
```csharp
using DotNetBrowser.WinForms;
...

public partial class BrowserForm : Form
{
    private readonly IEngine engine;

    public BrowserForm()
    {
        // You configure the rendering mode here.
        engine = EngineFactory.Create(RenderingMode.HardwareAccelerated);
        IBrowser browser = engine.CreateBrowser();

        InitializeComponent();
        
        BrowserView browserView = new BrowserView();    
        Controls.Add(browserView);
        FormClosed += Form1_FormClosed;

        browserView.InitializeFrom(browser);
        browser.Navigation.LoadUrl("https://teamdev.com");
    }

    private void Form1_FormClosed(object sender, FormClosedEventArgs e)
    {
        engine?.Dispose();
    }
}
```



### Headless mode

CefSharp provides a special `OffScreen` implementation of `ChromiumWebBrowser`
for headless use cases, where the browser is not shown in the UI.

In DotNetBrowser, **every** instance of `IBrowser` is a fully-functional browser
that works without a UI.


**CefSharp**
```csharp
using CefSharp.OffScreen;
...

public static class Program
{
    public static int Main(string[] args)
    {
        var settings = new CefSettings();
        Cef.Initialize(settings);
          
        var browser = new ChromiumWebBrowser("https://www.google.com/");
        ...
        // Just wait to keep the process running.
        Console.ReadKey();
        Cef.Shutdown();
        return 0;
    }
}
```


**DotNetBrowser**
```csharp
using DotNetBrowser.Browser;
using DotNetBrowser.Engine;
...

public static class Program
{
    public static int Main(string[] args)
    {
        using (IEngine engine = 
            EngineFactory.Create(RenderingMode.HardwareAccelerated))
        {
            IBrowser browser = engine.CreateBrowser();
            browser.Navigation
                   .LoadUrl("https://www.google.com/").Wait();
            ...
            // Just wait to keep the process running.
            Console.ReadKey();
            return 0;
        }
    }
} 
```



## Disposing the browser

In both CefSharp and DotNetBrowser, you must close the Chromium engine and
browser instances to prevent resource leaks. Closing the engine will
automatically close all browser instances created by it:


**CefSharp**
```csharp
// You must dispose the browser only in the main thread.
cefBrowser.Dispose();
```


**DotNetBrowser**
```csharp
// You may dispose the browser in any thread.
browser.Dispose();
```



CefSharp doesn't provide a universal way to detect when the browser is closed.

In DotNetBrowser, you can register the `Disposed` event handler, for both
browser and the engine. This event is emitted when the engine or browser are
closed, regardless of how and why they got closed.


**DotNetBrowser**
```csharp
engine.Disposed += (sender, args) =>
{
    Console.WriteLine("The engine was closed!");
};

browser.Disposed += (sender, args) =>
{
    Console.WriteLine("The browser was closed!");
};
```



## Threading

In CefSharp, it's important to always be aware of which thread you're calling 
a method from. Many methods have specific thread requirements, and 
the documentation often includes statements like the following:

> This method must be called on the CEF XYZ thread.

DotNetBrowser doesn't impose any threading limitations. You're allowed to use
the API of the library from any thread.

## Browser isolation {#browser-isolation}

### Data and network isolation

In CefSharp, you can isolate the browsers from each other by putting them in
different `RequestContext`'s. The browsers within the same request context share
everything: preferences, cookies, cache, service workers. Respectively, the
browsers in the different request contexts are isolated.

In DotNetBrowser, the alternative for a request context is
a [guide-profile][guide-profile]. The browsers created within the same 
profile share preferences, networking layer, cache, cookies, storage, 
and other things. To isolate the browsers from each other, create them 
in different profiles:


**CefSharp**
```csharp
var publicContext = RequestContext.Configure()
                    .WithCachePath("<path to a public cache location>")
                    .Create();
var publicBrowser = new ChromiumWebBrowser("https://teamdev.com");
publicBrowser.RequestContext = publicContext;


var secureContext = RequestContext.Configure()
                    .WithCachePath("<path to a secure cache location>")
                    .Create();
var secureBrowser = new ChromiumWebBrowser("https://internal.system");
secureBrowser.RequestContext = secureContext;
```


**DotNetBrowser**
```csharp
var publicProfile = engine.Profiles.Default;
var publicBrowser = publicProfile.CreateBrowser();
publicBrowser.Navigation.LoadUrl("https://teamdev.com");
            
var secureProfile = engine.Profiles.Create("secure-profile");
var secureBrowser = secureProfile.CreateBrowser();
secureBrowser.Navigation.LoadUrl("https://internal.system");
```



### Runtime isolation

CefSharp runs a Chromium engine **inside** the .NET process. The Chromium engine
is a singleton, and can be created only once per process lifetime. If 
the engine crashes, not just the browser instances, but 
**the whole application** goes down.

DotNetBrowser runs Chromium engines **in separate processes**, which keeps
the .NET process unaffected when the engine crashes. When such a crash 
occurs, the .NET process will receive a notification:


**DotNetBrowser**
```csharp
engine.Disposed += (s, e) =>
{
    if (e.ExitCode != 0)
    {
        // Engine has crashed.
    }
};
```



When the engine crashes, its `IBrowser` instances are also immediately closed.
By creating profiles and browsers within different `IEngine`'s, you can isolate
them from crashes in each other's engines.

> Please note that creating and operating extra `IEngine` instances is resource-intensive and is rarely required.


**DotNetBrowser**
```csharp
// Start the Chromium main process for the public browser.
var publicEngine = EngineFactory.Create(RenderingMode.HardwareAccelerated);
var publicProfile = publicEngine.Profiles.Default;
var publicBrowser = publicProfile.CreateBrowser();
publicBrowser.Navigation.LoadUrl("https://teamdev.com");

// Start the Chromium main process for the secure browser.
var secureEngine = EngineFactory.Create(RenderingMode.HardwareAccelerated);
var secureProfile = secureEngine.Profiles.Create("secure-profile");
var secureBrowser = secureProfile.CreateBrowser();
secureBrowser.Navigation.LoadUrl("https://internal.system");
```



## Navigation methods

Most of the navigation methods in CefSharp have a one-to-one counterpart in
DotNetBrowser:


**CefSharp**
```csharp
ChromiumWebBrowser chromiumBrowser = new ChromiumWebBrowser();
chromiumBrowser.LoadUrl("https://teamdev.com");

IBrowser browser = chromiumBrowser.GetBrowser();
browser.GoBack();
browser.GoForward();
browser.Reload(true);
browser.StopLoad();
bool canGoBack = browser.CanGoBack;
bool canGoForward = browser.CanGoForward;
```


**DotNetBrowser**
```csharp
INavigation navigation = browser.Navigation;
navigation.LoadUrl("https://teamdev.com");
navigation.GoBack();
navigation.GoForward();
navigation.Reload();
navigation.ReloadIgnoringCache();
navigation.Stop();
bool canGoBack = navigation.CanGoBack();
bool canGoForward = navigation.CanGoForward();
```



### Navigation events

Both CefSharp and DotNetBrowser provide you with means to track 
the navigation status. Replace `LoadingStateChanged` and `LoadError` 
events with the combination of DotNetBrowser's `NavigationStarted`, 
`NavigationStopped`, and `NavigationFinished`:


**CefSharp**
```csharp
browser.LoadingStateChanged += (sender, args) =>
{
    if (args.IsLoading)
    {
        Console.WriteLine("Navigation started.");
    }
    else
    {
        Console.WriteLine("Navigation completed.");
    }
};

browser.LoadError += (sender, args) => 
{
    if (args.ErrorCode == CefErrorCode.Aborted)
    {
        Console.WriteLine("Navigation aborted");
    }
}
```


**DotNetBrowser**
```csharp
navigation.NavigationStarted += (s, e) => 
{
    Console.WriteLine("Navigation started.");
};
navigation.NavigationStopped += (s, e) => 
{
    Console.WriteLine("Navigation stopped.");
};
navigation.NavigationFinished += (sender, args) =>
{
    if (args.ErrorCode == NetError.Aborted)
    {
        Console.WriteLine("Navigation aborted");
    }
};
```



Replace `FrameLoadEnd` with `FrameDocumentLoadFinished` to determine when the
JavaScript context and DOM tree is ready in a frame:


**CefSharp**
```csharp
browser.FrameLoadEnd += (sender, args) =>
{
    if (args.Frame.IsMain)
    {
        Console.WriteLine("DOM and V8 context are ready in the main frame.");
    }
    else
    {
        Console.WriteLine("DOM and V8 context are in an iframe.");
    }
};

```


**DotNetBrowser**
```csharp
navigation.FrameDocumentLoadFinished += (s, args) => 
{
    if (args.Frame.IsMain) 
    {
        Console.WriteLine("DOM and V8 context are ready in the main frame.");
    }
    else
    {
        Console.WriteLine("DOM and V8 context are in an iframe.");
    }
};
```



There are 10 granular navigation events in DotNetBrowser. Check
the [complete list][guide-nav-events].

### Loading with POST data

In CefSharp, you can't directly load a URL with POST parameters. To achieve
that, you need to register a global request handler, cherry-pick the request you
want to modify, and manually add the POST data.

In DotNetBrowser, you can directly load a URL with any POST data:


**CefSharp**
```csharp
class MyRequestHandler : RequestHandler
{
    protected override IResourceRequestHandler GetResourceRequestHandler(...)
    {
        if (request.Url == "https://my.post.endpoint")
        {
            return new MyResourceRequestHandler();
        }
        return null;
     }
}

class MyResourceRequestHandler : ResourceRequestHandler
{
    protected override CefReturnValue OnBeforeResourceLoad(...)
    {
        var postData = new PostData();
        postData.AddData("username=test&password=1234");
        request.Method = "POST";
        request.PostData = postData;
        request.SetHeaderByName(
            "Content-Type", "application/x-www-form-urlencoded", true);
        return CefReturnValue.Continue;
    }
}

browser = new ChromiumWebBrowser("https://my.post.endpoint");
browser.RequestHandler = new CustomRequestHandler();
```


**DotNetBrowser**
```csharp
// Create an array with post data parameters
KeyValuePair<string, string>[] formData = 
{
    new KeyValuePair<string, string>("username", "test"),
    new KeyValuePair<string, string>("password", "1234")
};

LoadUrlParameters request = new LoadUrlParameters("https://my.post.endpoint")
{
    // DotNetBrowser will automatically derive the content type 
    // from the data type.
    UploadData = new FormData(formData)
};

// Navigate with the custom request.
browser.Navigation.LoadUrl(request);
```



DotNetBrowser automatically fills in the `Content-Type` and `Content-Length`
headers for POST requests. For multipart uploads, it also adds the form boundary
and sets each part's `Content-Disposition` and `Content-Type` headers.

You can read more about making POST requests in the guide on
the [navigation with POST data][guide-loading-post].

### Loading HTML content

The easiest way to load an HTML string in both CefSharp and DotNetBrowser is to
load it as a `data:` URL:


**CefSharp**
```csharp
var html = "<html>Html Encoded in URL!</html>";
var encodedHtml = Convert.ToBase64String(Encoding.UTF8.GetBytes(html));
browser.Load("data:text/html;base64," + encodedHtml);
```


**DotNetBrowser**
```csharp
var html = "<html>Html Encoded in URL!</html>";
var encodedHtml = Convert.ToBase64String(Encoding.UTF8.GetBytes(html));
browser.Navigation.LoadUrl("data:text/html;base64," + encodedHtml);
```



This method is limited by the maximum URL size of roughly ~2 MB. If you're using
CefSharp's `ResourceHandler` to load more content, replace it with
a [custom scheme request interceptor][section-intercepting].

## JavaScript

### When to start executing JavaScript

To run JavaScript at the earliest possible moment, you need to know when
Chromium has finished initializing the V8 JavaScript context.

CefSharp provides the `OnContextCreated` event that is called when 
the JavaScript context has just been created in the frame. At this moment, 
no other scripts in the frame ran yet. Replace it with DotNetBrowser's 
`InjectJsHandler` that has the same semantics:


**CefSharp**
```csharp
class RenderProcessMessageHandler : IRenderProcessMessageHandler
{
    void OnContextCreated(IWebBrowser browserControl, 
                          IBrowser browser, IFrame frame)
    {
        frame.ExecuteJavaScriptAsync("...");
    }
}
browser.RenderProcessMessageHandler = new RenderProcessMessageHandler();

```

**DotNetBrowser**
```csharp
browser.InjectJsHandler = new Handler<InjectJsParameters>(args =>
{
    args.Frame.ExecuteJavaScript<IJsObject>("...");
});
```



### Calling JavaScript from .NET

Both libraries provide similar capabilities when it comes to JavaScript, with
the difference in type conversion and injecting .NET objects 
into JavaScript.

To execute a script, replace `EvaluateScriptAsync` call
with `ExecuteJavaScript`:


**CefSharp**
```csharp
JavascriptResponse response = await frame.EvaluateScriptAsync("'Hello'");
```


**DotNetBrowser**
```csharp
string response = await frame.ExecuteJavaScript<string>("'Hello'");
```



While the calls look alike, the results you will be getting are different. Both
CefSharp and DotNetBrowser will attempt to convert JavaScript types to their C#
counterparts, but they do it differently.

CefSharp can return primitive types, simple non-cyclic JavaScript objects, and
arrays of these types. It **can't return** the DOM elements or the `window`
objects.

DotNetBrowser returns primitive types and JavaScript **objects of any complexity
**, including objects with cyclic references — the library uses 
the V8 objects directly, without serializing and copying them under 
the hood.


**CefSharp**
```csharp
JavascriptResponse numberResponse = await frame.EvaluateScriptAsync("123");
int number = (int) numberResponse.Result;

JavascriptResponse booleanResponse = await frame.EvaluateScriptAsync("true");
bool boolean = (bool) booleanResponse.Result;

JavascriptResponse strResponse = await frame.EvaluateScriptAsync("'Hello'");
string str = (string) strResponse.Result;

JavascriptResponse objResponse = 
    await frame.EvaluateScriptAsync("({'foo': 'bar'})");
dynamic obj = objResponse.Result;
var foo = obj.foo;

// You can't do this:
JavascriptResponse windowResponse = await frame.EvaluateScriptAsync("window");
object window = strResponse.Result; // Null.
```


**DotNetBrowser**
```csharp
// DotNetBrowser directly converts primitive types, just like CefSharp:
double number = await frame.ExecuteJavaScript<double>("123");
bool boolean = await frame.ExecuteJavaScript<bool>("true");
string str = await frame.ExecuteJavaScript<string>("'Hello'");

IJsObject obj = 
    await frame.ExecuteJavaScript<IJsObject>("{'foo': 'bar'}");
var foo = obj.Properties["foo"];

// This works in DotNetBrowser.
IJsObject window = await frame.ExecuteJavaScript<IJsObject>("window");

// When possible, DotNetBrowser will select a more specific type:
IElement body = await frame.ExecuteJavaScript<IElement>("document.body");

```



Read more in the guide about [calling JavaScript from .NET][guide-executing-js].

### Calling .NET from JavaScript

In both solutions, calling the .NET code from JavaScript involves injecting 
a .NET object into the JavaScript world.

In CefSharp, that is a two-step process where you need to put the .NET object
into the `JavascriptObjectRepository` on the .NET side, and then
asynchronously "fetch" it on the JavaScript side.

In DotNetBrowser, the approach is simpler: you assign an arbitrary .NET object
to an arbitrary JavaScript property.

**In C# code:**


**CefSharp**
```csharp
// Register a .NET object in the registry:
browser.JavascriptObjectRepository.ResolveObject += (sender, e) =>
{
    var repo = e.ObjectRepository;
    if (e.ObjectName == "myObject")
    {
        repo.Register("myObject", new MyObject(), null);
    }
};
```


**DotNetBrowser**
```csharp
// Assign the .NET object to a property of any JavaScript object. 
IJsObject window = frame.ExecuteJavaScript<IJsObject>("window").Result;
window.Properties["myObject"] = new MyObject();
```



**In JavaScript code:**


**CefSharp**
```js
// Fetch the .NET object once:
await CefSharp.BindObjectAsync("myObject");

// Use the injected .NET object.
myObject.add(40, 2).then((sum) => console.log("Sum is: " + sum));
```


**DotNetBrowser**
```js
// You can use the JavaScript object right away:
const sum = myObject.add(40, 2);
console.log("Sum is: " + sum);
```



Read more about
calling [.NET from JavaScript in DotNetBrowser][guide-dotnet-from-js].

## Intercepting traffic {#intercepting-traffic}

Both CefSharp and DotNetBrowser allow you to intercept traffic and substitute
server responses in both standard and `custom://` schemes:


**CefSharp**
```csharp
public class MySchemeHandlerFactory : ISchemeHandlerFactory
{
    IResourceHandler Create(IBrowser browser, IFrame frame, 
                            string schemeName, IRequest request)
    {
        var uri = new Uri(request.Url);
        var fileName = uri.AbsolutePath;

        var responseContent = ReadMyCustomResponse(uri);
        return ResourceHandler.FromString(responseContent, ...);
        return null;
    }
}

settings.RegisterScheme(new CefCustomScheme
{
    // Corresponds to custom-sceme://
    SchemeName = "custom-scheme",
    // You must register a handler for the pair of scheme & host.
    DomainName = "my-app.com",
    SchemeHandlerFactory = new MySchemeHandlerFactory()
});

Cef.Initialize(settings);
```


**DotNetBrowser**
```csharp
var handler =
    new Handler<InterceptRequestParameters, InterceptRequestResponse>(p =>
    {
        var url = p.UrlRequest.Url;
        if (GetDomain(url) == "my-app.com") 
        {
            var opts = new UrlRequestJobOptions
            {
                HttpStatusCode = HttpStatusCode.OK,
                Headers = new List<HttpHeader>
                {
                    new HttpHeader("Content-Type", "text/html", "charset=utf-8")
                }
            };

            var job = p.Network.CreateUrlRequestJob(p.UrlRequest, opts);
            Task.Run(() =>
            {
                var responseContent = ReadMyCustomResponse(url);
                job.Write(Encoding.UTF8.GetBytes(responseContent));
                job.Complete();
            });
            // Return a job that will populate the response data.
            return InterceptRequestResponse.Intercept(job);
        } 
        else 
        {
            // Let the request through.
            return InterceptRequestResponse.Proceed();
        }
    });

var engineOptions = new EngineOptions.Builder
{
    // Register a request interceptor for the entire scheme. 
    Schemes = 
    { 
        { Scheme.Create("custom-scheme"), handler }
    }
}.Build();

var engine = EngineFactory.Create(engineOptions);
```



DotNetBrowser doesn't provide alternatives to CefSharp's convenience methods
like `ResourceHandler.FromStream` or `ResourceHandler.FromFilePath`.

## Request handler

CefSharp provides the `IRequestHandler` that allows you to modify outgoing
requests, handle authentication, and certain events from the render process. In
DotNetBrowser, the same functionality is spread across multiple individual event
handlers.

DotNetBrowser equivalents to `IRequestHandler` methods:

| Method in `IRequestHandler`      | Equivalent in DotNetBrowser                                                                            |
|:---------------------------------|:-------------------------------------------------------------------------------------------------------|
| `OnSelectClientCertificate`      | [`SelectCertificateHandler`][guide-client-cert]                                                        |
| `GetAuthCredentials`             | [`AuthenticateHandler`][guide-proxy-auth]                                                              |
| `OnCertificateError`             | [`VerifyCertificateHandler`][guide-cert-verification]                                                  |
| `OnRenderProcessTerminated`      | [`RenderProcessTerminated`][event-render-process]                                                      |
| `OnDocumentAvailableInMainFrame` | [`FrameDocumentLoadFinished`][event-frame-load-finished]                                               |
| `OnOpenUrlFromTab`               | no alternative available. To allow or cancel pop-up windows, use [`CreatePopupHandler`][guide-popups]. |

DotNetBrowser equivalents to `IResourceRequestHandler`:

| Method in `IResourceRequestHandler`                                               | Equivalent in DotNetBrowser                                |
|:----------------------------------------------------------------------------------|:-----------------------------------------------------------|
| GetResourceHandler                                                                | Use the [custom scheme interceptor][section-intercepting]. |
| OnResourceRedirect                                                                | [`RedirectResponseCodeReceived`][event-redirect-response]  |
| OnBeforeResourceLoad                                                              | [`SendUrlRequestHandler`][event-before-url-request]        |
| OnResourceLoadComplete                                                            | [`RequestCompleted`][event-request-completed]              |
| OnResourceResponse                                                                | [`StartTransactionHandler`][event-before-start]            |
| GetCookieAccessFilter                                                             | [`StartTransactionHandler`][event-before-start]            |
| `GetResourceResponseFilter` <br /><small>for reading the response content</small> | [`ResponseBytesReceived`][event-response-bytes]            |
| `GetResourceResponseFilter` <br /><small>to inject custom CSS</small>             | [`InjectCssHandler`][guide-inject-js]                      |
| `GetResourceResponseFilter` <br /><small>for filtering incoming bytes</small>     | no alternative available                                   |
| `OnProtocolExecution`                                                             | no alternative available                                   |

## Cookie manager

CefSharp provides an `ICookieManager` interface to create, read, update, and
delete cookies in the storage. There is one global cookie manager shared across
all browsers, and each `RequestContext` has its own cookie manager.

DotNetBrowser provides a similar entity called `ICookieStore`. All cookie stores
are bound to their respective `IProfile`, with no global store available:


**CefSharp**
```csharp
// The cookie manager is created in an async fasion. 
// Use IBrowserProcessHandler.OnContextInitialized to know 
// when it's ready to use.
var cookieManager = Cef.GetGlobalCookieManager();

// Create a cookie.
var success = cookieManager.SetCookie("google.com", new Cookie
{
    Name = "name",
    Value = "value",
    Expires = expirationTime,
    Path = "/"  
});

// Delete a cookie.
cookieManager.DeleteCookies("https://google.com", "cookie-name");

// Persist cookie changes immediately.
cookieManager.FlushStore();

// Iterate over all existing cookies.
cookieManager.VisitAllCookies(new CookieVisitor());

// Iterate over all cookies for a give URL.
bool withHttpOnly = false;
cookieManager.VisitUrlCookies(
    "httos://google.com", withHttpOnly, new CookieVisitor());

```


**DotNetBrowser**
```csharp
// No initialization required, you can use the cookie store right away.
var cookieStore = profile.CookieStore;

// Create a cookie.
Cookie cookie = new Cookie.Builder("google.com")
{
    Name = "name",
    Value = "value",
    ExpirationTime = expirationTime,
    Path = "/"
}.Build();
await engine.Profiles.Default.CookieStore.SetCookie(cookie);

// Delete a cookie.
await cookieStore.Delete(cookie);

// Persist cookie changes immediately.
cookieStore.Flush();

// Read all cookies.
IEnumerable<Cookie> allCookies = 
    await cookieStore.GetAllCookies();

// Read all cookies for a give URL.
IEnumerable<Cookie> urlCookies = 
    await cookieStore.GetAllCookies("https://google.com");
```



## Proxy

CefSharp allows you to configure proxy in two ways:

* by using special Chromium switches when initializing the engine;
* by changing the proxy in `IRequestContext` at runtime.

In DotNetBrowser, the preferred way is to configure the proxy at runtime
using `IProfile` instances, which you can do before creating any `IBrowser`
instances.


**CefSharp**
```csharp
// Specify global proxy settings for all browsers.
var settings = new CefSettings();

// Inherit system proxy settings.
settings.CefCommandLineArgs.Add("no-proxy-server"); 

// Use Web Proxy Auto-Disovery.
settings.CefCommandLineArgs.Add("proxy-auto-detect"); 

// Manually configure the proxy.
settings.CefCommandLineArgs.Add(
    "proxy-server=http=proxy.com:8080;https=proxy.com:8081"); 

// Use the PAC file.
settings.CefCommandLineArgs.Add("proxy-pac-url=URL"); 
Cef.Initialize(settings);


// Alternatively, configure the proxy for a specific RequestContext:
var requestContext = RequestContext
    .Configure()
    .WithProxyServer("proxy.com", 8080)
    .Create();
```


**DotNetBrowser**
```csharp
IProxy proxy = profile.Proxy;

// Inherit system proxy settings.
proxy.Settings = new SystemProxySettings();

// Don't use any proxy servers.
proxy.Settings = new DirectProxySettings();

// Use Web Proxy Auto-Disovery.
proxy.Settings = new AutoDetectProxySettings();

// Manually configure the proxy.
string proxyRules = "http=proxy.com:8080;https=proxy.com:8081";
proxy.Settings = new CustomProxySettings(proxyRules);

// Use the PAC file.
proxy.Settings = new PacProxySettings("<pac-file-url>");
```



To authenticate the proxy, replace the
CefSharp's `IRequestHandler.GetAuthCredentials` with the `AuthenticateHandler`:


**CefSharp**
```csharp
class CustomRequestHandler : CefSharp.Handler.RequestHandler
{
    override bool GetAuthCredentials(...)
    {
        if (isProxy)
        {
            using (callback)
            {
                callback.Continue(username: "user", password: "pass");
            }
            return true;
        }
        // Cancel the authentication request.
        return false;
    }
}

browser.RequestHandler = new CustomRequestHandler();
```


**DotNetBrowser**
```csharp
network.AuthenticateHandler = 
    new Handler<AuthenticateParameters, AuthenticateResponse>(p =>
        {
            if (p.IsProxy)
            {
                return AuthenticateResponse.Continue("user", "pass");
            }
            return AuthenticateResponse.Cancel();
        });
```



## Popups

In CefSharp, the pop-up browsers are controlled using the `ILifeSpanHandler`. By
using either WPF or WinForms implementation of this interface, you can show the
newly created browser in a new window. For example, here's how it looks in
WinForms:


**CefSharp**
```csharp
browser.LifeSpanHandler = CefSharp.WinForms.Handler.LifeSpanHandler
    .Create()
    .OnBeforePopupCreated((...) => {
        if (...) 
        {
            return PopupCreation.Continue;
        } 
        else
        {
            return PopupCreation.Cancel;
        }
    })
    .OnPopupCreated((ctrl, targetUrl) =>
    {
        parent.Controls.Add(ctrl);
    })
    .OnPopupDestroyed((ctrl, popupBrowser) =>
    {
        if (!ctrl.IsDisposed && ctrl.IsHandleCreated)
        {
            parent.Controls.Remove(ctrl);
        }
    }).Build(); 
```



In DotNetBrowser, you will need to replace it with two handlers:

* `CreatePopupHandler` to enable/disable the creation of a pop-up.
* `OpenPopupHandler` to show the pop-up, if needed.

In the `OpenPopupHandler`, you receive the newly created instance of `IBrowser`
and you will be able to use it in a headless mode, or display in the UI
using `BrowserView`. By default, if the browser is in `BrowserView`, it opens
the pop-up in a new window; otherwise, it suppresses the pop-up:


**DotNetBrowser**
```csharp
class MyOpenPopupHandler : IHandler<OpenPopupParameters>
{
    private readonly Control parent;

    public MyOpenPopupHandler(Control parent)
    {
        this.parent = parent;
    }

    public void Handle(OpenPopupParameters parameters)
    {
        Action showPopupAction = () =>
        {
            ShowPopup(parameters.PopupBrowser,
                      parameters.Rectangle);
        };
        parent.BeginInvoke(showPopupAction);
    }

    private void ShowPopup(IBrowser popupBrowser, Rectangle rectangle)
    {
        BrowserView browserView = new BrowserView
        {
            Dock = DockStyle.Fill
        };

        browserView.InitializeFrom(popupBrowser);
        // Add the browser view to the parent and show it.
    }
}

browser.CreatePopupHandler =
    new Handler<CreatePopupParameters, CreatePopupResponse>(p =>
    {
        if (...)
        {
            return CreatePopupResponse.Create();
        }
        else 
        {
            return CreatePopupResponse.Suppress();
        }
    });

// Set this handler if you don't want the DotNetBrowser's default behavior: 
// to show the pop-up in a new window.
browser.OpenPopupHandler = new MyOpenPopupHandler(parent);
```



## JavaScript Dialogs

CefSharp provides the `IJsDialogHandler` that allows you to handle 
the JavaScript dialogs. In DotNetBrowser, you can replace it
with [individual handlers][guide-js-dialogs]:


**CefSharp**
```csharp
class MyDialogHandler : IJsDialogHandler
{
    // Handle alert, prompt, and confirm dialogs in this method.
    bool OnJSDialog(IWebBrowser chromiumWebBrowser, ...)
    {
        ...
    }

    // Handle onBeforeUnload dialog in this method.
    bool OnBeforeUnloadDialog(IWebBrowser chromiumWebBrowser, ...)
    {
        ...
    }

    // The following methods have no alternative in DotNetBrowser, because 
    // you completely control the state of the dialog in the .NET code.
    void OnResetDialogState(IWebBrowser chromiumWebBrowser, IBrowser browser) 
    {
        ...
    } 
    void OnDialogClosed(IWebBrowser chromiumWebBrowser, IBrowser browser) 
    {
        ...
    }
}

browser.JsDialogHandler = new MyDialogHandler();
```


**DotNetBrowser**
```csharp
var dialogs = browser.JsDialogs;
dialogs.AlertHandler = new Handler<AlertParameters>(p => {  });
dialogs.ConfirmHandler =
    new Handler<ConfirmParameters, ConfirmResponse>(p =>
    {
        ...
        return ConfirmResponse.Ok();
    });
dialogs.PromptHandler =
    new Handler<PromptParameters, PromptResponse>(p =>
    {
        ...
        return PromptResponse.SubmitText("some response");
    });
dialogs.BeforeUnloadHandler =
    new Handler<BeforeUnloadParameters, BeforeUnloadResponse>(p =>
    {
        ...
        return BeforeUnloadResponse.Leave();
    });
```



If you don't set up a handler, DotNetBrowser manages the dialogs automatically.
Inside a `BrowserView`, it shows the default dialog implementation using 
the application's UI library. Otherwise, it skips the dialogs as if 
the user pressed "Cancel".

## Downloads

CefSharp provides the `IDownloadHandler` for controlling the downloading
process. In DotNetBrowser, the direct replacement
is [`StartDownloadHandler`][guide-downloads]:


**CefSharp**
```csharp
class MyDownloadHandler : IDownloadHandler
{
    bool OnBeforeDownload(IWebBrowser chromiumWebBrowser, IBrowser browser, 
                          DownloadItem downloadItem, 
                          IBeforeDownloadCallback callback)
    {
        if (downloadItem.IsValid)
        {
            string downloadPath = 
                Path.GetFullPath(downloadItem.SuggestedFileName);
            if (!callback.IsDisposed)
            {
                using (callback)
                {
                    callback.Continue(
                        downloadPath: downloadPath,
                        // Show the default save dialog.
                        showDialog: true  
                    );
                }
            }
            return true;
        }
        // Let CefSharp handle the download. 
        // In Alloy, the download is cancelled by default.
        return false;
    }

    void OnDownloadUpdated(IWebBrowser chromiumWebBrowser, IBrowser browser, 
                           DownloadItem downloadItem, 
                           IDownloadItemCallback callback)
    {
        if (downloadItem.IsValid)
        {
            if (downloadItem.IsComplete)
            {
                Console.WriteLine("Download completed");
            }
        }
    }
}
browser.DownloadHandler = new MyDownloadHandler();
```


**DotNetBrowser**
```csharp
browser.StartDownloadHandler =
    new Handler<StartDownloadParameters, StartDownloadResponse>(p =>
    {
        var fileName = p.Download.Info.SuggestedFileName;
        var targetPath = Path.GetFullPath(fileName);
        p.Download.Finished += (sender, args) =>
        {
            Console.WriteLine("Download completed");
        };

        // Return StartDownloadResponse.Cancel() to cancel the download.
        return StartDownloadResponse.DownloadTo(targetPath);
    });
```



If you don't configure this handler, DotNetBrowser handles the downloads
automatically. Inside a `BrowserView`, it presents the "Save As" dialog using
the application's UI library. Outside of that context, it cancels 
the download.

Visit the [guide on Downloads][guide-downloads] to find more details.

## Screenshots

In CefSharp, you can capture a screenshot only using the DevTools protocol.
DotNetBrowser provides a method for that — you don't need to use DevTools or
expose the remote debugging port:


**CefSharp**
```csharp
using (var devToolsClient = chromiumWebBrowser.GetDevToolsClient())
{
    var result = await devToolsClient.Page.CaptureScreenshotAsync();
    byte[] pixels = result.Data;
}
```


**DotNetBrowser**
```csharp
// Get the raw pixels of the current viewport.
// No DevTools or window required.
DotNetBrowser.Ui.Bitmap image = browser.TakeImage();

// Save the image to the file.
Bitmap bitmap = ToBitmap(image);
bitmap.Save("screenshot.png", ImageFormat.Png);
```



Check out the advanced [tutorial on taking screenshots][blog-screenshots] in
DotNetBrowser.

## DevTools

In both CefSharp and DotNetBrowser, you can configure 
the [remote debugging port][guide-rdp]
and open the DevTools for each browser:


**CefSharp**
```csharp
var settings = new CefSettings();
settings.RemoteDebuggingPort = 9222;
settings.CefCommandLineArgs.Add("remote-allow-origins=http://localhost:9222"); 
Cef.Initialize(settings);

...

// Open the dev tools window.
browser.ShowDevTools();
// Close it.
browser.HideDevTools();

```


**DotNetBrowser**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumSwitches = { "--remote-allow-origins=http://localhost:9222" },
    RemoteDebuggingPort = 9222
}.Build());

...

// Open the dev tools window.
browser.DevTools.Show();
// Close it.
browser.DevTools.Hide();

// Or open the dev tools in another browser by URL.
string url = browser.DevTools.RemoteDebuggingUrl;
```



DotNetBrowser doesn't provide an alternative to CefSharp's
`browser.GetDevToolsClient()`.

## User Agent

In CefSharp, you can configure the user agent in three ways:

* beforehand, when initializing CEF;
* at runtime, using the DevTools protocol;
* at runtime, by overriding the `User-Agent` header of a request.

In DotNetBrowser, you can set the default user agent when creating
the `IEngine`:


**DotNetBrowser**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    UserAgent = "<user-agent>"
}.Build());
```



At runtime, you can override this value for an individual browser:


**DotNetBrowser**
```csharp
browser.UserAgent = "<user-agent>";
```



Or for an individual request
using [`StartTransactionHandler`][event-before-start]:


**DotNetBrowser**
```csharp
network.StartTransactionHandler =
    new Handler<StartTransactionParameters, StartTransactionResponse>(p =>
        {
            var newHeaders = p.Headers.Cast<HttpHeader>().ToList();
            newHeaders.Add(
                new HttpHeader("User-Agent", "Mozilla/5.0 ..."));
            return StartTransactionResponse.OverrideHeaders(newHeaders);
        });
```



Alternatively, you can specify the [User Agent Client Hints][guide-ua-hints].

## Conclusion

If you've used CefSharp, you'll find that DotNetBrowser works in similar ways.
Most of the features are available, with a few changes in how they're used.

In this guide, we went through migrating the browser lifecycle management,
navigation, pop-ups and dialogs, JavaScript, and many more.

We hope that this guide will be of great help and make the migration from
CefSharp to DotNetBrowser a smooth experience.



[guide-nuget]: https://teamdev.com/dotnetbrowser/docs/guides/installation/nuget/
[guide-zip]: https://teamdev.com/dotnetbrowser/docs/guides/installation/zip/
[guide-vsix]: https://teamdev.com/dotnetbrowser/docs/guides/installation/vsix/
[blog-architecture]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/#in-process-vs-out-of-process
[blog-screenshots]: https://teamdev.com/dotnetbrowser/blog/taking-screenshots-of-web-pages/
[event-render-process]: https://teamdev.com/dotnetbrowser/docs/guides/gs/browser/#render-process-termination-event
[event-frame-load-finished]: https://teamdev.com/dotnetbrowser/docs/guides/gs/navigation/#frame-document-load-finished
[event-redirect-response]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#redirect-response-code-received
[event-before-url-request]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-url-request
[event-request-completed]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#request-completed
[event-before-start]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-start-transaction
[event-response-bytes]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#response-bytes-received
[guide-architecture]: https://teamdev.com/dotnetbrowser/docs/guides/architecture/
[guide-rendering-modes]: https://teamdev.com/dotnetbrowser/docs/guides/gs/browser-view/#rendering
[guide-profile]: https://teamdev.com/dotnetbrowser/docs/guides/gs/profile/
[guide-nav-events]: https://teamdev.com/dotnetbrowser/docs/guides/gs/navigation/#navigation-events
[guide-loading-post]: https://teamdev.com/dotnetbrowser/docs/guides/gs/navigation/#loading-url-with-post
[guide-executing-js]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/#executing-javascript
[guide-dotnet-from-js]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/#calling-net-from-javascript
[guide-client-cert]: https://teamdev.com/dotnetbrowser/docs/guides/gs/authentication/#https-client-certificate
[guide-proxy-auth]: https://teamdev.com/dotnetbrowser/docs/guides/gs/authentication/#proxy-basic-digest-and-ntlm-authentication
[guide-cert-verification]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#certificate-verification
[guide-popups]: https://teamdev.com/dotnetbrowser/docs/guides/gs/popups/#opening-pop-ups
[guide-inject-js]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/#injecting-javascript
[guide-js-dialogs]: https://teamdev.com/dotnetbrowser/docs/guides/gs/dialogs/#javascript-dialogs
[guide-downloads]: https://teamdev.com/dotnetbrowser/docs/guides/gs/downloads/#overview
[guide-rdp]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#remote-debugging-port
[guide-ua-hints]: https://teamdev.com/dotnetbrowser/docs/guides/gs/browser/#user-agent-client-hints
[section-intercepting]: https://teamdev.com/dotnetbrowser/blog/migrating-from-cefsharp-to-dotnetbrowser/#intercepting-traffic
[section-isolation]: https://teamdev.com/dotnetbrowser/blog/migrating-from-cefsharp-to-dotnetbrowser/#browser-isolation
