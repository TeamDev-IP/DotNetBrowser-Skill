
# Engine

**Lead**
This guide describes how to create, use, and close `Engine`.


Refer to [Architecture](https://teamdev.com/dotnetbrowser/docs/guides/architecture/) guide for information on how DotNetBrowser architecture is designed and works as well as main components it provides.

## Creating an engine

To create a new `IEngine` instance, use the `EngineFactory.Create()` or the `EngineFactory.Create(EngineOptions)` static methods. The method overload with `EngineOptions` initializes and runs the Chromium engine with the passed options.


**C#**
```csharp
IEngine engine = EngineFactory.Create(engineOptions);
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(engineOptions)
```



Depending on the hardware performance, the initialization process might take several seconds. You can create the engine on any thread, including the UI thread. However, if you call `EngineFactory.Create()` on the UI thread, the application UI does not respond until the engine starts.

To keep the UI responsive, use the `EngineFactory.CreateAsync()` method. It has the same overloads as `EngineFactory.Create()` and returns `Task<IEngine>`:


**C#**
```csharp
IEngine engine = await EngineFactory.CreateAsync(engineOptions);
```

**VB**
```vb
Dim engine As IEngine = Await EngineFactory.CreateAsync(engineOptions)
```



When a new `IEngine` instance is created, DotNetBrowser performs the following actions:

1. Checks the environment and makes sure that it is a [supported](https://teamdev.com/dotnetbrowser/docs/guides/requirements/) one.
2. Finds the [Chromium binaries](https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#binaries) and extracts them to the required [directory](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#chromium-binaries-directory) if necessary.
3. Runs the [main process](https://teamdev.com/dotnetbrowser/docs/guides/architecture/#chromium-main-process) of the Chromium engine.
4. Establishes the [IPC](https://teamdev.com/dotnetbrowser/docs/guides/architecture/#inter-process-communication) connection between .NET and the Chromium main process.

## Engine options

This section highlights major Engine options you can customize. 

### Rendering mode

This option indicates how the content of a web page is [rendered](https://teamdev.com/dotnetbrowser/docs/guides/gs/browser-view/#rendering). DotNetBrowser supports the following rendering modes:

* hardware-accelerated
* off-screen

#### Hardware-accelerated mode

Chromium renders the content using GPU and displays it directly on a surface. See the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(RenderingMode.HardwareAccelerated);
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(RenderingMode.HardwareAccelerated)
```



Read [more](https://teamdev.com/dotnetbrowser/docs/guides/gs/browser-view/#hardware-accelerated) about hardware accelerated rendering mode, its performance, and limitations.

#### Off-screen mode

Chromium renders the content using GPU and copies the pixels to RAM. See the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(RenderingMode.OffScreen);
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(RenderingMode.OffScreen)
```



Read [more](https://teamdev.com/dotnetbrowser/docs/guides/gs/browser-view/#off-screen) about off-screen rendering mode, its performance, and limitations.

### Language

This option configures the language used on the default error pages and message [dialogs](https://teamdev.com/dotnetbrowser/docs/guides/gs/dialogs/). By default, the language is dynamically configured according to the default locale of your .NET application. If the list of [supported languages](https://api.dotnetbrowser.dev/4.3.3/api/DotNetBrowser.Ui.Language) does not contain the language obtained from the .NET application locale, American English is used.

Current option allows to override the default behavior and configure the Chromium engine with the given language. See the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    Language = DotNetBrowser.Ui.Language.German
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .Language = DotNetBrowser.Ui.Language.German
}.Build())
```



In the code sample above, we configure the `IEngine` with the German language. If DotNetBrowser fails to load a web page, the error page in German is displayed:

![Error Page](https://teamdev.com/dotnetbrowser/img/articles/guides/engine/error-page.webp)

### User data directory

Represents an absolute path to the directory containing the profiles and their data such as cache, cookies, history, GPU cache, local storage, visited links, web data, spell checking dictionary files, and so on. See the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    UserDataDirectory = @"C:\Users\Me\DotNetBrowser"
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .UserDataDirectory = "C:\Users\Me\DotNetBrowser"
}.Build())
```



**Important**
Same user data directory cannot be used simultaneously by multiple `IEngine` instances running in a single or different .NET applications. The `IEngine` creation fails if the directory is already used by another `IEngine`.


**Note**
If you do not provide the user data directory path, DotNetBrowser creates and uses a temp directory in the user's temp folder.


### Incognito

This option indicates whether *incognito* mode for the default profile is enabled. In this mode, the user data such as browsing history, cookies, site data, and the information entered in the forms on the web pages is stored in the memory. It will be released once you delete `Profile` or dispose the `IEngine`.

**Note**
By default, incognito mode is disabled.


The following example demonstrates how to enable incognito mode:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    IncognitoEnabled = true
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .IncognitoEnabled = true
}.Build())
```



### Intercept request per URI scheme
The `Schemes` option can be used to configure the URL request interception per scheme. Here is how to configure it to intercept and handle all the requests for the custom URI schemes:


**C#**

```csharp
Handler<InterceptRequestParameters, InterceptRequestResponse> handler =
    new Handler<InterceptRequestParameters, InterceptRequestResponse>(p =>
    {
        UrlRequestJobOptions options = new UrlRequestJobOptions
        {
            Headers = new List<HttpHeader>
            {
                new HttpHeader("Content-Type", "text/html", "charset=utf-8")
            }
        };

        UrlRequestJob job = p.Network.CreateUrlRequestJob(p.UrlRequest, options);

        Task.Run(async () =>
        {
            // The request processing is performed in a worker thread
            // in order to avoid freezing the web page.
            try
            {
                await job.WriteAsync(Encoding.UTF8.GetBytes("Hello world!"));
                job.Complete();
            }
            catch
            {
                job.Fail();
            }
        });

        return InterceptRequestResponse.Intercept(job);
    });

EngineOptions engineOptions = new EngineOptions.Builder
{
    Schemes =
    {
        { Scheme.Create("myscheme"), handler }
    }
}.Build();

using (IEngine engine = EngineFactory.Create(engineOptions))
{
    using (IBrowser browser = engine.CreateBrowser())
    {
        NavigationResult result =
            browser.Navigation.LoadUrl("myscheme://test1").Result;

        // If the scheme handler was not set, the LoadResult would be 
        // LoadResult.Stopped.
        // However, with the scheme handler, the web page is loaded and
        // the result is LoadResult.Completed.
        Console.WriteLine($"Load result: {result.LoadResult}");
        Console.WriteLine($"HTML: {browser.MainFrame.Html}");
    }
}
```

**VB**

```vb
Dim interceptRequestHandler =
New Handler(Of InterceptRequestParameters, InterceptRequestResponse)(
    Function(p)
        Dim options = New UrlRequestJobOptions With {
                .Headers = New List(Of HttpHeader) From {
                New HttpHeader("Content-Type", "text/html",
                               "charset=utf-8")
                }
                }

        Dim job As UrlRequestJob =
                p.Network.CreateUrlRequestJob(p.UrlRequest, options)

        Task.Run(Async Function()
                     ' The request processing is performed in a worker thread
                     ' in order to avoid freezing the web page.
                     Try
                         Await job.WriteAsync(Encoding.UTF8.GetBytes("Hello world!"))
                         job.Complete()
                     Catch
                         job.Fail()
                     End Try
                 End Function)

        Return InterceptRequestResponse.Intercept(job)
    End Function)


Dim engineOptionsBuilder = new EngineOptions.Builder
With engineOptionsBuilder
    .Schemes.Add(Scheme.Create("myscheme"), interceptRequestHandler)
End With

Dim engineOptions = engineOptionsBuilder.Build()

Using engine As IEngine = EngineFactory.Create(engineOptions)

    Using browser As IBrowser = engine.CreateBrowser()
        Dim result As NavigationResult =
                browser.Navigation.LoadUrl("myscheme://test1").Result
        ' If the scheme handler was not set, the LoadResult would be 
        ' LoadResult.Stopped.
        ' However, with the scheme handler, the web page is loaded and
        ' the result is LoadResult.Completed.
        Console.WriteLine($"Load result: {result.LoadResult.ToString()}")
        Console.WriteLine($"HTML: {browser.MainFrame.Html}")
    End Using
End Using
```



You can also use asynchronous and stream-based response writing APIs such as
`UrlRequestJob.WriteAsync(...)` and
`UrlRequestJobExtensions.WriteAsync(...)`.
After writing all data, call `Complete()`.
If writing cannot be completed, call `Fail()`.

Head to our repository for the complete example: [C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/csharp/console/CustomRequestHandling/Program.cs), [VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/vbnet/console/CustomRequestHandling/Program.vb).

The same approach can be used to intercept and handle all HTTPS requests.

Not all schemes can be intercepted. For example, it is not possible to intercept schemes such as `chrome`, `data`, or `chrome-extensions`. The attempt to intercept them might lead to unexpected behavior or crash inside Chromium.

In addition, some schemes are treated as local schemes, e.g. `file`. They cannot be intercepted because it is not a network request.

**Note**
If the specified scheme cannot be intercepted, the corresponding exception will be thrown by the `EngineOptions` builder. For example: "The "file" scheme cannot be intercepted."



### User agent

Using this option you can configure the default user agent string. See the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    UserAgent = "<user-agent>"
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .UserAgent = "<user-agent>"
}.Build())
```



You can [override](https://teamdev.com/dotnetbrowser/docs/guides/gs/browser/#user-agent) the default user agent string in each `IBrowser` instance.

### Remote debugging port

This option allows to enable the Chrome Developer Tools (or DevTools) remote debugging. The following example demonstrates how to use this feature:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumSwitches = { "--remote-allow-origins=http://localhost:9222" },
    RemoteDebuggingPort = 9222
}.Build());
```

**VB**
```vb
Dim engineOptions = New EngineOptions.Builder With {
    .RemoteDebuggingPort = 9222
}
engineOptions.ChromiumSwitches.Add("--remote-allow-origins=http://localhost:9222")

Dim engine As IEngine = EngineFactory.Create(engineOptions.Build())
```



**Note**
Since Chromium 111, it is required to specify `remote-allow-origins` switch to allow web socket connections from specified origin. More information in [Issue 1422444.](https://bugs.chromium.org/p/chromium/issues/detail?id=1422444)


Now you can load the [remote debugging URL](https://teamdev.com/dotnetbrowser/docs/guides/gs/browser/#remote-debugging-url) in an `IBrowser` instance to open the DevTools page to inspect HTML, debug JavaScript, and others. See an example below:

![Remote Debugging Port](https://teamdev.com/dotnetbrowser/img/articles/guides/engine/remote-debugging-port.webp)

**Important**
Do not open the remote debugging URL in other web browser applications such as Mozilla Firefox, Microsoft Internet Explorer, Safari, Opera, and others as it can result in a native crash in Chromium DevTools web server.


**Note**
The remote debugging feature is compatible only with the Chromium version used by DotNetBrowser library. For example, if you use DotNetBrowser 4.3.3 based on Chromium 155.0.8059.40, you can open the remote debugging URL only in the same Chromium/Google Chrome.
<br>
<br>
We recommend loading the remote debugging URL in an `IBrowser` instance instead of Google Chrome.


### Disabling touch menu

Long press on Windows 10 touch devices may show the following touch menu:

![Touch Menu](https://teamdev.com/dotnetbrowser/img/articles/guides/engine/touch-menu.webp)

The code sample below demonstrates how to disable this touch menu:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    TouchMenuDisabled = true
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .TouchMenuDisabled = true
}.Build())
```



### Chromium binaries directory

Use this option to define an absolute or relative path to the directory where the Chromium binaries are located or should be extracted to. See the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumDirectory = @"C:\Users\Me\.DotNetBrowser\chromium"
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .ChromiumDirectory = @"C:\Users\Me\.DotNetBrowser\chromium"
}.Build())
```



For details, refer to [Chromium Binaries Location](https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#location) section.

### Autoplaying videos

To enable autoplay of video content on the web pages, use the option below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    AutoplayEnabled = true
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .AutoplayEnabled = true
}.Build())
```



### Chromium switches

Use this option to define the Chromium [switches](https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#switches) passed to the Chromium [main process](https://teamdev.com/dotnetbrowser/docs/guides/architecture/#chromium-main-process). See the code sample below:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ChromiumSwitches = { "--<switch-name>", "--<switch-name>=<switch-value>" }
}.Build());
```

**VB**
```vb
Dim engineOptions As New EngineOptions.Builder()
engineOptions.ChromiumSwitches.Add("--<switch-name>")
engineOptions.ChromiumSwitches.Add("--<switch-name>=<switch-value>")

