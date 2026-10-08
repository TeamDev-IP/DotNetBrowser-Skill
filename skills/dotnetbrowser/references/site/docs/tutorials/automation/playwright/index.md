
# Playwright

**Lead**
Playwright for .NET can attach to the browser your application already embeds.
This tutorial covers the connection code and the limits of CDP mode.


Playwright usually manages its own browser builds. It also supports connecting
to a running Chromium over the Chrome DevTools Protocol, or CDP, which is how
it attaches to DotNetBrowser.

Read [DevTools Protocol](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/) first
for the rules that apply to every automation tool.

## Prerequisites

Reference the `Microsoft.Playwright` NuGet package in the project that runs
the scenario.

Because Playwright attaches to a browser that already exists, you do not need
to run `playwright install`. Its Node-based driver is still required, but the
NuGet package deploys that with the application.

## Enabling the endpoint

Create the engine with `RemoteDebuggingPort` set to a free port, as described
in [DevTools Protocol](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/#opening-the-endpoint).
The example uses `9223`.

## Connecting Playwright

Create a Playwright instance and connect it to the endpoint:


**C#**

```csharp
using IPlaywright playwright = await Microsoft.Playwright.Playwright.CreateAsync();

// Connect to the browser using CDP
Microsoft.Playwright.IBrowser playwrightBrowser =
    await playwright.Chromium
                    .ConnectOverCDPAsync($"http://localhost:{RemoteDebuggingPort}");

IBrowserContext browserContext = playwrightBrowser.Contexts[0];
await browserContext.GrantPermissionsAsync(new[] { "geolocation" });
await browserContext.SetGeolocationAsync(new Geolocation
{
    Latitude = 42.746635f,
    Longitude = -75.770045f
});

IPage page = browserContext.Pages[0];
await page.GotoAsync(LocationUrl);
await page.WaitForSelectorAsync("title");

// Scroll the map into view
await page.Locator("#map").ScrollIntoViewIfNeededAsync();
```

**VB**

```vb
Using _
    playwright As IPlaywright =
        Await Microsoft.Playwright.Playwright.CreateAsync()
    ' Connect to the browser using CDP
    Dim playwrightBrowser As IBrowser =
            Await _
            playwright.Chromium.ConnectOverCDPAsync(
                $"http://localhost:{RemoteDebuggingPort}")

    Dim browserContext As IBrowserContext = playwrightBrowser.Contexts(0)
    Await browserContext.GrantPermissionsAsync({"geolocation"})
    Await browserContext.SetGeolocationAsync(New Geolocation With {
                                                .Latitude = 42.746635F,
                                                .Longitude = - 75.770045F
                                                })

    Dim page As IPage = browserContext.Pages(0)
    Await page.GotoAsync(LocationUrl)
    Await page.WaitForSelectorAsync("title")

    ' Scroll the map into view
    Await page.Locator("#map").ScrollIntoViewIfNeededAsync()
End Using
```



`ConnectOverCDPAsync` takes the endpoint URL, `http://localhost:9223` here,
and returns a browser object backed by the running engine.

The example then takes `Contexts[0]` and `Pages[0]` rather than creating a
context or a page. Those are the context and the page your application already
displays, so everything the scenario does is visible in the `BrowserView`
control.

## What CDP mode covers

The Playwright documentation describes a CDP connection as lower fidelity than
Playwright's own protocol. Page-level automation works as usual, with two
limits:

* Playwright normally launches Chromium with a fixed set of command-line
  switches and expects them to be in effect. DotNetBrowser starts Chromium
  with a different set, so a Playwright feature that relies on one of those
  switches can behave differently here. The
  [Playwright documentation](https://playwright.dev/dotnet/docs/api/class-browsertype#browser-type-connect-over-cdp)
  covers this.
* Anything that assumes Playwright owns the browser process — closing the
  browser, launch options, and the tooling built on them — does not apply.

To have an AI agent work with the page instead of test code, connect
Playwright MCP to the same endpoint. The
[MCP servers](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/mcp-servers/) tutorial covers the
configuration and the limits specific to agents.

## Threading and lifetime

The example connects after the first `Navigation.LoadUrl` call completes, so
the engine is running by the time Playwright attaches. Playwright calls are
asynchronous and run off the UI thread; marshal results back before touching
controls.

## The IBrowser name collision

Both libraries define an `IBrowser` interface. In C#, the example resolves
this with an alias:

```csharp
using IBrowser = DotNetBrowser.Browser.IBrowser;
```

`Microsoft.Playwright.IBrowser` is then written out in full where it is
needed. The VB.NET example qualifies the DotNetBrowser type instead, as
`DotNetBrowser.Browser.IBrowser`.

The complete example is available in our repository:
[C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/csharp/devtools-protocol/Playwright),
[VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/vbnet/devtools-protocol/Playwright).
