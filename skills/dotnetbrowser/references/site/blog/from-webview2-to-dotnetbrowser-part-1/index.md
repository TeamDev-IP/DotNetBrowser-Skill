# From WebView2 to DotNetBrowser: Part 1

This guide is for .NET developers evaluating a transition 
from WebView2 to DotNetBrowser. This is the first part of a two-part series.

Each section of this guide focuses on one area of functionality that commonly
appears in applications embedding a `WebView2` control.

We will provide drop-in replacements for your existing code, highlight subtle
differences between DotNetBrowser and WebView2, and include useful links to
related documentation.

This guide is about **how** to migrate to DotNetBrowser. To learn more about 
**why**, check out the [DotNetBrowser or WebView2 article][dotnetbrowser-vs-wv2].

## Installing dependencies

Adding DotNetBrowser to your project is most straightforward through NuGet.
Install the UI‑specific package that matches your app, and NuGet will pull in
the core API package and the platform Chromium binaries you need. 
That's it.

For example, here's how to add DotNetBrowser for a WPF project running on
Windows x64:

* `DotNetBrowser.Wpf.x64` – WPF integration.
* (Pulled transitively) `DotNetBrowser.Win-x64` – core API.
* (Pulled transitively) `DotNetBrowser.Chromium.Win-x64` – bundled Chromium.

You can see the complete list of NuGet packages for different UI libraries and
platforms in the [installation guide][nuget].

Not using NuGet? Add DotNetBrowser to your project as [DLL files][dll]
or [VSIX packages][vsix].

## Initializing the browser

Initializing WebView2 and DotNetBrowser is conceptually similar. In XAML-based
libraries, you'll need to add a browser control to XAML, then initialize 
the Chromium engine in a code-behind file.

**MainWindow.xaml:**

**WebView2**
```xml
<Window ...
        x:Class="WebView2Example.MainWindow"
        xmlns:local="clr-namespace:WebView2Example"
        Title="WebView2" Width="800" Height="600" Closed="Window_Closed">
    <Grid>
        <Wpf:WebView2 Name="webView"/>
    </Grid>
</Window>
```


**DotNetBrowser**
```xml
<Window ...
        x:Class="DotNetBrowserExample.MainWindow"
        xmlns:local="clr-namespace:DotNetBrowserExample"
        Title="DotNetBrowser" Width="800" Height="600" Closed="Window_Closed">
    <Grid>
        <WPF:BrowserView Name="browserView"/>
    </Grid>
</Window>
```



**MainWindow.xaml.cs:**


**WebView2**
```csharp
public partial class MainWindow : Window
{
    private const string Url = "https://example.com/";

    public MainWindow()
    {
        InitializeComponent();
        InitializeWebViewAsync();
    }

    async void InitializeWebViewAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.Navigate(Url);
    }

    private void Window_Closed(object sender, EventArgs e)
    {
        webView.Dispose();
    }
}
```


**DotNetBrowser**
```csharp
public partial class MainWindow : Window
{
    private const string Url = "https://example.com/";
    private readonly IBrowser browser;
    private readonly IEngine engine;

    public MainWindow()
    {
        engine = EngineFactory.Create(RenderingMode.HardwareAccelerated);
        browser = engine.CreateBrowser();

        InitializeComponent();
        browserView.InitializeFrom(browser);
        browser.Navigation.LoadUrl(Url);
    }

    private void Window_Closed(object sender, EventArgs e)
    {
        engine?.Dispose();
    }
}
```



In WebView2, the engine is mostly hidden. You place a `WebView2` control in
XAML, and call `EnsureCoreWebView2Async()` to spin up the runtime behind 
the scenes. Once initialized, you use `CoreWebView2` to navigate or 
interact with the page.

In DotNetBrowser, the engine is explicit. You create an `IEngine` object,
then `IBrowser`, and finally wire the browser into the `BrowserView` UI control.

This separation gives you more control over browser lifetime, resource usage,
and session isolation. You can create multiple engines per application, and
multiple browsers per engine. The `IBrowser` instances are fully functional from
the get-go, they can work in a headless mode.

## Closing the browser

WebView2 ties Edge lifetime to the last living control; once all WebView2
instances are closed, the whole engine exits.

DotNetBrowser lets you shut down an individual browser *or* the entire engine.
Note that the lifetime of the engine is independent of individual browsers:
you always need to close `IEngine` explicitly.


