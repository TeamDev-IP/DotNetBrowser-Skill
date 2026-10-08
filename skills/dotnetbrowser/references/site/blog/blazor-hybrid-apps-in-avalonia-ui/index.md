# Blazor hybrid apps in Avalonia UI

Blazor is a .NET front end framework for building web apps using only .NET
technologies. In 2021, Blazor extended to the desktop with Blazor Hybrid,
allowing developers to use their existing skills on desktop platforms.

Blazor Hybrid apps are traditional desktop apps that host the actual Blazor web
app inside a web view control. They use .NET MAUI for the desktop side, but you
can use another framework if it doesn't meet your requirements.

The lack of Linux support and the use of different browser engines on Windows
and macOS are limitations of MAUI. Microsoft Edge and Safari vary in how they
implement web standards, execute JavaScript, and render pages. In advanced apps,
this difference can be a source of bugs and require additional testing.

If MAUI is not an option, consider opting for Avalonia UI — a cross-platform UI
library with several Chromium-based web views in its ecosystem.

In this article, we explore how to use Avalonia UI to create Blazor Hybrid apps
with DotNetBrowser as a web view.

## Quick start with a template

To create a basic Blazor Hybrid app with DotNetBrowser and Avalonia UI use our
template:

```shell
dotnet new install DotNetBrowser.Templates
```

Then, get a free 30-day evaluation license for DotNetBrowser.



Create a Blazor Hybrid app from the template and pass your license key as a
 parameter:

```shell
dotnet new dotnetbrowser.blazor.avalonia.app -o Blazor.AvaloniaUi -li <your_license_key>
```

And run the app:

