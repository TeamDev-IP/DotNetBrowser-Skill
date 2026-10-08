
# Selenium

**Lead**
Selenium WebDriver can attach to the browser your application already embeds
and drive the page your users see. This tutorial covers the connection code,
the ChromeDriver version constraint, and what does not work.


Selenium reaches Chromium through ChromeDriver. ChromeDriver normally starts a
browser of its own, but it can also attach to one that is already running and
exposes a remote debugging endpoint over the Chrome DevTools Protocol, or CDP.
That is how it connects to DotNetBrowser.

Read [DevTools Protocol](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/) first
for the rules that apply to every automation tool.

## Prerequisites

Reference two NuGet packages in the project that runs the test scenario:

* `Selenium.WebDriver` — the WebDriver API. The example uses `3.141.0`, and
  the API shown here is unchanged in Selenium 4.
* `Selenium.WebDriver.ChromeDriver` — the ChromeDriver executable.

DotNetBrowser 4.3.3 is based on Chromium
155.0.8059.40, so use a
`Selenium.WebDriver.ChromeDriver` package built for that release.

## Enabling the endpoint

Create the engine with a remote debugging port:


**C#**

```csharp
EngineOptions engineOptions = new EngineOptions.Builder
    {
        RemoteDebuggingPort = RemoteDebuggingPort
    }
   .Build();

engine = EngineFactory.Create(engineOptions);
browser = engine.CreateBrowser();
```

**VB**

```vb
Dim engineOptionsBuilder As EngineOptions.Builder = new EngineOptions.Builder
With engineOptionsBuilder
    .RemoteDebuggingPort = RemoteDebuggingPort
End With

Dim engineOptions = engineOptionsBuilder.Build()

engine = EngineFactory.Create(engineOptions)
browser = engine.CreateBrowser()
```



`RemoteDebuggingPort` is the only engine option the connection needs.

## Connecting the driver

Point `ChromeOptions.DebuggerAddress` at the endpoint and create the driver:


**C#**

```csharp
ChromeOptions options = new ChromeOptions
{
    DebuggerAddress = RemoteDebuggingAddress
};

IWebDriver webDriver = new ChromeDriver(options)
{
    Url = StartPage
};

// Give FindElement time to wait for the page to load.
webDriver.Manage().Timeouts().ImplicitWait =
    TimeSpan.FromSeconds(10);
```

**VB**

```vb
Dim options As ChromeOptions = new ChromeOptions
With options
    .DebuggerAddress = RemoteDebuggingAddress
End With

Dim webDriver As IWebDriver = new ChromeDriver(options)
With webDriver
    .Url = StartPage
End With

' Give FindElement time to wait for the page to load.
webDriver.Manage().Timeouts().ImplicitWait = TimeSpan.FromSeconds(10)
```



`DebuggerAddress` takes a host and port, without a scheme. The port has to be
the one the engine opened: the example sets `RemoteDebuggingPort` to `9222`, so
the driver connects to `localhost:9222`. When `DebuggerAddress` is set,
ChromeDriver attaches to that endpoint instead of starting a browser.

Assigning `Url` navigates the page that is already open in the `BrowserView`
control. The example points it at a page shipped alongside the application, so
the scenario does not depend on an external site.

From there the element-level WebDriver API applies: `FindElement`, `Click`,
`SendKeys`, and script execution all operate on the embedded browser. The
implicit wait covers the navigation a click starts, so `FindElement` retries
until the next page has loaded instead of failing on the first attempt.

Window commands are the exception. The window belongs to your application, not
to ChromeDriver: switching to full screen fails outright, and the rest are not
reliable. Size the `BrowserView` control from your application instead.

## Threading and lifetime

The example runs its scenario from the form `Load` handler, once the engine is
up, and calls `webDriver.Quit()` when the scenario finishes.

WebDriver calls block, so run them off the UI thread and marshal any result
back before touching controls. The example wraps the scenario in `Task.Run`
and calls `Invoke` when it needs the form.

## Troubleshooting

A version mismatch between ChromeDriver and Chromium is the most common
failure. ChromeDriver reports it as a session creation error naming both
versions. Install the `Selenium.WebDriver.ChromeDriver` version named in
[Prerequisites](#prerequisites).

If the connection is refused, check that the engine was created with
`RemoteDebuggingPort`, that the port in `DebuggerAddress` is the same one, and
that the engine is running when the driver connects. Trying `127.0.0.1`
instead of `localhost` is also worth a moment.

The complete example is available in our repository:
[C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/csharp/devtools-protocol/SeleniumChromeDriver),
[VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/vbnet/devtools-protocol/SeleniumChromeDriver).