**WebView2**
```csharp
// Close a single WebView2 control.
webView.Dispose();
// Once all controls are closed, the Edge process exits.
```


**DotNetBrowser**
```csharp
// Close a single browser.
browser.Disposed += (sender, args) =>
{
    Console.WriteLine("The browser was closed!");
};
browser.Dispose();

// Close a single engine. It will automatically close all 
// browsers within it. 
//
// It will not close other IEngine instances.
engine.Disposed += (sender, args) =>
{
    Console.WriteLine("The engine was closed!");
};
engine.Dispose();
```



Note that the `browser.Disposed` event is not equivalent to WebView2's
`WindowCloseRequested`. The latter is raised only when JavaScript
calls `window.close()` on the top‑level view. The former is **always** raised
when the browser is disposed, regardless of how it happened.

## Navigation

Navigation API is mostly equivalent in both WebView2 and DotNetBrowser:


**WebView2**
```csharp
webView.CoreWebView2.Navigate("https://www.example.com");
webView.CoreWebView2.GoBack();
webView.CoreWebView2.GoForward();
webView.CoreWebView2.Reload();
webView.CoreWebView2.Stop();
bool canGoBack = webView.CoreWebView2.CanGoBack;
bool canGoForward = webView.CoreWebView2.CanGoForward;
```


**DotNetBrowser**
```csharp
browser.Navigation.LoadUrl("https://example.com");
browser.Navigation.GoBack();
browser.Navigation.GoForward();
browser.Navigation.Reload();
browser.Navigation.Stop();
bool canGoBack = browser.Navigation.CanGoBack();
bool canGoForward = browser.Navigation.CanGoForward();
```



### Navigation events

This section describes the closest DotNetBrowser equivalents to WebView2
navigation events. In several cases you will need to combine multiple events or
handlers to fully replicate WebView2 semantics.

Replace `NavigationStarting` with `NavigationStarted` to detect when navigation
begins, and use `StartNavigationHandler` to cancel the navigation.


**WebView2**
```csharp
// Occurs when the browser starts loading a new page.
webView.CoreWebView2.NavigationStarting += (sender, args) =>
{
    Console.WriteLine("Navigation started.");
    // Cancel the navigation.
    args.Cancel = true;
};
```


**DotNetBrowser**
```csharp
// Occurs when the browser starts loading a new page.
browser.Navigation.NavigationStarted += (sender, args) =>
{
    Console.WriteLine("Navigation started.");
};

// Cancel the navigation.
browser.Navigation.StartNavigationHandler =
    new Handler<
          StartNavigationParameters, 
          StartNavigationResponse>
          (p => StartNavigationResponse.Ignore());
```



Replace `ContentLoading` with `LoadStarted` to detect when loading begins,
and `FrameLoadFailed` to handle errors.


**WebView2**
```csharp
webView.CoreWebView2.ContentLoading += (sender, args) =>
{
    Console.WriteLine("Loading started.");
    // True if the loaded content is an error page.
    bool isErrorPage = args.IsErrorPage;
};
```


**DotNetBrowser**
```csharp
browser.Navigation.LoadStarted += (sender, args) => 
{ 
    Console.WriteLine("Loading started.");
};

// Occurs when a content load is failed.
browser.Navigation.FrameLoadFailed += (sender, args) =>
{
    NetError errorCode = args.ErrorCode;
};
```



Replace `NavigationCompleted` with `NavigationFinished` event:


**WebView2**
```csharp
webView.CoreWebView2.NavigationCompleted += (sender, args) =>
{
    var webErrorStatus = args.WebErrorStatus;
    var isSuccess = args.IsSuccess;
};
```


**DotNetBrowser**
```csharp
browser.Navigation.NavigationFinished += (sender, args) =>
{
    // Error code if the navigation failed.
    var errorCode = args.ErrorCode;
    // Indicates if the navigation resulted in the error page.
    var isErrorPage = args.IsErrorPage;
};
```



Replace `FrameCreated` with the event of the same name, `FrameCreated`. You can
use this event to cache the `IFrame` instance. However, the JavaScript context
and DOM tree might not be available immediately.
Use `FrameDocumentLoadFinished` and `InjectJsHandler`
to determine when the page is [ready for interaction][when-execute-js].


