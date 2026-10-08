
# Puppeteer

**Lead**
Puppeteer Sharp speaks the DevTools Protocol natively, so it can drive the
browser your application already embeds. This tutorial covers the connection
code and what the connection does not cover.


Puppeteer Sharp is the .NET port of Puppeteer. It speaks the Chrome DevTools
Protocol, or CDP, natively, so it connects to DotNetBrowser with nothing more
than the endpoint URL.

Read [DevTools Protocol](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/) first
for the rules that apply to every automation tool.

## Prerequisites

Reference the `PuppeteerSharp` NuGet package in the project that runs the
scenario.

Puppeteer Sharp can download a Chromium build through `BrowserFetcher`. That
step is unnecessary here, because the browser it drives is the one your
application already runs.

## Enabling the endpoint

Create the engine with `RemoteDebuggingPort` set to a free port, as described
in [DevTools Protocol](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/#opening-the-endpoint).
The example uses `9223`.

## Connecting Puppeteer

Point `ConnectOptions.BrowserURL` at the endpoint:


**C#**

```csharp
ConnectOptions options = new ConnectOptions
{
    BrowserURL = $"http://127.0.0.1:{RemoteDebuggingPort}",
};
```

**VB**

```vb
Dim options As New ConnectOptions With {
        .BrowserURL = $"http://127.0.0.1:{RemoteDebuggingPort}"
        }
```



Then pass those options to `Puppeteer.ConnectAsync` and work with the page
that is already open:


**C#**

```csharp
PuppeteerSharp.IBrowser browser =
    await PuppeteerSharp.Puppeteer.ConnectAsync(options);

await browser.DefaultContext.OverridePermissionsAsync(LocationUrl, new[]
{
    OverridePermission.Geolocation
});

IPage page = (await browser.PagesAsync()).FirstOrDefault();
await page.GoToAsync(LocationUrl);
await page.WaitForSelectorAsync("title");

await page.SetGeolocationAsync(new GeolocationOption
{
    Latitude = 42.746635M, Longitude = -75.770045M
});
await (await page.QuerySelectorAsync("#map")).ScrollIntoViewAsync();
```

**VB**

```vb
Dim puppeteerBrowser As IBrowser =
        Await PuppeteerSharp.Puppeteer.ConnectAsync(options)

Await puppeteerBrowser.DefaultContext.OverridePermissionsAsync(
    LocationUrl,
    New OverridePermission() {OverridePermission.Geolocation}
    )

Dim page As IPage = (Await puppeteerBrowser.PagesAsync()).FirstOrDefault()
Await page.GoToAsync(LocationUrl)
Await page.WaitForSelectorAsync("title")

Await page.SetGeolocationAsync(New GeolocationOption With {
                                  .Latitude = 42.746635D,
                                  .Longitude = - 75.770045D
                                  })
Await (Await page.QuerySelectorAsync("#map")).ScrollIntoViewAsync()
```



`ConnectAsync` attaches to the running engine and returns a browser object.
`PagesAsync` returns the pages open in the engine; the example takes the
first, which is the one shown in the `BrowserView` control.

## What the connection does not cover

Puppeteer does not own this browser process, so the parts of its API that
assume ownership do not apply. DotNetBrowser does not support `NewPageAsync`,
because browsers are created in other ways: your application creates them
with `IEngine.CreateBrowser`, and a page opens
[pop-ups](https://teamdev.com/dotnetbrowser/docs/guides/gs/popups/). The launch options that configure a browser
Puppeteer starts itself have nothing to act on either.

## Threading and lifetime

The example starts the connection right after `Navigation.LoadUrl`, on a
background task, so the engine is running by the time Puppeteer attaches.
Puppeteer calls are asynchronous and run off the UI thread; marshal results
back before touching controls.

## The IBrowser name collision

Both libraries define an `IBrowser` interface. In C#, the example resolves
this with an alias:

```csharp
using IBrowser = DotNetBrowser.Browser.IBrowser;
```

`PuppeteerSharp.IBrowser` is then written out in full where it is needed. The
VB.NET example qualifies the DotNetBrowser type instead, as
`DotNetBrowser.Browser.IBrowser`.

The complete example is available in our repository:
[C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/csharp/devtools-protocol/Puppeteer),
[VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/vbnet/devtools-protocol/Puppeteer).