```shell
dotnet run --project Blazor.AvaloniaUi
```
![Blazor Hybrid app on Avalonia UI on Linux](https://teamdev.com/dotnetbrowser/blog/blazor-hybrid-apps-in-avalonia-ui/blazor-hybrid-avalonia-linux.webp)
<p class="image-caption">Blazor Hybrid app on Avalonia UI on Linux.</p>

## Implementation

In the hybrid environment, the Blazor app runs in the process of its desktop
shell. That shell, or a window, manages the lifecycle of the whole app, shows
the web view, and starts the Blazor app. We're going to create that window with
Avalonia UI.

The Blazor app's back end is .NET code, and the front end is web content hosted
inside a web view. The browser engine inside a web view and the .NET runtime
don't have a direct connection. So, for the back and front end to communicate,
Blazor must know how to exchange data between them. We're introducing a new web
view, so we must teach Blazor how to do it with DotNetBrowser.

Next, we’ll walk you through the key pieces that integrate Blazor with Avalonia
and DotNetBrowser. Check out the template above for the complete solution.

### Creating a window

To host a Blazor Hybrid app, we need to create a regular Avalonia window with a
web view component. 

**MainWindow.axaml**

```xml
<Window ... Closed="Window_Closed">
    <browser:BlazorBrowserView x:Name="BrowserView" ... />
        ...
    </browser:BlazorBrowserView>
</Window>
```

**MainWindow.axaml.cs**
```cs
public partial class MainWindow : Window
{
    public MainWindow()
    {
        InitializeComponent();
	 ...	
        BrowserView.Initialize();
    }

    private void Window_Closed(object sender, EventArgs e)
    {
        BrowserView.Shutdown();
    }
}
```

The `BlazorBrowserView` is an Avalonia control that we create to encapsulate
DotNetBrowser. Later we will integrate it with Blazor in this control.

**BlazorBrowserView.axaml**
```xml
<UserControl ...>
    ...
    <avaloniaUi:BrowserView x:Name="BrowserView" IsVisible="False" ... />
</UserControl>
```

**BlazorBrowserView.axaml.cs**
```cs
public partial class BlazorBrowserView : UserControl
{
    private IEngine engine;
    private IBrowser browser;

    public BlazorBrowserView()
    {
        InitializeComponent();
    }

    public async Task Initialize()
    {
        EngineOptions engineOptions = new EngineOptions.Builder
        {
            RenderingMode = RenderingMode.HardwareAccelerated
        }.Build();
        engine = await EngineFactory.CreateAsync(engineOptions);
        browser = engine.CreateBrowser();
        ...
        Dispatcher.UIThread.InvokeAsync(ShowView);
    }

    public void Shutdown()
    {
        engine?.Dispose();
    }

    private void ShowView()
    {
        BrowserView.InitializeFrom(browser);
        BrowserView.IsVisible = true;
        browser?.Focus();
    }
}
```

### Configuring Blazor

In hybrid apps, the main entity responsible for integration between Blazor and
the environment is `WebViewManager`. This is an abstract class, so we create our
own implementation called `BrowserManager` and instantiate it in
`BlazorBrowserView`.

**BrowserManager.cs**
```cs
class BrowserManager : WebViewManager
{
    private static readonly string AppHostAddress = "0.0.0.0";
    private static readonly string AppOrigin = $"https://{AppHostAddress}/";
    private static readonly Uri AppOriginUri = new(AppOrigin);

    private IBrowser Browser { get; }

    public BrowserManager(IBrowser browser, IServiceProvider provider,
                          Dispatcher dispatcher,
                          IFileProvider fileProvider,
                          JSComponentConfigurationStore jsComponents,
                          string hostPageRelativePath)
        : base(provider, dispatcher, AppOriginUri, fileProvider, jsComponents,
               hostPageRelativePath)
    {
        Browser = browser;
    }
    
    ...
}
```

**BlazorBrowserView.axaml.cs**
```cs {hl_lines=18}
public partial class BlazorBrowserView : UserControl
{
    private IEngine engine;
    private IBrowser browser;
    private BrowserManager browserManager;

    ...

    public async Task Initialize()
    {
        EngineOptions engineOptions = new EngineOptions.Builder
        {
            RenderingMode = RenderingMode.HardwareAccelerated
        }.Build();
        engine = await EngineFactory.CreateAsync(engineOptions);
        browser = engine.CreateBrowser();
        ...
        browserManager = new BrowserManager(browser, ...);
        ...
    }
    ...
}
```

A Blazor app requires one or more root components. We add them to WebViewManager
when the web view is being initialized.

**RootComponent.cs**
```cs
public class RootComponent
{
    public string ComponentType { get; set; }
    public IDictionary<string, object> Parameters { get; set; }
    public string Selector { get; set; }

    public Task AddToWebViewManagerAsync(BrowserManager browserManager)
    {
        ParameterView parameterView = Parameters == null
                                          ? ParameterView.Empty
                                          : ParameterView.FromDictionary(Parameters);
        return browserManager?.AddRootComponentAsync(
                Type.GetType(ComponentType)!, Selector, parameterView);
    }
}
```

**BlazorBrowserView.axaml.cs**
```cs {hl_lines=[6,"15-18"]}
public partial class BlazorBrowserView : UserControl
{
    private IEngine engine;
    private IBrowser browser;
    private BrowserManager browserManager;
    public ObservableCollection<RootComponent> RootComponents { get; set; } = new();
    ...
    public async Task Initialize()
    {
        ...
        engine = await EngineFactory.CreateAsync(engineOptions);
        browser = engine.CreateBrowser();
        browserManager = new BrowserManager(browser, ...);
        
        foreach (RootComponent rootComponent in RootComponents)
        {
            await rootComponent.AddToWebViewManagerAsync(browserManager);
        }
        ...
    }
    ...
}
```

**MainWindow.axaml**
```xml {hl_lines=["3-5"]}
<Window ... Closed="Window_Closed">
    <browser:BlazorBrowserView x:Name="BrowserView" ... />
        <browser:BlazorBrowserView.RootComponents>
           <browser:RootComponent Selector="..." ComponentType="..." />
        </browser:BlazorBrowserView.RootComponents>
    </browser:BlazorBrowserView>
</Window>
```

### Loading static resources

In a regular web app, the browser loads pages and static resources by making
HTTP requests to a server. In a Blazor Hybrid app, it works the same way, but
there is no server. Instead, `WebViewManager` provides a method called
`TryGetResponseContent` that takes a URL and returns data as a quasi HTTP
 response.

We deliver HTTP requests and responses to this method and back by intercepting
HTTPS traffic in DotNetBrowser.

**BlazorBrowserView.axaml.cs**
```cs {hl_lines=["13-20", "29-31"]}
public partial class BlazorBrowserView : UserControl
{
    private IEngine engine;
    private IBrowser browser;
    private BrowserManager browserManager;
    ...

    public async Task Initialize()
    {
        EngineOptions engineOptions = new EngineOptions.Builder
        {
            RenderingMode = RenderingMode.HardwareAccelerated,
            Schemes =
            {
                {
                    Scheme.Https,
                    new Handler<InterceptRequestParameters,
                        InterceptRequestResponse>(OnHandleRequest)
                }
            }
        }.Build();

        engine = await EngineFactory.CreateAsync(engineOptions);
        browser = engine.CreateBrowser();
        browserManager = new BrowserManager(browser, ...);
        ...
    }

    public InterceptRequestResponse OnHandleRequest(
            InterceptRequestParameters p) =>
            browserManager?.OnHandleRequest(p);

    ...
}
```

**BrowserManager.cs**
```cs
internal class BrowserManager : WebViewManager
{
    private static readonly string AppHostAddress = "0.0.0.0";
    private static readonly string AppOrigin = $"https://{AppHostAddress}/";
    private static readonly Uri AppOriginUri = new(AppOrigin);

    ...

    public InterceptRequestResponse OnHandleRequest(InterceptRequestParameters p)
    {
        if (!p.UrlRequest.Url.StartsWith(AppOrigin))
        {
            // If request doesn't start with AppOrigin, let it through.
            return InterceptRequestResponse.Proceed();
        }

        ResourceType resourceType = p.UrlRequest.ResourceType;
        bool allowFallbackOnHostPage = resourceType is ResourceType.MainFrame
                                           or ResourceType.Favicon
                                           or ResourceType.SubResource;

        if (TryGetResponseContent(p.UrlRequest.Url, allowFallbackOnHostPage,
                                  out int statusCode, out string _,
                                  out Stream content,
                                  out IDictionary<string, string> headers))
        {
            UrlRequestJob urlRequestJob = p.Network.CreateUrlRequestJob(p.UrlRequest,
             new UrlRequestJobOptions
             {
                 HttpStatusCode = (HttpStatusCode)statusCode,
                 Headers = headers
                          .Select(pair => new HttpHeader(pair.Key, pair.Value))
                          .ToList()
             });
            Task.Run(() =>
            {
                using (MemoryStream memoryStream = new())
                {
                    content.CopyTo(memoryStream);
                    urlRequestJob.Write(memoryStream.ToArray());
                }

                urlRequestJob.Complete();
            });
            return InterceptRequestResponse.Intercept(urlRequestJob);
        }

        return InterceptRequestResponse.Proceed();
    }
}
```

### Navigation

Now, when the web view can navigate to the app pages and load static resources,
we can load the index page and teach `WebViewManager` to perform the navigation.

**BlazorBrowserView.axaml.cs**
```cs {hl_lines=[20]}
public partial class BlazorBrowserView : UserControl
{
    private IEngine engine;
    private IBrowser browser;
    private BrowserManager browserManager;
    ...

    public async Task Initialize()
    {
        ...
        engine = await EngineFactory.CreateAsync(engineOptions);
        browser = engine.CreateBrowser();
        browserManager = new BrowserManager(browser, ...);
        
        foreach (RootComponent rootComponent in RootComponents)
        {
            await rootComponent.AddToWebViewManagerAsync(browserManager);
        }
        
        browserManager.Navigate("/");
        ...
    }
    ...
}
```

**BrowserManager.cs**
```cs {hl_lines=["7-10"]}
internal class BrowserManager : WebViewManager
{
    ...
    private IBrowser Browser { get; }
    ...

    protected override void NavigateCore(Uri absoluteUri)
    {
        Browser.Navigation.LoadUrl(absoluteUri.AbsoluteUri);
    }
}
```

### Exchanging data

Unlike regular web apps, Blazor Hybrid doesn't use HTTP for exchanging data. The
front end and the back end communicate with string messages using a special
.NET-JavaScript interop. In JavaScript, the messages are sent and received via
the `window.external` object, and on the .NET side, via `WebViewManager`.

We use DotNetBrowser .NET-JavaScript bridge to create the `window.external` 
object and transfer the messages.

**BrowserManager.cs**
```cs {hl_lines=[5,"16-18"]}
internal class BrowserManager : WebViewManager
{
    ...
    private IBrowser Browser { get; }
    private IJsFunction sendMessageToFrontEnd;

    public BrowserManager(IBrowser browser, IServiceProvider provider,
                          Dispatcher dispatcher,
                          IFileProvider fileProvider,
                          JSComponentConfigurationStore jsComponents,
                          string hostPageRelativePath)
        : base(provider, dispatcher, AppOriginUri, fileProvider, jsComponents,
               hostPageRelativePath)
    {
        Browser = browser;
        // This handler is called after the page is loaded
        // but before it executes its own JavaScript.
        Browser.InjectJsHandler = new Handler<InjectJsParameters>(OnInjectJs);
    }
    
    ...

    private void OnInjectJs(InjectJsParameters p)
    {
        if (!p.Frame.IsMain)
        {
            return;
        }

        dynamic window = p.Frame.ExecuteJavaScript("window").Result;
        window.external = p.Frame.ParseJsonString("{}");

        // When the page will call these methods, DotNetBrowser will
        // proxy calls to the .NET methods.
        window.external.sendMessage = (Action<dynamic>)OnMessageReceived;
        window.external.receiveMessage = (Action<dynamic>)SetupCallback;
    }

    private void OnMessageReceived(dynamic obj)
    {
        this.MessageReceived(new Uri(Browser.Url), obj.ToString());
    }
    
    private void SetupCallback(dynamic callbackFunction)
    {
        sendMessageToFrontEnd = callbackFunction as IJsFunction;
    }
    
    protected override void SendMessage(string message)
    {
        sendMessageToFrontEnd?.Invoke(null, message);
    }
}
```

## Conclusion

In this article, we discussed Blazor Hybrid, a .NET technology for building
desktop apps with Blazor.

Blazor Hybrid uses .NET MAUI, which comes with two limitations:

 * Does not support Linux.
 * Uses different browser engines on Windows and macOS, where the same app can
behave and look differently.

We suggested using Avalonia UI + DotNetBrowser instead. This combination
provides the full support of Windows, macOS, and Linux, and ensures a consistent
browser environment across all platforms. 