**WebView2**
```csharp
webView.CoreWebView2.FrameCreated += (sender, args) =>
{
    CoreWebView2Frame frame = args.Frame;
};
```


**DotNetBrowser**
```csharp
browser.FrameCreated += (sender, args) =>
{
    IFrame frame = args.Frame;
};
```



Replace `FrameNavigationCompleted` with the pair of `FrameLoadFinished`
and `FrameLoadFailed`:


**WebView2**
```csharp
// Occurs when a child frame body.onload event has been raised 
// or loading stopped with error.
webView.CoreWebView2.FrameNavigationCompleted += (sender, args) =>
{
    CoreWebView2WebErrorStatus errorStatus = args.WebErrorStatus;
    int httpStatusCode = args.HttpStatusCode;
    bool isSuccess = args.IsSuccess;
};
```


**DotNetBrowser**
```csharp
browser.Navigation.FrameLoadFinished += (sender, args) =>
{
    IFrame frame = args.Frame;
    string validatedUrl = args.ValidatedUrl;
};

browser.Navigation.FrameLoadFailed += (sender, args) =>
{
    IFrame frame = args.Frame;
    NetError errorCode = args.ErrorCode;
    string validatedUrl = args.ValidatedUrl;
};
```



The `SourceChanged` event doesn't have an equivalent in DotNetBrowser. 
The closest alternative is the `NavigationStarted` event with a condition:


**WebView2**
```csharp
webView.CoreWebView2.SourceChanged += (sender, args) =>
{
    var isNewDocument = args.IsNewDocument;
};
```


**DotNetBrowser**
```csharp
browser.Navigation.NavigationStarted += (sender, args) =>
{
    if (args.IsMainFrame)
    {
        var isNewDocument = !args.IsSameDocument;
    }
};
```



Visit the [guide on navigation][navigation-guide] to see the full list of
navigation events in DotNetBrowser.

### Loading with POST data

In both WebView2 and DotNetBrowser, you can navigate to a URL using a POST
request:


**WebView2**
```csharp
var postData = "username=test&password=1234";
var byteArray = Encoding.UTF8.GetBytes(postData);
var stream = new MemoryStream(byteArray);

var request = webView.CoreWebView2.Environment.CreateWebResourceRequest(
     uri: "https://example.com",
     Method: "POST",
     postData: stream,
     Headers: "Content-Type: application/x-www-form-urlencoded\r\n"
    );
webView.CoreWebView2.NavigateWithWebResourceRequest(request);
```


**DotNetBrowser**
```csharp
KeyValuePair<string, string>[] formData = 
{
    new KeyValuePair<string, string>("username", "test"),
    new KeyValuePair<string, string>("password", "1234")
};
LoadUrlParameters request = new LoadUrlParameters("https://example.com")
{
    UploadData = new FormData(formData)
};
browser.Navigation.LoadUrl(request);
```



When sending POST data, DotNetBrowser automatically sets the `Content-Type`
and `Content-Length` headers. In the multipart case, it will also include 
the form boundary plus each part's `Content-Disposition` and 
`Content-Type`.

You can override the default headers and add more in the
<a href="https://api.dotnetbrowser.dev/4.3.3/api/DotNetBrowser.Navigation.LoadUrlParameters.HttpHeaders.html#DotNetBrowser_Navigation_LoadUrlParameters_HttpHeaders">
HttpHeaders</a>
parameter.

## JavaScript

Both libraries let you execute scripts, receive results, and allow page scripts
call the .NET code. The differences are in typing and plumbing.

### When to start executing JavaScript

After Chromium finishes loading the page, it needs additional time to create the
JavaScript context and DOM tree. You can successfully execute JavaScript only
after this step completes.

Replace the pair of WebView's `DOMContentLoaded` events with a
single `FrameDocumentLoadFinished` event to ensure the frame is ready to execute
JavaScript:


**WebView2**
```csharp
webView.CoreWebView2.DOMContentLoaded += (sender, args) =>
{
    Console.WriteLine("Ready to execute JS in the main frame.");
};

webView.CoreWebView2.FrameCreated += (s, e) =>
{
    var frame = e.Frame;
    frame.DOMContentLoaded += (sender, args) =>
       {
           Console.WriteLine("Ready to execute JS in an iframe.");
       };
};
```


