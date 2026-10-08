
# DevTools Protocol

**Lead**
This tutorial explains how to connect Selenium, Playwright, Puppeteer, and
other automation tools to the browser embedded in your .NET application.


Selenium, Playwright, and Puppeteer normally start their own copy of Chrome
and drive it. With DotNetBrowser the browser already exists: it runs inside
your application and displays web pages in a `BrowserView` control. Rather
than starting a browser, these tools attach to the one you have.

They attach over the Chrome DevTools Protocol, or CDP — the same protocol
Chrome DevTools speaks. DotNetBrowser can expose a remote debugging endpoint
on a local TCP port, and any CDP client can connect to it.

Once connected, the tool operates on the page your application already
displays. Clicks, navigation, and script evaluation issued from the test code
appear in the `BrowserView` control. That lets you run an existing test suite
against the web UI inside your own application rather than against a
standalone browser.

## Opening the endpoint

Set `RemoteDebuggingPort` on `EngineOptions.Builder` when you create the
`IEngine` instance:


**C#**
```csharp
IEngine engine = EngineFactory.Create(
    new EngineOptions.Builder
    {
        RemoteDebuggingPort = 9222
    }.Build()
);
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(
    New EngineOptions.Builder() With {
        .RemoteDebuggingPort = 9222
    }.Build()
)
```



Any free TCP port works. These tutorials use `9222` for Selenium, `9223` for
Playwright and Puppeteer, and `9224` for MCP servers.

Address the endpoint as `localhost` or `127.0.0.1`. Both normally work, but
`localhost` can resolve to an address the endpoint is not listening on, which
surfaces as a refused connection.

The [Engine](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#remote-debugging-port) guide covers the
same option in more detail. Its `--remote-allow-origins` switch is for clients
that are themselves web pages, such as the DevTools front end: a browser
attaches an `Origin` header, and Chromium answers `403` unless that origin is
allowed. Selenium, Playwright, and Puppeteer send no `Origin` header, so these
tutorials do not need the switch.

## Security

**Important**
The remote debugging endpoint has no authentication. Any process on the same
machine that can reach the port can control the pages in that engine. Enable
it for local development and test runs, and keep it disabled in the builds you
ship.


## Attach, do not launch

Every one of these tools offers two modes: start a browser, or connect to a
running one. With DotNetBrowser you always use the second mode, and you work
with the page that is already open.

| Tool | Connect API | The already-open page |
|---|---|---|
| Selenium | `ChromeOptions.DebuggerAddress` | the driver's current page |
| Playwright | `IBrowserType.ConnectOverCDPAsync` | `Contexts[0].Pages[0]` |
| Puppeteer | `Puppeteer.ConnectAsync` with `ConnectOptions.BrowserURL` | the first entry of `PagesAsync()` |
| MCP servers | `--cdp-endpoint` (Playwright MCP), `--browser-url` (Chrome DevTools MCP) | the current tab; page `1` in `list_pages` |

A `BrowserView` displays the `IBrowser` instance it was initialized from, so
that page is the one your users see. DotNetBrowser does not support opening a
page from the tool, such as `NewPageAsync` in Playwright and Puppeteer,
because browsers are created in other ways: your application creates each
`IBrowser` with `IEngine.CreateBrowser`, and a page opens
[pop-ups](https://teamdev.com/dotnetbrowser/docs/guides/gs/popups/) that the pop-up handlers allow.

These tutorials all assume a single page. If the engine has several browsers,
or a popup has opened, the order of `Pages` and `PagesAsync()` is not
guaranteed — match on the page URL rather than taking the first entry.

## Match the Chromium version

How closely the client has to track Chromium depends on the tool.

ChromeDriver is versioned against Chromium directly and refuses to attach to a
build it does not recognize. DotNetBrowser 4.3.3 is based on Chromium
155.0.8059.40, so the
`Selenium.WebDriver.ChromeDriver` package has to be built for that Chromium
release. A mismatch is the most common reason a Selenium connection fails.

Playwright and Puppeteer tolerate a version gap. Each pins a Chromium build of
its own but speaks a stable subset of the protocol to whatever it attaches to,
so these tutorials use package versions built against much older Chromium
releases and still connect. A feature that relies on a recent CDP command can
still be missing from the older protocol build the client was written against.

## Connect after the engine is running

The endpoint accepts connections once the engine has started. The examples
connect from a window `Load` handler or right after the first
`Navigation.LoadUrl` call. That ordering happens to work, but nothing
guarantees it, so retry rather than treating the first failure as fatal. The
examples only log a failed attempt, to keep the code focused on the connection
itself.

CDP calls are asynchronous and run off the UI thread. When a result has to
reach the user interface, marshal it back the way your framework requires.
Dispose the `IBrowser` and `IEngine` instances when the window closes.

## Off-screen rendering

`RemoteDebuggingPort` is an engine option and does not depend on the rendering
mode. An engine created with `RenderingMode.OffScreen` exposes the endpoint in
the same way, so a test host can drive a page with no window on screen. The
code is the same; the only difference is that there is no `BrowserView` in
which to watch the scenario run.

## Tutorials for each tool

Each tutorial covers one tool: the package to reference, the code that
attaches to the engine, and the failure modes specific to that tool.

* [Selenium](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/selenium/) — attach a WebDriver
  session through ChromeDriver.
* [Playwright](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/playwright/) — connect Playwright
  for .NET over CDP.
* [Puppeteer](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/puppeteer/) — connect Puppeteer Sharp
  to a running engine.
* [MCP servers](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/mcp-servers/) — let an AI agent
  work with the page through Playwright MCP or Chrome DevTools MCP.

The complete projects are available in our repository:
[C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/csharp/devtools-protocol),
[VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/vbnet/devtools-protocol).