Dim engine As IEngine  = EngineFactory.Create(engineOptions.Build())
```



**Important**
Not all the Chromium switches are supported by DotNetBrowser, so there is no guarantee that the passed switches will work and will not cause any errors. We recommend configuring Chromium through the [Engine Options](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#engine-options) instead of switches.


### Google APIs

Some Chromium features such as Geolocation, Spelling, Speech, and others use Google APIs. To access those APIs, an API Key, OAuth 2.0 client ID, and client secret are required. To acquire the API Key, follow these [instructions](http://www.chromium.org/developers/how-tos/api-keys#acquiring-keys).

To provide the API Key, client ID, and client secret, use the following code sample:


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
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .GoogleApiKey = "<api-key>",
    .GoogleDefaultClientId = "<client-id>",
    .GoogleDefaultClientSecret = "<client-secret>"
}.Build())
```



**Note**
Setting up API keys is optional. However, if this is not done, some APIs using Google services fail to work.


#### Geolocation

Geolocation is one of Chromium features using Google API. You must enable __Google Maps Geolocation API__ and [billing](https://support.google.com/googleapi/answer/6158867?hl=en), otherwise, Geolocation API fails to work. Once you enable Google Maps Geolocation API and billing, you can [provide the keys](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#google-apis) to DotNetBrowser Chromium engine.

**Note**
To enable geolocation in DotNetBrowser, grant a specific [permission](https://teamdev.com/dotnetbrowser/docs/guides/gs/permissions/).


#### Voice recognition 

Voice recognition is one of those Chromium features that uses Google API. You must enable __Speech API__ and [billing](https://support.google.com/googleapi/answer/6158867?hl=en), otherwise voice recognition does not work.

Once you enable Speech API and billing, you can [provide the keys](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#google-apis) to DotNetBrowser Chromium engine.

## Engine dispose

The `IEngine` instance allocates memory and system resources that must be released. When the `IEngine` is no longer needed, it must be disposed through the `IEngine.Dispose()` method to shutdown the native Chromium process and free all the allocated memory and system resources. See the example below:


**C#**
```csharp
IEngine engine = EngineFactory.Create();
// ...
engine.Dispose();
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create()
' ...
engine.Dispose()
```



**Note**
Any attempt to use an already disposed `IEngine` will lead to the `ObjectDisposedException`.


To check whether the `IEngine` is disposed, use the `IsDisposed` property shown in the code sample below:


**C#**
```csharp
bool disposed = engine.IsDisposed;
```

**VB**
```vb
Dim disposed As Boolean = engine.IsDisposed
```



## Engine events
### Engine disposed

To get notifications when the `IEngine` is disposed, use the `Disposed` event shown in the code sample below:


**C#**
```csharp
engine.Disposed += (s, e) => {};
```

**VB**
```vb
AddHandler engine.Disposed, Sub(s, e)
End Sub
```



### Engine crashed

To get notifications when the `IEngine` unexpectedly crashes due to an error inside the Chromium engine, use the approach shown in the code sample below:


**C#**
```csharp
engine.Disposed += (s, e) => 
{
    long exitCode = e.ExitCode;
    // The engine has crashed if this exit code is non-zero.
};
```

**VB**
```vb
AddHandler engine.Disposed, Sub(s, e)
    Dim exitCode As Long = e.ExitCode
    ' The engine has crashed if this exit code is non-zero.
End Sub
```