**DotNetBrowser**
```csharp
browser.Navigation.FrameDocumentLoadFinished += (sender, args) =>
{
    if (args.Frame.IsMain)
    {
        Console.WriteLine("Ready to execute JS in the main frame.");
    }
    else
    {
        Console.WriteLine("Ready to execute JS in an iframe.");
    }
};
```



If you want to execute JavaScript before any scripts on the page run, you're
most likely using the `AddScriptToExecuteOnDocumentCreatedAsync` method. 
The alternative in DotNetBrowser is `InjectJsHandler`:


**WebView2**
```csharp
webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("...");
```


**DotNetBrowser**
```csharp
browser.InjectJsHandler = new Handler<InjectJsParameters>(args =>
{
  args.Frame.ExecuteJavaScript<IJsObject>("...");
});
```



### Calling JavaScript from .NET

WebView2 always returns a JSON string. Special values such as `undefined` and
non-serializable objects are returned as the literal string `"null"`.

DotNetBrowser converts JavaScript values into the corresponding .NET types.
Primitive values map automatically to native .NET types, while complex values
are wrapped into `IJsObject`, `IJsArray`, or `IJsFunction`:


**WebView2**
```csharp
// Returns the string "4".
string four = await webView.CoreWebView2.ExecuteScriptAsync("2 + 2");
// Returns the string "null", because `window` can't be serialized.
string window = await webView.CoreWebView2.ExecuteScriptAsync("window");
// You can do the same asynchronously:
var result = 
    await webView.CoreWebView2.ExecuteScriptWithResultAsync("2 + 2");
string fourAsync = scriptResult.ResultAsJson;
```


**DotNetBrowser**
```csharp
// Returns the number as double.
double four = await browser.MainFrame.ExecuteJavaScript<double>("2 + 2");
// Returns the functional IJsObject wrapper.
IJsObject window = await args.Frame.ExecuteJavaScript<IJsObject>("window");
```



Visit the guide on [JavaScript][js-guide-exec] for more details.

### Calling .NET from JavaScript

WebView2 provides two communication patterns: message passing
through `window.chrome.webview.postMessage()`, and direct calls via injected
COM-visible host objects.

DotNetBrowser uses the direct calls and allows you to inject arbitrary .NET
objects into JavaScript. No COM required.


**WebView2**
```js
window.chrome.webview.postMessage({action: "hello", name: "John"});
window.chrome.webview.hostObjects.bridge.SayHello("John");
```


**DotNetBrowser**
```js
// You can emulate the same path to the injected objects:
window.chrome.webview.postMessage({action: "hello", name: "John"});
window.chrome.webview.hostObjects.bridge.SayHello("John");

// Or inject .NET objects to arbitrary places:
window.postMessage({action: "hello", name: "John"});
window.myHostObjects.SayHello("John");
```



If you're using the `postMessage()` method, you can emulate it in DotNetBrowser
and avoid rewriting existing JavaScript code. But you will need to replace
the `WebMessageReceived` event handler with an object:


**WebView2**
```csharp
webView.CoreWebView2.WebMessageReceived += (s, e) =>
{
    var jsonString= e.WebMessageAsJson;
    Console.WriteLine($"{jsonString}");
};
```


**DotNetBrowser**
```csharp
public class Bridge
{
    public void postMessage(Object message)
    {
        // Beware, the `message` will not be string, 
        // if the underlying JS object is not a string.
        Console.WriteLine($"{message}");
    }
}

var bridge = new Bridge();
browser.InjectJsHandler = new Handler<InjectJsParameters>(args =>
{
    // Create a JavaScript object with the same name 
    // and path as in WebView2.
    IJsObject webview = args.Frame.ExecuteJavaScript<IJsObject>(
             "(window.chrome.webview = {})").Result;
    // Creat ethe `postMessage` property and assign it to a .NET method.
    webview.Properties["postMessage"] = (Action<Object>) bridge.postMessage;
});
```



Similarly, you can replace injected COM-objects with arbitrary .NET objects:


**WebView2**
```csharp
[ComVisible(true)]
[ClassInterface(ClassInterfaceType.AutoDual)]
public class Bridge
{
    public void SayHello(string name)
    {
        MessageBox.Show($"Hello {name}!");
    }
}

webView.CoreWebView2.AddHostObjectToScript("bridge", new Bridge());
```


