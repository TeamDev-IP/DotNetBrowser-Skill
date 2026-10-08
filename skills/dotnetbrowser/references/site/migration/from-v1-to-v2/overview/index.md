
# Migrating from 1.x to 2.0

**Lead**
DotNetBrowser version 2.0 brings major improvements to both internal features and public API of the library. This guide shows how to make your application code written with DotNetBrowser version 1.x compatible with version 2.0.


## Overview

### Why migrate?

We recommend you to update your code to the latest version because all the new features, Chromium upgrades, support of new operating systems and .NET Framework versions, bug fixes, security patches, performance, and memory usage enhancements are applied on top of the latest version.

### How long does it take?

From our experience, upgrade to a new major version may take from a couple of hours to a few days depending on the number of the features you use in your application. As usual, we strongly recommend to test your software after the upgrade in all the environments it supports.

### Getting help

Please check out the [FAQ](#faq) section at the end of this guide. Maybe the answer to your question is already there.

In case you did not find the answer in this guide and you need assistance with migration, please [contact us](https://dotnetbrowser.support.teamdev.com/support/tickets/new). We will be happy to help.

## Key changes

### API & architecture

In DotNetBrowser version 2.0, the [architecture](https://teamdev.com/dotnetbrowser/docs/guides/architecture/) of the library has been improved. Now DotNetBrowser allows you to create two absolutely independent `IBrowser` instances and control their life cycle. Along with this internal architecture change, public API has been improved and extended with [new features](https://teamdev.com/dotnetbrowser/releases/2020/v2/).

Refer to the [Mapping](https://teamdev.com/dotnetbrowser/migration/from-v1-to-v2/overview/#mapping) section to find out how the main functionality of version 1.x maps to version 2.0.

### System requirements

Starting with this version, DotNetBrowser no longer supports .NET Framework 4.0. Current system requirements are available [here](https://teamdev.com/dotnetbrowser/docs/guides/requirements/).

### Assemblies

The structure of the library has changed. Now the library consists of the following assemblies:
* `DotNetBrowser.dll` &mdash; data classes and interfaces;
* `DotNetBrowser.Core.dll` &mdash; core implementation;
* `DotNetBrowser.Logging.dll` &mdash; DotNetBrowser Logging API implementation;
* `DotNetBrowser.WinForms.dll` &mdash; classes and interfaces for embedding into a WinForms application;
* `DotNetBrowser.Wpf.dll` &mdash; classes and interfaces for embedding into a WPF app;
* `DotNetBrowser.Chromium.Win-x86.dll` &mdash; Chromium 32-bit binaries for Windows;
* `DotNetBrowser.Chromium.Win-x64.dll` &mdash;  Chromium 64-bit binaries for Windows.

### Basic concepts

The way to create and dispose various objects has changed in the new API. 

To create an `IEngine` object use the `EngineFactory.Create()` static method:


**C#**
```csharp
IEngine engine = EngineFactory.Create(options);
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(options)
```



To create an immutable data object use the `<Object>.Builder.Build()` method:


**C#**
```csharp
EngineOptions engineOptions = new EngineOptions.Builder()
{
    Language = Language.EnglishUs
}.Build();
```

**VB**
```vb
Dim engineOptions As EngineOptions = New EngineOptions.Builder() With {
    .Language = Language.EnglishUs
}.Build()
```



Every object that should be disposed manually implements the `IDisposable` interface, for example, `IBrowser`. To dispose the object, call the `IDisposable.Dispose()` method:


**C#**
```csharp
browser.Dispose();
```

**VB**
```vb
browser.Dispose()
```



**Note**
Some service objects depend on the other service objects. When you dispose a service object, all the service objects depending on it will be disposed automatically, so you do not need to dispose them manually. Refer to [Architecture](https://teamdev.com/dotnetbrowser/docs/guides/architecture/) guide for more details about the key objects and their interaction principles.


### Handlers

Handlers are used to process various callbacks from the Chromium engine and modify its behavior. 

**v1.x**

In DotNetBrowser version 1.x, handlers are usually implemented as the properties of interface types, such as `PrintHandler`, `PermissionHandler`, `LoadHandler`, and others.

**v2.0**

In DotNetBrowser version 2.0, all the handlers are implemented as the properties of type `IHandler<in T>` or `IHandler<in T, out TResult>`, where `T` is the parameters type, `TResult` is the result type. The result returned from the handler will be used to notify the Chromium engine and affect its behavior.

To register and unregister a handler, use corresponding property setters and getters.

There are default implementations of the `IHandler<in T, out TResult>` interface:
 - `Handler<T, TResult>` class allows wrapping lambdas and method groups;
 - `AsyncHandler<T, TResult>` class allows wrapping async lambdas and method groups, or lambdas and method groups that return `Task<TResult>`.

**Important**
In some cases, engine appears blocked until the handler returns the result. In case of using the `AsyncHandler`, engine appears blocked until the result is available in the returned task.


### Thread safety

The library is not thread-safe, so please avoid working with the library from different threads at the same time.

### Licensing

In DotNetBrowser version 2.0 the license format and the way how the library checks the license has been improved.

**v1.x**

In previous version, the license represented a `teamdev.licenses` text file. This text file contained the plain text of the license. To set up the license, you had to include this text file in your project as an `EmbeddedResource` or copy it to the working directory of the .NET application.

Project license was tied to a fully qualified type name (for example, `Company.Product.MyClass`). It could be any class of your application. The only requirement was that this class must be included in the classpath of your .NET app where you used DotNetBrowser.

**v2.0**

Now, the library requires a license key that represents a string with combination of letters and digits. You can [add the license to your project](https://teamdev.com/dotnetbrowser/docs/guides/installation/license/#installing-key-through-the-api) through the API.

It is also possible to put this string to a text file named `dotnetbrowser.license` and include this text file in your project as an `EmbeddedResource` or copy it to the working directory of the .NET application.

The Project license is tied to a namespace now. The namespace is expected to be in the `Company.Product.Namespace` format. It should be a top-level namespace for the classes where you create an `IEngine` instance.

**Note**
For example, if the Project license is tied to the `Company.Product` namespace, then you can create `IEngine` instances only in the classes located in this namespace or its inner namespaces, e. g. `Company.Product.Namespace`.
 

The `IEngine` was [introduced](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/) in DotNetBrowser 2. We recommend that you check out the [guide](https://teamdev.com/dotnetbrowser/docs/guides/architecture/) that describes the new architecture, how to create an `IEngine` and manage multiple `IBrowser`s lifecycle.

You can work with the created `IEngine` instance and make calls to the library’s API from the classes located in other namespaces without any restrictions.

### Dropped functionality

Starting with this version DotNetBrowser no longer supports .NET Framework 4.

In the new version, the following functionality has been temporarily dropped:

* `Notifications` API;
* `PasswordManager` API;
* Printing API (restored in [DotNetBrowser 2.4](https://teamdev.com/dotnetbrowser/releases/2021/v2-4/#printing-api));
* HTML5 Application Cache API;
* Displaying the `BeforeUnload` dialog when disposing `IBrowser`(restored in [DotNetBrowser 2.5](https://teamdev.com/dotnetbrowser/releases/2021/v2-5/));
* Drag&amp;Drop `IDataObject` API (restored in [DotNetBrowser 2.3](https://teamdev.com/dotnetbrowser/releases/2020/v2-3/#drag-and-drop-events-interception-and-idataobject-support));
* Intercepting Drag&amp;Drop events (restored in [DotNetBrowser 2.3](https://teamdev.com/dotnetbrowser/releases/2020/v2-3/#drag-and-drop-events-interception-and-idataobject-support));
* Intercepting and suppressing touch and gesture events (touch events interception restored in [DotNetBrowser 2.11](https://teamdev.com/dotnetbrowser/releases/2022/v2-11/#intercepting-touch-events)).

We are going to provide the alternatives of the above-mentioned features in the next versions.

## Mapping

In this section, we describe how the main functionality of DotNetBrowser version 1.x maps to version 2.0.

### Engine

#### Creating Engine

**1.x**

The `IEngine` is not a part of the public API. It is created internally when the first `Browser` instance is created in the application. Only one `IEngine` can be created and used in the application.

**2.0**

The `IEngine` is a part of the public API now. You can create and use multiple `Engine` instances in the application. To create an `Engine` instance with the required options, use the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    // The language used on the default error pages and GUI.
    Language = Language.EnglishUs,
    // The absolute path to the directory where the data 
    // such as cache, cookies, history, GPU cache, local 
    // storage, visited links, web data, spell checking 
    // dictionary files, etc. is stored.
    UserDataDirectory = @"C:\Users\Me\DotNetBrowser"
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With {
    ' The language used on the default error pages and GUI.
    .Language = Language.EnglishUs,
    ' The absolute path to the directory where the data 
    ' such as cache, cookies, history, GPU cache, local 
    ' storage, visited links, web data, spell checking 
    ' dictionary files, etc. is stored.
    .UserDataDirectory = "C:\Users\Me\DotNetBrowser"
}.Build())
```



Each `IEngine` instance runs a separate native process where Chromium with the provided options is created and initialized. The native process communicates with the .NET process using the Inter-Process Communication (IPC) bridge. If the native process is unexpectedly terminated because of a crash, the .NET process will continue running.

You can use the following notification to find out when the `IEngine` is unexpectedly terminated, so that you can re-create the Engine and restore the `IBrowser` instances:


**C#**
```csharp
engine.Disposed += (s, e) => 
{
    long exitCode = e.ExitCode;
    if(exitCode != 0)
    {
        // Clear all the allocated resources and re-create the Engine.
    }
};
```

**VB**
```vb
AddHandler engine.Disposed, Sub(s, e)
    Dim exitCode As Long = e.ExitCode
    If exitCode <> 0 Then
        ' Clear all the allocated resources and re-create the Engine.
    End If
End Sub
```



#### Closing Engine

**1.x**

The `IEngine` is disposed automatically when the last `Browser` instance is disposed in the application.

**2.0**

The `IEngine` should be disposed manually using the `Dispose()` method when it is no longer required:


**C#**
```csharp
engine.Dispose();
```

**VB**
```vb
engine.Dispose()
```



When the `IEngine` is disposed, all its `IBrowser` instances are disposed automatically. Any attempt to use an already disposed `IEngine` leads to an exception.

To find out when the `IEngine` is disposed, use the following event:


**C#**
```csharp
engine.Disposed += (s, e) => {};
```

**VB**
```vb
AddHandler engine.Disposed, Sub(s, e)
End Sub
```



### Browser

#### Creating a browser

**1.x**


**C#**
```csharp
Browser browser = BrowserFactory.Create();
```

**VB**
```vb
Dim browser As Browser = BrowserFactory.Create()
```



**2.0**


**C#**
```csharp
IBrowser browser = engine.CreateBrowser();
```

**VB**
```vb
Dim browser As IBrowser = engine.CreateBrowser()
```



#### Creating a browser with options

**1.x**


**C#**
```csharp
BrowserContextParams parameters = new BrowserContextParams(@"C:\Users\Me\DotNetBrowser") 
{ 
    StorageType = StorageType.MEMORY 
};
BrowserContext context = new BrowserContext(parameters);
Browser browser = BrowserFactory.Create(context, BrowserType.LIGHTWEIGHT);
```

**VB**
```vb
Dim parameters As BrowserContextParams = 
    New BrowserContextParams("C:\Users\Me\DotNetBrowser") With {
        .StorageType = StorageType.MEMORY
    }
Dim context As BrowserContext = New BrowserContext(parameters)
Dim browser As Browser = BrowserFactory.Create(context, BrowserType.LIGHTWEIGHT)
```



**2.0**

The `BrowserContext` functionality has been moved to `IEngine`. Thus, the same code should be replaced with the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    IncognitoEnabled = true,
    RenderingMode = RenderingMode.OffScreen,
    UserDataDirectory = @"C:\Users\Me\DotNetBrowser"
}.Build());
IBrowser browser = engine.CreateBrowser();
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With {
    .IncognitoEnabled = True,
    .RenderingMode = RenderingMode.OffScreen,
    .UserDataDirectory = "C:\Users\Me\DotNetBrowser"
}.Build())
Dim browser As IBrowser = engine.CreateBrowser()
```



#### Disposing a browser

**1.x**


**C#**
```csharp
browser.Dispose();
```

**VB**
```vb
browser.Dispose()
```



**2.0**


**C#**
```csharp
browser.Dispose();
```

**VB**
```vb
browser.Dispose()
```



#### Responsive/Unresponsive

**1.x**


**C#**
```csharp
browser.RenderResponsiveEvent += (s, e ) => {};
browser.RenderUnresponsiveEvent += (s, e) => {};
```

**VB**
```vb
AddHandler browser.RenderResponsiveEvent, Sub(s, e)
End Sub
AddHandler browser.RenderUnresponsiveEvent, Sub(s, e)
End Sub
```



**2.0**


**C#**
```csharp
browser.BrowserBecameResponsive += (s, e ) => {};
browser.BrowserBecameUnresponsive += (s, e) => {};
```

**VB**
```vb
AddHandler browser.BrowserBecameResponsive, Sub(s, e)
End Sub
AddHandler browser.BrowserBecameUnresponsive, Sub(s, e)
End Sub
```



### BrowserView

In DotNetBrowser version 1.x, creating a `BrowserView` with its default constructor leads to initializing a bound `Browser` instance in the same thread. As a result, the main UI thread may appear blocked until the `Browser` instance is created and initialized, and this may take a significant amount of time.

In DotNetBrowser version 2.0, creating an `IBrowserView` implementation with its default constructor creates a UI control that is not initially bound to any browser.
The connection with a specific `IBrowser` instance is established when it is necessary by calling `InitializeFrom(IBrowser)` extension method.

**Important**
The `IBrowserView` implementations do not dispose the connected `IBrowser` or `IEngine` instances when the application is closed. As a result, the browser and engine will appear alive even after all the application windows are closed and prevent the application from terminating. To handle this case, dispose `IBrowser` or `IEngine` instances during your application shutdown.


#### Creating WinForms BrowserView

**1.x**


**C#**
```csharp
using DotNetBrowser.WinForms;
// ...
BrowserView view = new WinFormsBrowserView();
```

**VB**
```vb
Imports DotNetBrowser.WinForms
' ...
Dim view As BrowserView = New WinFormsBrowserView()
```



**2.0**


**C#**
```csharp
using DotNetBrowser.WinForms;
// ...
BrowserView view = new BrowserView();
view.InitializeFrom(browser);
```

**VB**
```vb
Imports DotNetBrowser.WinForms
' ...
Dim view As BrowserView = New BrowserView()
view.InitializeFrom(browser)
```



#### Creating WPF BrowserView

**1.x**


**C#**
```csharp
using DotNetBrowser.WPF;
// ...
BrowserView view = new WPFBrowserView(browser);
```

**VB**
```vb
Imports DotNetBrowser.WPF
' ...
Dim view As BrowserView = New WPFBrowserView()
```



**2.0**


**C#**
```csharp
using DotNetBrowser.Wpf;
// ...
BrowserView view = new BrowserView();
view.InitializeFrom(browser);
```

**VB**
```vb
Imports DotNetBrowser.Wpf
' ...
Dim view As BrowserView = New BrowserView()
view.InitializeFrom(browser)
```



### Frame

#### Working with frame

**1.x**

A web page may consist of the main frame including multiple sub-frames. To perform an operation with a frame, pass the frame’s identifier to the corresponding method:


**C#**
```csharp
// Get HTML of the main frame.
browser.GetHTML();

// Get HTML of the all frames.
foreach (long frameId in browser.GetFramesIds()) {
    string html = browser.GetHTML(frameId);
}
```

**VB**
```vb
' Get HTML of the main frame.
browser.GetHTML()

' Get HTML of the all frames.
For Each frameId As Long In browser.GetFramesIds()
    Dim html As String = browser.GetHTML(frameId)
Next
```



**2.0**

The `IFrame` is a part of the public API now. You can work with the frame through the `IFrame` instance:


**C#**
```csharp
// Get HTML of the main frame if it exists.
string html = browser.MainFrame?.Html;

// Get HTML of all the frames.
foreach (IFrame frame in browser.AllFrames) 
{
    string html = frame.Html;
}
```

**VB**
```vb
' Get HTML of the main frame if it exists.
Dim html As String = browser.MainFrame?.Html

' Get HTML of all the frames.
For Each frame As IFrame In browser.AllFrames
    Dim html As String = frame.Html
Next
```



### Navigation

#### Loading URL

**1.x**


**C#**
```csharp
browser.LoadURL("https://www.google.com");
```

**VB**
```vb
browser.LoadURL("https://www.google.com")
```



**2.0**


**C#**
```csharp
browser.Navigation.LoadUrl("https://www.google.com");
```

**VB**
```vb
browser.Navigation.LoadUrl("https://www.google.com")
```



#### Loading HTML

**1.x**


**C#**
```csharp
browser.LoadHTML("<html><body></body></html>");
```

**VB**
```vb
browser.LoadHTML("<html><body></body></html>")
```



**2.0**


**C#**
```csharp
browser.MainFrame?.LoadHtml("<html><body></body></html>"));
```

**VB**
```vb
browser.MainFrame?.LoadHtml("<html><body></body></html>"))
```



### Navigation events

#### Start loading

**1.x**


**C#**
```csharp
browser.StartLoadingFrameEvent += (s, e) =>
{
    string url = e.ValidatedURL;
};
```

**VB**
```vb
AddHandler browser.StartLoadingFrameEvent, Sub(s, e)
    Dim url As String = e.ValidatedURL
End Sub
```



**2.0**


**C#**
```csharp
browser.Navigation.NavigationStarted += (s, e) => 
{
    string url = e.Url;
};
```

**VB**
```vb
AddHandler browser.Navigation.NavigationStarted, Sub(s, e)
    Dim url As String = e.Url
End Sub
```



#### Finish loading

**1.x**


**C#**
```csharp
browser.FinishLoadingFrameEvent+= (s, e) =>
{
    string html = browser.GetHTML(e.FrameId);
};
```

**VB**
```vb
AddHandler browser.FinishLoadingFrameEvent, Sub(s, e)
    Dim html As String = browser.GetHTML(e.FrameId)
End Sub
```



**2.0**


**C#**
```csharp
browser.Navigation.FrameLoadFinished += (s, e) =>
{
    string html = e.Frame.Html;
};
```

**VB**
```vb
AddHandler browser.Navigation.FrameLoadFinished, Sub(s, e)
    Dim html As String = e.Frame.Html
End Sub
```



#### Fail loading

**1.x**


**C#**
```csharp
browser.FailLoadingFrameEvent  += (s, e) => 
{
    NetError errorCode = e.ErrorCode;
};
```

**VB**
```vb
AddHandler browser.FailLoadingFrameEvent, Sub(s, e)
    Dim errorCode As NetError = e.ErrorCode
End Sub
```



**2.0**


**C#**
```csharp
browser.Navigation.FrameLoadFailed += (s, e) => 
{
    NetError error = e.ErrorCode;
};
```

**VB**
```vb
AddHandler browser.Navigation.FrameLoadFailed, Sub(s, e)
    Dim errorCode As NetError = e.ErrorCode
End Sub
```



or


**C#**
```csharp
browser.Navigation.NavigationFinished += (s, e) => 
{
    NetError error = e.ErrorCode;
};
```

**VB**
```vb
AddHandler browser.Navigation.NavigationFinished, Sub(s, e)
    Dim errorCode As NetError = e.ErrorCode
End Sub
```



### Network

#### Configuring User-Agent

**1.x**


**C#**
```csharp
BrowserPreferences.SetUserAgent("My User-Agent");
```

**VB**
```vb
BrowserPreferences.SetUserAgent("My User-Agent")
```



**2.0**


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    UserAgent = "My User-Agent"
}
.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With {
    .UserAgent = "My User-Agent"
}.Build())
```



#### Configuring Accept-Language

**1.x**


**C#**
```csharp
browserContext.AcceptLanguage = "fr, en-gb;q=0.8, en;q=0.7";
```

**VB**
```vb
browserContext.AcceptLanguage = "fr, en-gb;q=0.8, en;q=0.7"
```



**2.0**


**C#**
```csharp
engine.Network.AcceptLanguage = "fr, en-gb;q=0.8, en;q=0.7";
```

**VB**
```vb
engine.Network.AcceptLanguage = "fr, en-gb;q=0.8, en;q=0.7"
```



#### Configuring proxy

**1.x**


**C#**
```csharp
ProxyConfig proxyConfig = browserContext.ProxyConfig;
browserContext.ProxyConfig = new CustomProxyConfig("http-proxy-server:80");
```

**VB**
```vb
Dim proxyConfig As ProxyConfig = browserContext.ProxyConfig
browserContext.ProxyConfig = New CustomProxyConfig("http-proxy-server:80")
```



**2.0**


**C#**
```csharp
engine.Proxy.Settings = new CustomProxySettings("http-proxy-server:80");
```

**VB**
```vb
engine.Proxy.Settings = New CustomProxySettings("http-proxy-server:80")
```



#### Redirecting URL request

**1.x**


**C#**
```csharp
class MyNetworkDelegate : DefaultNetworkDelegate
{
    public override void OnBeforeURLRequest(BeforeURLRequestParams parameters)
    {
        parameters.SetURL("https://www.google.com");
    }
}
// ...
browserContext.NetworkService.NetworkDelegate = new MyNetworkDelegate();
```

**VB**
```vb
Class MyNetworkDelegate
    Inherits DefaultNetworkDelegate

    Public Overrides Sub OnBeforeURLRequest(ByVal parameters As BeforeURLRequestParams)
        parameters.SetURL("https://www.google.com")
    End Sub
End Class
' ...
browserContext.NetworkService.NetworkDelegate = New MyNetworkDelegate()
```



**2.0**


**C#**
```csharp
engine.Network.SendUrlRequestHandler =
    new Handler<SendUrlRequestParameters, SendUrlRequestResponse>((e) =>
    {
        return SendUrlRequestResponse.Override("https://www.google.com");
    });
```

**VB**
```vb
engine.Network.SendUrlRequestHandler =
        New Handler(Of SendUrlRequestParameters, SendUrlRequestResponse)(
            Function(e) SendUrlRequestResponse.Override("https://www.google.com"))
```



#### Overriding HTTP headers

**1.x**


**C#**
```csharp
class MyNetworkDelegate : DefaultNetworkDelegate
{
    public override void OnBeforeSendHeaders(BeforeSendHeadersParams parameters)
    {
        HttpHeadersEx headers = params.HeadersEx;
        headers.SetHeader("User-Agent", "MyUserAgent");
        headers.SetHeader("Content-Type", "text/html");
    }
}
// ...
browserContext.NetworkService.NetworkDelegate = new MyNetworkDelegate();
```

**VB**
```vb
Class MyNetworkDelegate
    Inherits DefaultNetworkDelegate

    Public Overrides Sub OnBeforeSendHeaders(parameters As BeforeSendHeadersParams)
        Dim headers As HttpHeadersEx = params.HeadersEx
        headers.SetHeader("User-Agent", "MyUserAgent")
        headers.SetHeader("Content-Type", "text/html")
    End Sub
End Class
' ...
browserContext.NetworkService.NetworkDelegate = New MyNetworkDelegate()
```



**2.0**


**C#**
```csharp
engine.Network.SendHeadersHandler =
    new Handler<SendHeadersParameters, SendHeadersResponse>((e) =>
    {
        return SendHeadersResponse.OverrideHeaders(new[] {
            new HttpHeader("User-Agent", "MyUserAgent"),
            new HttpHeader("Content-Type", "text/html")
        });
    });
```

**VB**
```vb
engine.Network.SendHeadersHandler =
    New Handler(Of SendHeadersParameters, SendHeadersResponse)(
        Function(e) SendHeadersResponse.OverrideHeaders(
            {New HttpHeader("User-Agent", "MyUserAgent"),
             New HttpHeader("Content-Type", "text/html")}))
```



#### Intercepting URL requests

**1.x**


**C#**
```csharp
class MyProtocolHandler : IProtocolHandler
{
    public IUrlResponse Handle(IUrlRequest request)
    {
        string html = "<html><body><p>Hello there!</p></body></html>";
        IUrlResponse response = new UrlResponse(Encoding.UTF8.GetBytes(html));
        response.Headers.SetHeader("Content-Type", "text/html");
        return response;
    }
}
// ...
browser.Context.ProtocolService.Register("https", new MyProtocolHandler());
```

**VB**
```vb
Class MyProtocolHandler
    Inherits IProtocolHandler

    Public Function Handle(ByVal request As IUrlRequest) As IUrlResponse
        Dim html As String = "<html><body><p>Hello there!</p></body></html>"
        Dim response As IUrlResponse = New UrlResponse(Encoding.UTF8.GetBytes(html))
        response.Headers.SetHeader("Content-Type", "text/html")
        Return response
    End Function
End Class
' ...
browser.Context.ProtocolService.Register("https", New MyProtocolHandler())
```



**2.0**


**C#**
```csharp
network.InterceptRequestHandler =
    new Handler<InterceptRequestParameters, InterceptRequestResponse>(p =>
    {
        if (!p.UrlRequest.Url.StartsWith("https"))
        {
            return InterceptRequestResponse.Proceed();
        }

        UrlRequestJobOptions options = new UrlRequestJobOptions
        {
            Headers = new List<HttpHeader>
            {
                new HttpHeader("Content-Type", "text/plain"),
                new HttpHeader("Content-Type", "charset=utf-8")
            }
        };
        UrlRequestJob job = network.CreateUrlRequestJob(p.UrlRequest, options);

        Task.Run(() =>
        {
            // The request processing is performed in a background thread
            // in order to avoid freezing the web page.
            string html = "<html><body><p>Hello there!</p></body></html>";
            job.Write(Encoding.UTF8.GetBytes(html));
            job.Complete();
        });
        
        return InterceptRequestResponse.Intercept(job);
    });
```

**VB**
```vb
network.InterceptRequestHandler =
    New Handler(Of InterceptRequestParameters, InterceptRequestResponse)(Function(p)
        If Not p.UrlRequest.Url.StartsWith("https") Then
            Return InterceptRequestResponse.Proceed()
        End If

        Dim options = New UrlRequestJobOptions With {
                .Headers = New List(Of HttpHeader) From {
                New HttpHeader("Content-Type", "text/plain"),
                New HttpHeader("Content-Type", "charset=utf-8")
                }
                }
        Dim job As UrlRequestJob = network.CreateUrlRequestJob(p.UrlRequest, options)
        Task.Run(Sub()
            ' The request processing is performed in a background thread
            ' in order to avoid freezing the web page.
            Dim html = "<html><body><p>Hello there!</p></body></html>"
            job.Write(Encoding.UTF8.GetBytes(html))
            job.Complete()
        End Sub)
        Return InterceptRequestResponse.Intercept(job)
    End Function)
```



### Authentication

#### Proxy, Basic, Digest, NTLM

**1.x**


**C#**
```csharp
class MyNetworkDelegate : DefaultNetworkDelegate
{
    public override bool OnAuthRequired(AuthRequiredParams params)
    {
        if(params.IsProxy)
        {
            params.Username = "user";
            params.Password = "password";
            return false;
        }
        // Cancel authentication request.
        return true;
    }
}
// ...
browserContext.NetworkService.NetworkDelegate = new MyNetworkDelegate();
```

**VB**
```vb
Class MyNetworkDelegate
    Inherits DefaultNetworkDelegate

    Public Overrides Function OnAuthRequired(ByVal params As AuthRequiredParams) As Boolean
        If params.IsProxy Then
            params.Username = "user"
            params.Password = "password"
            Return False
        End If
        ' Cancel authentication request.
        Return True
    End Function
End Class
' ...
browserContext.NetworkService.NetworkDelegate = New MyNetworkDelegate()
```



**2.0**


**C#**
```csharp
engine.Network.AuthenticateHandler =
    new Handler<AuthenticateParameters, AuthenticateResponse>((p) =>
    {
        if (p.IsProxy)
        {
            return AuthenticateResponse.Continue("user", "password");
        }
        else
        {
            return AuthenticateResponse.Cancel();
        }
    });
```

**VB**
```vb
engine.Network.AuthenticateHandler =
    New Handler(Of AuthenticateParameters, AuthenticateResponse)(Function(p)
        If p.IsProxy Then
            Return AuthenticateResponse.Continue("user", "password")
        Else
            Return AuthenticateResponse.Cancel()
        End If
    End Function)
```



#### HTTPS client certificate

**1.x**


**C#**
```csharp
class MyDialogHandler : DialogHandler
{
    public CloseStatus OnSelectCertificate(CertificatesDialogParams parameters)
    {
        List<Certificate> certificates = parameters.Certificates;
        if (certificates.Count == 0) {
            return CloseStatus.CANCEL;
        } else {
            parameters.SelectedCertificate = certificates.LastOrDefault();
            return CloseStatus.OK;
        }
    }

    // ...
}
// ...
browser.DialogHandler = new MyDialogHandler();
```

**VB**
```vb
Class MyDialogHandler
    Inherits DialogHandler

    Public Function OnSelectCertificate(parameters As CertificatesDialogParams) As CloseStatus
        Dim certificates As List(Of Certificate) = parameters.Certificates

        If certificates.Count Is 0 Then
            Return CloseStatus.CANCEL
        Else
            parameters.SelectedCertificate = certificates.LastOrDefault()
            Return CloseStatus.OK
        End If
    End Function
    ' ...
End Class
' ...
browser.DialogHandler = New MyDialogHandler()
```



**2.0**


**C#**
```csharp
browser.SelectCertificateHandler
    = new Handler<SelectCertificateParameters, SelectCertificateResponse>(p =>
    {
        int count = p.Certificates.Count();
        return count == 0 ?
            SelectCertificateResponse.Cancel() :
            SelectCertificateResponse.Select(p.Certificates.Count() - 1);
    });
```

**VB**
```vb
browser.SelectCertificateHandler =
    New Handler(Of SelectCertificateParameters, SelectCertificateResponse)(Function(p)
        Dim count As Integer = p.Certificates.Count()
        Return If (count = 0,
                   SelectCertificateResponse.Cancel(),
                   SelectCertificateResponse.Select(p.Certificates.Count() - 1))
    End Function)
```



### Plugins

#### Filtering plugins

**1.x**


**C#**
```csharp
class MyPluginFilter : PluginFilter
{
    public bool IsPluginAllowed(PluginInfo pluginInfo)
    {
        return true;
    }
}
// ...
browser.PluginManager.PluginFilter = new MyPluginFilter();
```

**VB**
```vb
Class MyPluginFilter
    Inherits PluginFilter

    Public Function IsPluginAllowed(ByVal pluginInfo As PluginInfo) As Boolean
        Return True
    End Function
End Class
' ...
browser.PluginManager.PluginFilter = New MyPluginFilter()
```



**2.0**


**C#**
```csharp
engine.Plugins.AllowPluginHandler = 
    new Handler<AllowPluginParameters, AllowPluginResponse>(p =>
    {
        return AllowPluginResponse.Allow();
    });
```

**VB**
```vb
engine.Plugins.AllowPluginHandler =
    New Handler(Of AllowPluginParameters, AllowPluginResponse)(
        Function(p) AllowPluginResponse.Allow())
```



### DOM

#### Accessing a document

**1.x**


**C#**
```csharp
DOMDocument document = browser.GetDocument();
```

**VB**
```vb
Dim document As DOMDocument = browser.GetDocument()
```



**2.0**


**C#**
```csharp
IDocument document = browser.MainFrame?.Document;
```

**VB**
```vb
Dim document As IDocument = browser.MainFrame?.Document
```



### DOM events

#### Working with events

**1.x**


**C#**
```csharp
element.AddEventListener(DOMEventType.OnClick, (s, e) =>
{
    DOMEventTarget eventTarget = e.Target;
    if (eventTarget != null) {
        // ...
    }
}, false);
```

**VB**
```vb
element.AddEventListener(DOMEventType.OnClick, Sub(s, e)
    Dim eventTarget As DOMEventTarget = e.Target

    If eventTarget IsNot Nothing Then
        ' ...
    End If
End Sub, False)
```



**2.0**


**C#**
```csharp
element.Events.Click += (s, e) =>
{
    IEventTarget eventTarget = e.Event.Target;
    if (eventTarget != null)
    {
        // ...
    }
};
```

**VB**
```vb
AddHandler element.Events.Click, Sub(s, e)
    Dim eventTarget As IEventTarget = e.Event.Target

    If eventTarget IsNot Nothing Then
        ' ...
    End If
End Sub
```



### JavaScript

#### Calling JavaScript from .NET

**1.x**


**C#**
```csharp
string name = browser.ExecuteJavaScriptAndReturnValue("'Hello'")
        .AsString().Value;
double number = browser.ExecuteJavaScriptAndReturnValue("123")
        .AsNumber().Value;
bool flag = browser.ExecuteJavaScriptAndReturnValue("true")
        .AsBoolean().Value;
JSObject window = browser.ExecuteJavaScriptAndReturnValue("window")
        .AsObject();
```

**VB**
```vb
Dim name As String = browser.ExecuteJavaScriptAndReturnValue("'Hello'") _
        .AsString().Value
Dim number As Double = browser.ExecuteJavaScriptAndReturnValue("123") _
        .AsNumber().Value
Dim flag As Boolean = browser.ExecuteJavaScriptAndReturnValue("true") _
        .AsBoolean().Value
Dim window As JSObject = browser.ExecuteJavaScriptAndReturnValue("window") _
        .AsObject()
```



**2.0**

The `JSValue` class has been removed in DotNetBrowser 2.0. The type conversion is done automatically now. You can execute JavaScript both synchronously blocking the current thread execution or asynchronously:


**C#**
```csharp
IFrame mainFrame = browser.MainFrame;
if(mainFrame != null)
{
    // Execution with await.
    string name = await mainFrame.ExecuteJavaScript<string>("'Hello'");
    double number = await mainFrame.ExecuteJavaScript<double>("123");
    bool flag = await mainFrame.ExecuteJavaScript<bool>("true");
    IJsObject window = await mainFrame.ExecuteJavaScript<IJsObject>("window");

    // Synchronous execution that blocks the current thread.
    name = mainFrame.ExecuteJavaScript<string>("'Hello'").Result;
    number = mainFrame.ExecuteJavaScript<double>("123").Result;
    flag = mainFrame.ExecuteJavaScript<bool>("true").Result;
    window = mainFrame.ExecuteJavaScript<IJsObject>("window").Result;

    // Asynchronous execution with continuation.
    mainFrame.ExecuteJavaScript<IDocument>("document").ContinueWith(t =>{
        string baseUri = t.Result.BaseUri;
    });
}
```

**VB**
```vb
Dim mainFrame As IFrame = browser.MainFrame

If mainFrame IsNot Nothing Then
    ' Execution with await.
    Dim name As String = Await mainFrame.ExecuteJavaScript (Of String)("'Hello'")
    Dim number As Double = Await mainFrame.ExecuteJavaScript (Of Double)("123")
    Dim flag As Boolean = Await mainFrame.ExecuteJavaScript (Of Boolean)("true")
    Dim window As IJsObject = Await mainFrame.ExecuteJavaScript (Of IJsObject)("window")

    ' Synchronous execution that blocks the current thread.
    name = mainFrame.ExecuteJavaScript (Of String)("'Hello'").Result
    number = mainFrame.ExecuteJavaScript (Of Double)("123").Result
    flag = mainFrame.ExecuteJavaScript (Of Boolean)("true").Result
    window = mainFrame.ExecuteJavaScript (Of IJsObject)("window").Result

    ' Asynchronous execution with continuation.
    mainFrame.ExecuteJavaScript (Of IDocument)("document").ContinueWith(
        Sub(t)
            Dim baseUri As String = t.Result.BaseUri
        End Sub)
End If
```



#### Calling .NET from JavaScript

**1.x**

In .NET code:


**C#**
```csharp
public class MyObject {
    public void foo(string text) {}
}
// ...
JSValue window = browser.ExecuteJavaScriptAndReturnValue("window");
if (window.IsObject()) {
    window.AsObject().SetProperty("myObject", new MyObject());
}
```

**VB**
```vb
Public Class MyObject
    Public Sub foo(text As String)
    End Sub
End Class
' ...
Dim window As JSValue = browser.ExecuteJavaScriptAndReturnValue("window")

If window.IsObject() Then
    window.AsObject().SetProperty("myObject", New MyObject())
End If
```



In JavaScript code:

```js
window.myObject.foo("Hello");
```

**2.0**

In .NET code:


**C#**
```csharp
public class MyObject {
    public void foo(string text) {}
}
// ...
IJsObject window = frame.ExecuteJavaScript<IJsObject>("window").Result;
window.Properties["myObject"] = new MyObject();
```

**VB**
```vb
Public Class MyObject
    Public Sub foo(text As String)
    End Sub
End Class
' ...
Dim window As IJsObject = frame.ExecuteJavaScript(Of IJsObject)("window").Result
window.Properties("myObject") = New MyObject()
```



In JavaScript code:

```js
window.myObject.foo("Hello");
```

#### Injecting JavaScript

**1.x**


**C#**
```csharp
browser.ScriptContextCreated += (sender, args) =>
{
    JSValue window = browser.ExecuteJavaScriptAndReturnValue(args.Context.FrameId, @"window");
    window.AsObject().SetProperty("myObject", new MyObject());
};
```

**VB**
```vb
AddHandler browser.ScriptContextCreated, Sub(sender, args)
    Dim window As JSValue = 
        browser.ExecuteJavaScriptAndReturnValue(args.Context.FrameId, "window")
    window.AsObject().SetProperty("myObject", New MyObject())
End Sub
```



**2.0**


**C#**
```csharp
browser.InjectJsHandler = new Handler<InjectJsParameters>((args) => 
{
    IJsObject window = args.Frame.ExecuteJavaScript<IJsObject>("window").Result;
    window.Properties["myObject"] = new MyObject();
});
```

**VB**
```vb
browser.InjectJsHandler = New Handler(Of InjectJsParameters)(Sub(args)
    Dim window As IJsObject = args.Frame.ExecuteJavaScript (Of IJsObject)("window").Result
    window.Properties("myObject") = New MyObject()
End Sub)
```



#### Console events

**1.x**


**C#**
```csharp
browser.ConsoleMessageEvent += (s, args) =>
{
    string message = args.Message;
};
```

**VB**
```vb
AddHandler browser.ConsoleMessageEvent, Sub(s, args)
    Dim message As String = args.Message
End Sub
```



**2.0**


**C#**
```csharp
browser.ConsoleMessageReceived += (s, args) =>
{
    string message = args.Message;
};
```

**VB**
```vb
AddHandler browser.ConsoleMessageReceived, Sub(s, args)
    Dim message As String = args.Message
End Sub
```



### Pop-ups

#### Suppressing pop-ups

**1.x**


**C#**
```csharp
class MyPopupHandler : PopupHandler
{
    public PopupContainer HandlePopup(PopupParams popupParams)
    {
        return null;
    }
}
// ...
browser.PopupHandler = new MyPopupHandler();
```

**VB**
```vb
 Class MyPopupHandler
    Inherits PopupHandler

    Public Function HandlePopup(ByVal popupParams As PopupParams) As PopupContainer
        Return Nothing
    End Function
End Class
' ...
browser.PopupHandler = New MyPopupHandler()
```



**2.0**


**C#**
```csharp
browser.CreatePopupHandler = new Handler<CreatePopupParameters, CreatePopupResponse>((p) =>
{
    return CreatePopupResponse.Suppress();
});
```

**VB**
```vb
browser.CreatePopupHandler =
    New Handler(Of CreatePopupParameters, CreatePopupResponse)(
        Function(p) CreatePopupResponse.Suppress())
```



#### Opening pop-ups

**1.x**


**C#**
```csharp
class MyPopupContainer : PopupContainer
{
    public void InsertBrowser(Browser browser, System.Drawing.Rectangle initialBounds)
    {
        // ...
    }
}
class MyPopupHandler : PopupHandler
{
    public PopupContainer HandlePopup(PopupParams popupParams)
    {
        return new MyPopupContainer();
    }
}
// ...
browser.PopupHandler = new MyPopupHandler();
```

**VB**
```vb
Class MyPopupContainer
    Inherits PopupContainer

    Public Sub InsertBrowser(browser As Browser, initialBounds As Rectangle)
    ' ...
    End Sub
End Class

Class MyPopupHandler
    Inherits PopupHandler

    Public Function HandlePopup(popupParams As PopupParams) As PopupContainer
        Return New MyPopupContainer()
    End Function
End Class
' ...
browser.PopupHandler = New MyPopupHandler()
```



**2.0**


**C#**
```csharp
browser.CreatePopupHandler = new Handler<CreatePopupParameters, CreatePopupResponse>((p) =>
{
    return CreatePopupResponse.Create();
});
browser.OpenPopupHandler = new Handler<OpenPopupParameters>((p) =>
{
    IBrowser popup = p.PopupBrowser;
    // ...
});
```

**VB**
```vb
browser.CreatePopupHandler =
    New Handler(Of CreatePopupParameters, CreatePopupResponse)(
        Function(p) CreatePopupResponse.Create())

browser.OpenPopupHandler = New Handler(Of OpenPopupParameters)(
    Sub(p)
        Dim popup As IBrowser = p.PopupBrowser
        ' ...
    End Sub)
```



### Dialogs

#### JavaScript dialogs

**1.x**


**C#**
```csharp
class MyDialogHandler : DialogHandler
{
    public void OnAlert(DialogParams parameters) 
    {
    }

    public CloseStatus OnConfirmation(DialogParams parameters) 
    {
        return CloseStatus.CANCEL;
    }

    public CloseStatus OnPrompt(PromptDialogParams parameters) 
    {
        parameters.PromptText = "Text";
        return CloseStatus.OK;
    }
    // ...
}
// ...
browser.DialogHandler = new MyDialogHandler();
```

**VB**
```vb
Class MyDialogHandler
    Inherits DialogHandler
    Public  Sub OnAlert(ByVal parameters As DialogParams)
    End Sub
 
    Public Function OnConfirmation(ByVal parameters As DialogParams) As CloseStatus
        Return CloseStatus.CANCEL
    End Function
 
    Public Function OnPrompt(ByVal parameters As PromptDialogParams) As CloseStatus
        parameters.PromptText = "Text"
        Return CloseStatus.OK
    End Function
    ' ...
End Class
' ...
browser.DialogHandler = New MyDialogHandler()
```



**2.0**


**C#**
```csharp
browser.JsDialogs.AlertHandler = new Handler<AlertParameters>(p =>
    {
        // ...
    });
browser.JsDialogs.ConfirmHandler =
    new Handler<ConfirmParameters, ConfirmResponse>(p => 
    {
        return ConfirmResponse.Cancel();
    });
browser.JsDialogs.PromptHandler =
    new Handler<PromptParameters, PromptResponse>(p =>
    {
        return PromptResponse.SubmitText("responseText");
    });
```

**VB**
```vb
browser.JsDialogs.AlertHandler = New Handler(Of AlertParameters)(
    Sub(p)
        ' ...
    End Sub)
browser.JsDialogs.ConfirmHandler =
    New Handler(Of ConfirmParameters, ConfirmResponse)(
        Function(p) ConfirmResponse.Cancel())
browser.JsDialogs.PromptHandler =
    New Handler(Of PromptParameters, PromptResponse)(
        Function(p) PromptResponse.SubmitText("responseText"))
```



#### File dialogs

**1.x**


**C#**
```csharp
class FileChooserHandler : DialogHandler
{
    public CloseStatus OnFileChooser(FileChooserParams parameters) {
        FileChooserMode mode = parameters.Mode;
        if (mode == FileChooserMode.Open) {
            parameters.SelectedFiles = "file1.txt";
        }
        if (mode == FileChooserMode.OpenMultiple) {
            string[] selectedFiles = {"file1.txt", "file2.txt"};
            parameters.SelectedFiles = string.Join("|", selectedFiles);
        }
        return CloseStatus.OK;
    }
    // ...
}
// ...
browser.DialogHandler = new FileChooserHandler();
```

**VB**
```vb
Class FileChooserHandler
    Inherits DialogHandler

    Public Function OnFileChooser(parameters As FileChooserParams) As CloseStatus
        Dim mode As FileChooserMode = parameters.Mode

        If mode Is FileChooserMode.Open Then
            parameters.SelectedFiles = "file1.txt"
        End If

        If mode Is FileChooserMode.OpenMultiple Then
            Dim selectedFiles As String() = {"file1.txt", "file2.txt"}
            parameters.SelectedFiles = String.Join("|", selectedFiles)
        End If

        Return CloseStatus.OK
    End Function
    ' ...
End Class
' ...
browser.DialogHandler = New FileChooserHandler()
```



**2.0**


**C#**
```csharp
browser.Dialogs.OpenFileHandler =
    new Handler<OpenFileParameters, OpenFileResponse>(p =>
    {
        return OpenFileResponse.SelectFile(Path.GetFullPath(p.DefaultFileName));
    });

browser.Dialogs.OpenMultipleFilesHandler =
    new Handler<OpenMultipleFilesParameters, OpenMultipleFilesResponse>(p =>
    {
        return OpenMultipleFilesResponse.SelectFiles(Path.GetFullPath("file1.txt"),
            Path.GetFullPath("file2.txt"));
    });
```

**VB**
```vb
browser.Dialogs.OpenFileHandler =
    New Handler(Of OpenFileParameters, OpenFileResponse)(
        Function(p) OpenFileResponse.SelectFile(
            Path.GetFullPath(p.DefaultFileName)))

browser.Dialogs.OpenMultipleFilesHandler =
    New Handler(Of OpenMultipleFilesParameters, OpenMultipleFilesResponse)(
        Function(p) OpenMultipleFilesResponse.SelectFiles(
            Path.GetFullPath("file1.txt"),
            Path.GetFullPath("file2.txt")))
```



#### Color dialogs

**1.x**


**C#**
```csharp
class ColorDialogHandler : DialogHandler
{
    private Color color;

    public ColorDialogHandler()
    {
        color = Color.White;
    }
    
    public CloseStatus OnColorChooser(ColorChooserParams parameters)
    {        
        parameters.Color = color;
        return CloseStatus.OK;
    }
    // ...
}
// ...
browser.DialogHandler = new ColorDialogHandler();
```

**VB**
```vb
Class ColorDialogHandler
    Inherits DialogHandler

    Private ReadOnly color As Color

    Public Sub New()
        color = Color.White
    End Sub

    Public Function OnColorChooser(parameters As ColorChooserParams) As CloseStatus
        parameters.Color = color
        Return CloseStatus.OK
    End Function
    ' ...
End Class
' ...
browser.DialogHandler = New ColorDialogHandler()
```



**2.0**


**C#**
```csharp
browser.Dialogs.SelectColorHandler =
    new Handler<SelectColorParameters, SelectColorResponse>(p =>
    {
        return SelectColorResponse.SelectColor(p.DefaultColor);
    });
```

**VB**
```vb
browser.Dialogs.SelectColorHandler =
    New Handler(Of SelectColorParameters, SelectColorResponse)(
        Function(p) SelectColorResponse.SelectColor(p.DefaultColor))
```



#### SSL certificate dialogs

**1.x**


**C#**
```csharp
class SelectCertificateDialogHandler : DialogHandler
{
    private const string ClientCertFile = "<cert-file>.pfx";
    private const string ClientCertPassword = "<cert-password>";
    private Certificate certificate;

    public SelectCertificateDialogHandler()
    {
        certificate = new X509Certificate2(Path.GetFullPath(ClientCertFile),
                                           ClientCertPassword,
                                           X509KeyStorageFlags.Exportable);
    }
    
    public CloseStatus OnSelectCertificate(CertificatesDialogParams parameters)
    {        
        parameters.SelectedCertificate = certificate;
        selectCertificateEvent.Set();
        return CloseStatus.OK;
    }
    // ...
}
// ...
browser.DialogHandler = new SelectCertificateDialogHandler();
```

**VB**
```vb
Class SelectCertificateDialogHandler
    Inherits DialogHandler

    Private Const ClientCertFile As String = "<cert-file>.pfx"
    Private Const ClientCertPassword As String = "<cert-password>"
    Private certificate As Certificate

    Public Sub New()
        certificate = New X509Certificate2(Path.GetFullPath(ClientCertFile),
                                           ClientCertPassword,
                                           X509KeyStorageFlags.Exportable)
    End Sub

    Public Function OnSelectCertificate(ByVal p As CertificatesDialogParams) As CloseStatus
        p.SelectedCertificate = certificate
        selectCertificateEvent.Set()
        Return CloseStatus.OK
    End Function
    ' ...
End Class
' ...
browser.DialogHandler = New SelectCertificateDialogHandler()
```



**2.0**


**C#**
```csharp
string ClientCertFile = "<cert-file>.pfx";
string ClientCertPassword = "<cert-password>";
// ...
X509Certificate2 certificate = new X509Certificate2(Path.GetFullPath(ClientCertFile),
    ClientCertPassword,
    X509KeyStorageFlags.Exportable);
Certificate cert = new Certificate(certificate);
browser.SelectCertificateHandler
    = new Handler<SelectCertificateParameters, SelectCertificateResponse>(p =>
    {
        return SelectCertificateResponse.Select(cert);
    });
```

**VB**
```vb
Dim ClientCertFile = "<cert-file>.pfx"
Dim ClientCertPassword = "<cert-password>"
' ...
Dim certificate = New X509Certificate2(Path.GetFullPath(ClientCertFile),
                                       ClientCertPassword,
                                       X509KeyStorageFlags.Exportable)
Dim cert = New Certificate(certificate)
browser.SelectCertificateHandler =
    New Handler(Of SelectCertificateParameters, SelectCertificateResponse)(
        Function(p) SelectCertificateResponse.Select(cert))
```



### Printing

#### Configuring printing

**1.x**


**C#**
```csharp
class MyPrintHandler : PrintHandler
{
    public PrintStatus OnPrint(PrintJob printJob)
    {
        PrintSettings printSettings = printJob.PrintSettings;
        printSettings.PrinterName = "Microsoft XPS Document Writer";
        printSettings.Landscape = true;
        printSettings.PrintBackgrounds = true;
        return PrintStatus.CONTINUE;
    }
}
// ...
browser.PrintHandler = new MyPrintHandler();
```

**VB**
```vb
Class MyPrintHandler
    Inherits PrintHandler

    Public Function OnPrint(ByVal printJob As PrintJob) As PrintStatus
        Dim printSettings As PrintSettings = printJob.PrintSettings
        printSettings.PrinterName = "Microsoft XPS Document Writer"
        printSettings.Landscape = True
        printSettings.PrintBackgrounds = True
        Return PrintStatus.CONTINUE
    End Function
End Class
' ...
browser.PrintHandler = New MyPrintHandler()
```



**2.0**

Functionality that allows configuring printing has been removed in DotNetBrowser version 2.0. Now the standard Print Preview dialog where you can provide the required settings is displayed:


**C#**
```csharp
browser.PrintHandler =
    new Handler<PrintParameters, PrintResponse>(p =>
    {
        return PrintResponse.ShowPrintPreview();
    });
```

**VB**
```vb
browser.PrintHandler =
    New Handler(Of PrintParameters, PrintResponse)(
        Function(p) PrintResponse.ShowPrintPreview())
```



#### Suppressing printing

**1.x**


**C#**
```csharp
class MyPrintHandler : PrintHandler
{
    public PrintStatus OnPrint(PrintJob printJob)
    {
        return PrintStatus.CANCEL;
    }
}
// ...
browser.PrintHandler = new MyPrintHandler();
```

**VB**
```vb
Class MyPrintHandler
    Inherits PrintHandler

    Public Function OnPrint(ByVal printJob As PrintJob) As PrintStatus
        Return PrintStatus.CANCEL
    End Function
End Class
' ...
browser.PrintHandler = New MyPrintHandler()
```



**2.0**


**C#**
```csharp
browser.PrintHandler =
    new Handler<PrintParameters, PrintResponse>(p =>
    {
        return PrintResponse.Cancel();
    });
```

**VB**
```vb
browser.PrintHandler =
    New Handler(Of PrintParameters, PrintResponse)(
        Function(p) PrintResponse.Cancel())
```



### Cache

#### Clearing HTTP cache

**1.x**


**C#**
```csharp
browser.CacheStorage.ClearCache(() => 
{
    // HTTP Disk Cache has been cleared.
});
```

**VB**
```vb
browser.CacheStorage.ClearCache(Sub()
    ' HTTP Disk Cache has been cleared.
End Sub)
```



**2.0**


**C#**
```csharp
await engine.HttpCache.ClearDiskCache();
// HTTP Disk Cache has been cleared.
```

**VB**
```vb
Await engine.HttpCache.ClearDiskCache()
' HTTP Disk Cache has been cleared.
```



or


**C#**
```csharp
engine.HttpCache.ClearDiskCache().Wait();
// HTTP Disk Cache has been cleared.
```

**VB**
```vb
engine.HttpCache.ClearDiskCache().Wait()
' HTTP Disk Cache has been cleared.
```



### Cookies

#### Accessing cookies

**1.x**


**C#**
```csharp
List<Cookie> cookies = browser.CookieStorage.GetAllCookies();
```

**VB**
```vb
Dim cookies As List(Of Cookie) = browser.CookieStorage.GetAllCookies()
```



**2.0**


**C#**
```csharp
IEnumerable<Cookie> cookies = await engine.CookieStore.GetAllCookies();
```

**VB**
```vb
Dim cookies As IEnumerable(Of Cookie) = Await engine.CookieStore.GetAllCookies()
```



or


**C#**
```csharp
IEnumerable<Cookie> cookies = engine.CookieStore.GetAllCookies().Result;
```

**VB**
```vb
Dim cookies As IEnumerable(Of Cookie) = engine.CookieStore.GetAllCookies().Result
```



### Render process termination

Each browser instance is running on a separate native process where the web page is rendered.

Sometimes this process can exit unexpectedly because of the plugin crash. The render process termination event can be used to receive notifications about unexpected render process termination. 

**1.x**


**C#**
```csharp
browser.RenderGoneEvent += (s, e) =>
{
    TerminationStatus status = e.TerminationStatus;
};
```

**VB**
```vb
AddHandler browser.RenderGoneEvent , Sub(s, e)
    Dim status As TerminationStatus = e.TerminationStatus
End Sub
```



**2.0**


**C#**
```csharp
browser.RenderProcessTerminated += (s, e) =>
{
    TerminationStatus status = e.TerminationStatus;
};
```

**VB**
```vb
AddHandler browser.RenderProcessTerminated , Sub(s, e)
    Dim status As TerminationStatus = e.TerminationStatus
End Sub
```



### Chromium

#### Switches

The library does not support all possible Chromium switches. It allows configuring Chromium with the switches, but we do not guarantee that the passed switches will work correctly or work at all. We recommend to check this functionality before using.

**1.x**


**C#**
```csharp
BrowserPreferences.SetChromiumSwitches(
    "--<switch_name>",
    "--<switch_name>=<switch_value>"
);
```

**VB**
```vb
BrowserPreferences.SetChromiumSwitches(
    "--<switch_name>", 
    "--<switch_name>=<switch_value>"
)
```



**2.0**


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumSwitches = { "--<switch-name>", "--<switch-name>=<switch-value>" }
}.Build());
```

**VB**
```vb
Dim engineOptions = New EngineOptions.Builder
engineOptions.ChromiumSwitches.Add("--<switch-name>")
engineOptions.ChromiumSwitches.Add("--<switch-name>=<switch-value>")

Dim engine = EngineFactory.Create(engineOptions.Build())
```



#### API keys

**1.x**


**C#**
```csharp
BrowserPreferences.SetChromiumVariable(
        "GOOGLE_API_KEY", "My API Key");
BrowserPreferences.SetChromiumVariable(
        "GOOGLE_DEFAULT_CLIENT_ID", "My Client ID");
BrowserPreferences.SetChromiumVariable(
        "GOOGLE_DEFAULT_CLIENT_SECRET", "My Client Secret");
```

**VB**
```vb
BrowserPreferences.SetChromiumVariable( _
    "GOOGLE_API_KEY", "My API Key")
BrowserPreferences.SetChromiumVariable( _
    "GOOGLE_DEFAULT_CLIENT_ID", "My Client ID")
BrowserPreferences.SetChromiumVariable( _
    "GOOGLE_DEFAULT_CLIENT_SECRET", "My Client Secret")
```



**2.0**


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    GoogleApiKey = "<api-key>",
    GoogleDefaultClientId = "<client-id>",
    GoogleDefaultClientSecret = "<client-secret>"
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With {
    .GoogleApiKey = "<api-key>",
    .GoogleDefaultClientId = "<client-id>",
    .GoogleDefaultClientSecret = "<client-secret>"
}.Build())
```



### Logging

In the new version, we improved the logging API. Read more about how to configure logging in the [Troubleshooting](https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/logging/) guide.

## FAQ

#### How long will DotNetBrowser version 1.x be supported?

DotNetBrowser version 1.x will be supported till February 2021. All new features, Chromium upgrades, support of the new operating systems and .NET implementations, different enhancements, will be applied on top of the [latest (mainstream) version](https://teamdev.com/dotnetbrowser/).

#### Can I upgrade to DotNetBrowser 2 for free?

If you already own a commercial license for DotNetBrowser 1 with an active Subscription, then you can receive a commercial license key for DotNetBrowser 2 for free. Contact our [Sales Team](https://teamdev.com/contacts/) if you have any questions regarding this.

#### I have a case not covered by this guide. What should I do?

We recommend checking our [Guides](https://teamdev.com/dotnetbrowser/docs/guides/) section. DotNetBrowser version 1.0 and version 2.0 have almost identical functionality. So, if this migration guide does not describe an alternative to the DotNetBrowser version 1.0 functionality you use, you can find description of the similar functionality in our guides where the documents are grouped by feature areas.

If you do not see description of the required functionality in the guides, [submit a ticket](https://dotnetbrowser.support.teamdev.com/support/tickets/new).