**DotNetBrowser**
```csharp
public class Bridge
{
    public void SayHello(string name)
    {
        MessageBox.Show($"Hello {name}!");
    }
}

browser.InjectJsHandler = new Handler<InjectJsParameters>(args =>
{
    // Create a JavaScript object with the same name 
    // and path as in WebView2.
    IJsObject webview = args.Frame.ExecuteJavaScript<IJsObject>(
             "(window.chrome.webview = {hostObjects: {}})").Result;
    IJsObject hosts = webview.Properties["hostObjects"] as IJsObject;         
    // Create the `postMessage` property and assign it to a .NET method.
    hosts.Properties["bridge"] = new Bridge();
});
```



Check out the [JavaScript guide][js-guide] to learn more about
the .NET-JavaScript bridge.

## Intercepting traffic

In WebView2, traffic interception happens in two steps. First, you register
filters to isolate specific requests, then you register a handler to process
those requests:


**WebView2**
```csharp
// Intercept only HTTPS requests for images resources.
webView.CoreWebView2
    .AddWebResourceRequestedFilter(
        "https://*", CoreWebView2WebResourceContext.Image);


webView.CoreWebView2.WebResourceRequested += (sender, args) =>
{
    if (...) {
        // Don't handle this request.
        return;
    }
    // Serve your own response.
    var response = 
        webView.CoreWebView2.Environment.CreateWebResourceResponse(...);
    args.Response = response;
};
```



By default, these filters work for the standard schemes: `http`, `https`,
and `file`. If you want to intercept requests for a `custom-scheme://`, you need
to register the custom scheme when initializing the engine:


**WebView2**
```csharp
var schemes = new List<CoreWebView2CustomSchemeRegistration>()
{
    new CoreWebView2CustomSchemeRegistration("custom-scheme")
};
var options = new CoreWebView2EnvironmentOptions(
                     null, null, null, false, schemes);
var env = await CoreWebView2Environment.CreateAsync(null, null, options);
await webView.EnsureCoreWebView2Async(env);

// Now, this will work too:
webView.CoreWebView2
    .AddWebResourceRequestedFilter("custom-scheme://*", ...);
```



In DotNetBrowser, traffic interception occurs without prior filtering — 
the corresponding handler is called for every request. For this, set up 
an `InterceptRequestHandler` for every scheme you need:


**DotNetBrowser**
```csharp
// Create the engine with request handlers for different schemes.
EngineOptions options = new EngineOptions.Builder
{
    Schemes =
    {
        {Scheme.Create("custom-scheme"), new CustomSchemeInterceptor()},
        {Scheme.Create("https"), new HttpsSchemeInterceptor()}
    }
}.Build();
var engine = EngineFactory.Create(options);
```



In this handler, you either let the request through, or serve your own response:


**DotNetBrowser**
```csharp
class CustomSchemeInterceptor : 
    IHandler<InterceptRequestParameters, InterceptRequestResponse>
{
    public InterceptRequestResponse Handle(InterceptRequestParameters p)
    {
        string uri = p.UrlRequest.Url;
        UrlRequestJob urlRequestJob = null;
        if (p.UrlRequest.ResourceType == ResourceType.Image)
        {
            // Serve your own custom response.
            urlRequestJob = 
                 p.Network.CreateUrlRequestJob(p.UrlRequest,
                     new UrlRequestJobOptions
                     {
                         HttpStatusCode = HttpStatusCode.OK,
                         Headers = new List<HttpHeader>
                         {
                             new HttpHeader("Content-Type", "text/plain"),
                         }
                     });
            byte[] body = loadImageFromDisk(p.UrlRequest.Url);
            urlRequestJob.Write(body);
            urlRequestJob.Complete();
            return InterceptRequestResponse.Intercept(urlRequestJob);
        }
        // Let other requests through.
        return InterceptRequestResponse.Proceed();
    }
}
```



Request interception has a **performance overhead**. If you only need to block
unwanted requests, use a more lightweight `SendUrlRequestHandler`.

Read more about handling custom schemes in
the [guide on intercepting requests][scheme-guide].

## DOM

WebView2 does not expose a native DOM API; interaction with page content occurs
by executing JavaScript and parsing the JSON result.

DotNetBrowser provides two options: you can continue using your existing
JavaScript snippets or switch to a typed DOM API that exposes elements as .NET
objects.

The drop-in replacement for your WebView2 code looks very similar:


**WebView2**
```csharp
string jsCode = "document.getElementById('username').value";
string username = await webView.CoreWebView2.ExecuteScriptAsync(jsCode);
```


**DotNetBrowser**
```csharp
string jsCode = "document.getElementById('username').value";
string username = await browser.MainFrame.ExecuteJavaScript<string>(jsCode);
```



Alternatively, you can use the DotNetBrowser DOM API:


**DotNetBrowser**
```csharp
// Re-use existing JavaScript selectors.
IElement element = await frame.ExecuteJavaScript<IElement>(
      "document.getElementById('username')");
string username = (element as IInputElement).Value;

// Or use C# selectors.
IDocument document = browser.MainFrame.Document;
IInputElement inputElement = 
    document.GetElementById("username") as IInputElement;
username = inputElement.Value;
```



**Why use the DOM API?** Better IntelliSense, compile‑time refactoring, and
strongly‑typed C#. Refer to the [guide on DOM][dom-guide] for mode details.

## JavaScript dialogs

In WebView2, you handle all JavaScript dialogs in a single `ScriptDialogOpening`
event handler. In DotNetBrowser, you replace this with separate handlers for
each dialog type:


**WebView2**
```csharp
webView.CoreWebView2.ScriptDialogOpening += (sender, args) =>
{
    switch (args.Kind)
    {
        case CoreWebView2ScriptDialogKind.Alert:
            Console.WriteLine("Alert dialog called.");
            break;
        case CoreWebView2ScriptDialogKind.Confirm:
            Console.WriteLine("Confirm dialog called.");
            args.Accept();
            break;
        case CoreWebView2ScriptDialogKind.Prompt:
            Console.WriteLine("Prompt dialog called.");
            args.ResultText = "some response";
            args.Accept();
            break;
        case CoreWebView2ScriptDialogKind.Beforeunload:
            Console.WriteLine("Beforeunload dialog called.");
            break;
    }
};
```

**DotNetBrowser**
```csharp
var dialogs = browser.JsDialogs;
dialogs.AlertHandler = new Handler<AlertParameters>(p =>
    {
        Console.WriteLine("Alert dialog called.");
    });
dialogs.ConfirmHandler =
    new Handler<ConfirmParameters, ConfirmResponse>(p =>
    {
        Console.WriteLine("Confirm dialog called.");
        return ConfirmResponse.Ok();
    });
dialogs.PromptHandler =
    new Handler<PromptParameters, PromptResponse>(p =>
    {
        Console.WriteLine("Prompt dialog called.");
        return PromptResponse.SubmitText("some response");
    });
dialogs.BeforeUnloadHandler =
    new Handler<BeforeUnloadParameters, BeforeUnloadResponse>(p =>
    {
        Console.WriteLine("Beforeunload dialog called.");
        return BeforeUnloadResponse.Leave();
    });
```



If you don't set up a handler, DotNetBrowser handles the dialogs automatically.
Inside a `BrowserView`, it presents the dialog using the application's UI
library. Outside of that context, it skips the dialogs as if the user pressed 
"Cancel".

## Native dialogs

Native dialogs originate from browser actions, such as file upload buttons, PDF
save prompts, form repost warnings, external app launch
triggers, `<input type="color">`, and more.

In WebView2, overriding native dialogs requires hacky workarounds. 

In DotNetBrowser, you can override any native dialog by registering 
a respective event handler:

* `OpenDirectoryHandler` for the "Open directory" dialog.
* `OpenFileHandler` for the "Open file" dialog.
* `OpenMultipleFilesHandler` for the "Open files" dialog.
* `OpenExternalAppHandler` for the dialog when the browser wants to open 
  an external app.
* `RepostFormHandler` for the "Confirm Form Resubmission" dialog.
* `SaveAsPdfHandler` for selecting a file when saving the page as PDF via 
   the Print Preview dialog.
* `SaveFileHandler` for the "Save file" dialog.
* `SelectColorHandler` for the color picker.

Below is an example demonstrating how to override an `OpenFileHandler`:


**DotNetBrowser**
```csharp
browser.Dialogs.OpenFileHandler =
    new Handler<OpenFileParameters, OpenFileResponse>(parameters =>
    {
        var initialDirectory = parameters.InitialDirectory;
        var acceptableExtensions = parameters.AcceptableExtensions;
        return OpenFileResponse.SelectFile(...);
    });
```



We have more examples in the [guide on dialogs][dialogs-guide].

## Popup windows

The browser creates a popup window when JavaScript calls window.open or when a
user clicks a link with `target="_blank"`.

In WebView2, pop-up window creation is controlled through
the `NewWindowRequested` event handler. You can choose to suppress 
the pop-up, open it in the same WebView2 control, or let it create 
a new window.

In DotNetBrowser, pop-up creation is managed using the `CreatePopupHandler`,
where you decide whether to allow or suppress the pop-up. If you decide to
create it, DotNetBrowser instantiates a new `IBrowser` and passes it to
the `OpenPopupHandler`. You can then either show it in the UI
using `BrowserView` or run it in headless mode.

Displaying the new browser in the same `BrowserView` control is not directly
supported, though it can be emulated:


**WebView2**
```csharp
webView.CoreWebView2.NewWindowRequested += (sender, e) =>
{
    if (openInSameBrowser)
    {
        e.NewWindow = (CoreWebView2)sender;
    } 
    else
    {
        // Prevent default popup behavior.
        e.Handled = true;
        // Create a new popup window.
        CreatePopup(e);
    }
};

private async void CreatePopup(CoreWebView2NewWindowRequestedEventArgs popup)
{
    // Create and configure the new window.
    Window popupWindow = new Window();
    ...

    // Create a new WebView2 control to display the new browser.
    WebView2 popupWebView = new WebView2();
    popupWindow.Content = popupWebView;
    popupWindow.Show();

    CoreWebView2Environment env = webView.CoreWebView2.Environment;
    await popupWebView.EnsureCoreWebView2Async(env);
    popupWebView.CoreWebView2.Navigate(popup.Uri);
}
```


**DotNetBrowser**
```csharp
browser.CreatePopupHandler =
    new Handler<CreatePopupParameters, CreatePopupResponse>(p =>
    {
        if (openInSameBrowser)
        {
            browser.Navigation.LoadUrl(p.TargetUrl);
            return CreatePopupResponse.Suppress();
        }
        return CreatePopupResponse.Create();
    });

browser.OpenPopupHandler = new Handler<OpenPopupParameters>(p =>
{
    Action createPopupAction = () =>
    {
        CreatePopupWindow(p.PopupBrowser, p.Rectangle);
    };
    Dispatcher.BeginInvoke(createPopupAction);
});

void CreatePopupWindow(IBrowser popupBrowser, Rectangle rect)
{
    // This method runs on the UI thread.
    BrowserView popupBrowserView = new BrowserView();
    popupBrowserView.InitializeFrom(popupBrowser);

    // Create and configure the new window.
    Window popupWindow = new Window();
    popupWindow.Content = popupBrowserView;
    popupWindow.Show();
    // ...
}
```



If no handler is configured, DotNetBrowser manages pop-ups automatically. When
inside a `BrowserView`, it will open a new window using the application's UI
library, otherwise it suppresses the dialogs.

## Conclusion

In this guide, we have covered how to create and close the browser,
navigate pages, interact with JavaScript, handle dialogs and pop-up windows, and
intercept network traffic.

In the upcoming part 2, we'll continue explaining how to transition from
WebView2 to DotNetBrowser and cover the following advanced topics:

* Proxy and authentication flows
* Cookies and persistent storage
* Profiles
* Context menus
* Downloads
* Printing APIs
* DevTools integration
* Chrome extensions



[dotnetbrowser-vs-wv2]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/
[nuget]: https://teamdev.com/dotnetbrowser/docs/guides/installation/nuget/
[dll]: https://teamdev.com/dotnetbrowser/docs/guides/installation/zip/
[vsix]: https://teamdev.com/dotnetbrowser/docs/guides/installation/vsix/
[navigation-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/navigation/#navigation-events
[http-headers]: https://api.dotnetbrowser.dev/3.3.1/api/DotNetBrowser.Navigation.LoadUrlParameters.HttpHeaders/#DotNetBrowser_Navigation_LoadUrlParameters_HttpHeaders
[when-execute-js]: https://teamdev.com/dotnetbrowser/blog/from-webview2-to-dotnetbrowser-part-1/#when-to-start-executing-javascript
[js-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/
[js-guide-exec]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/#executing-javascript
[scheme-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#intercept-request-per-uri-scheme
[dom-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/dom/
[dialogs-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/dialogs/
[support]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/#fixes-features-and-assistance
