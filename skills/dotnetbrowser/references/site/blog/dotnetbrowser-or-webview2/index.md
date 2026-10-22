# DotNetBrowser or WebView2

When it comes to embedded browsers, the industry offers all kinds of solutions:
free and commercial, open-source and proprietary. They differ in what they can 
do, how to use them, and the additional services that come along. In this 
article, we help you choose the right one.

In the [DotNetBrowser or CefSharp][dotnetbrowser-vs-cefsharp-article] article, 
we took open-source CefSharp, compared it with DotNetBrowser, and explained how 
to choose.

Today, we explore proprietary WebView2 and argue that DotNetBrowser is a better 
fit for commercial use. We start with the organizational and legal aspects. 
After that, we cover the functional differences.

Migrating to DotNetBrowser is straightforward. Check out the detailed
[migration guide][migration-guide] that walks you through the process and the
most important things you need to know.

## In a nutshell


<div class="table-wrapper comparison-table">

|                              | <img class="product-logo" src="/dotnetbrowser/blog/dotnetbrowser-or-webview2/edge-logo.svg" alt="WebView2 logo" width="22" height="22"/> WebView2 | <img class="product-logo" src="/images/product-logos/dotnetbrowser.svg" alt="DotNetBrowser logo" width="22" height="22"/> DotNetBrowser |
|:-----------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| License                      | Proprietary                                                                                                                                  | Commercial                                                                                                                              |
| Supported OS                 | Windows-only                                                                                                                                 | Windows, macOS, Linux                                                                                                                   |
| Supported UI toolkits        | WinForms, WPF, WinUI 3, MAUI                                                                                                                 | WinForms, WPF, WinUI 3, Avalonia                                                                                                        |
| [Data collection][privacy]   | Yes                                                                                                                                          | No                                                                                                                                      |
| Headless mode                | No                                                                                                                                           | Yes, works in the console or as a service                                                                                               |
| [Technical support][support] | Public GitHub repository                                                                                                                     | Yes, confidential, with SLA                                                                                                             |

</div>

DotNetBrowser and WebView2 are mature solutions from commercial companies with 
considerable experience in this area. So you get a software solution that works 
and doesn't depend on the open-source community.

Choose WebView2 when:

* You have to use free software.
* You want to use the perks of the evergreen distribution.
* You don't mind sharing the end user's data with Microsoft.

Choose DotNetBrowser when:

* You need a custom feature.
* You want to get assistance with product use.
* You want to report issues confidentially and have them fixed.
* You want to have control over the end user's data collection.
* You need to run the application without UI.
* You need to run on Linux and macOS.
* You need WPF controls over the browser while it plays DRM-protected video.
* You need to handle `window.print()` from the page or read printer
  capabilities.
* You need to intercept traffic on background threads, not on the UI thread.

## Difference in approaches

WebView2 is a control from Microsoft. It's free, but — as one expects from
Microsoft — it's also proprietary. It comes as a replacement for a Trident-based
WebView and uses Edge instead.

WebView2 is a control: an item in the Visual Studio toolbox, classes from the
`Microsoft.Web.WebView2.Core.dll` file. But it is not a standalone Microsoft
product like Office or Power BI. Microsoft's public channel for questions and
bug reports is a GitHub repository, with no guaranteed response time.

DotNetBrowser is a product created and developed by TeamDev, a company
specializing in browser embedding. We started with Internet Explorer in 2004 and
continued with Safari and WebKit later — before eventually settling down to
Chromium in 2013.

In 2015, we introduced DotNetBrowser. It is a commercial product designed for
commercial use. Besides the software and documentation, the offer includes a
dedicated Customer Care specialist, [technical support][getting-help], 
and [premium services][premium-services].

## Difference for business

### Fixes, features, and assistance

How do you get help if you find a bug or need a feature? Let's take a closer
look at what WebView2 and DotNetBrowser have to offer.

WebView2 gathers feedback from the public in a dedicated GitHub repository. When 
you have a report to make, you create an issue there. If Microsoft developers 
find your report worthy, they transfer it to their internal system. You will 
know by the "tracked" label they use for such issues.

DotNetBrowser has a private helpdesk system where reports from clients remain 
confidential. The guaranteed first response time, or SLA, is one business day.

The technical support includes: help with product use, assistance with 
troubleshooting, bug fixing, and considering feature requests. All your support 
requests will be processed by DotNetBrowser software engineers.

### Privacy of end users

The WebView2 Runtime that end users install comes with its own license terms.
They appear when you click a download button on Microsoft's [WebView2
page][webview2-download]. Two things may concern you:

 1. Microsoft may collect information about your end users.
 2. With the default settings, you're required to warn them about it.

Section 3(a) of the license states that the software may collect information
about you and your end users' use of the software and send it to Microsoft.
Your use of the software is your consent to this.

Section 3(b) says that Microsoft Defender SmartScreen is enabled by default. If
you leave it on, Section 9(a) obliges you to notify your users that your
software includes SmartScreen and sends their information to Microsoft. You turn
it off with the `IsReputationCheckingRequired` setting.

If you ship the Runtime with your application (the fixed version), the same
clauses are sections 4(a), 4(b), and 8 of its terms. Microsoft describes what
WebView2 collects on its [data privacy page][webview2-privacy].

DotNetBrowser does not collect information about you and your end users.
Furthermore, it prevents data collection by Google. Read more about how
DotNetBrowser handles data and gives you control over privacy in the [Privacy
Practices][privacy-practices].

## Technical differences

From a technical standpoint, DotNetBrowser and WebView2 are not that different.
Both have a similar architecture where Chromium runs in a separate process. Both
have hundreds of features, most of which overlap.

The differences, however, exist. And they can be essential when choosing the
solution that fits your case. This comparison describes WebView2 as of
[SDK 1.0.4258.31][webview2-sdk] (September 2026). Let's take a look.

### Distribution and deployment

You may bring WebView2 Runtime with your application or use the one installed at
the end user's. These are distribution modes: the fixed version and the
evergreen, respectively.

With the fixed version mode, you control the version of WebView2 in your
application, which is good for stability. While in the evergreen mode, you let
Microsoft take care of the logistics and updates and reduce the size of your
software.

DotNetBrowser needs to be packaged with your application. It is the only
distribution mode that comes out of the box.

### Chrome extensions

Both DotNetBrowser and WebView2 support extensions. While WebView2 
provides very basic functionality, DotNetBrowser gives developers more options
and full control over the extension lifecycle and activity.

Since [SDK 1.0.2210.55][webview2-sdk-extensions] (December 2023), a WebView2
developer can [install an extension][webview2-extensions] from an unpacked
folder, list the installed extensions, enable or disable them, and remove them.
You can't install from the Chrome Web Store, and there is no API for the
extension's icon, badge, or pop-up.

In DotNetBrowser, a developer can install an extension directly from the CRX 
file, programmatically "click" on the extension icon, interact with a pop-up and 
new "tabs" the extension may open. 

Also, you can let users interact with extensions directly:

* Enable using Chrome Web Store.
* Display the extension icon, with badges and labels.
* Show pop-ups and "tabs" created by the extension.

Read more in the [guide on extensions][extensions-guide]
and [try it in practice][extensions-article].

### Running without UI

For use cases such as automation or generating PDF reports, it's unnecessary to
have a user interface. Instead, it's simpler and more efficient to run headless.

WebView2 has no headless mode. It needs a window, which can be hidden, and a UI
thread with a message loop, even in a console app. Microsoft doesn't officially
support WebView2 in a [Windows service][webview2-service]. Rendering without a
window, [off-screen rendering][webview2-osr], is still an open feature request.

DotNetBrowser runs headless out of the box. You can use it in the console
application, on the web server, or even as a Windows service. Just like this:

```cs
using (IEngine engine = EngineFactory.Create())
{
    using (IBrowser browser = engine.CreateBrowser())
    {
        browser.Navigation.LoadUrl("https://teamdev.com/dotnetbrowser").Wait();
    }
}
```

### Linux and macOS

In 2024, Microsoft officially rejected the plans to support
[macOS][webview2-macos] and [Linux][webview2-linux] in WebView2.

DotNetBrowser is a cross-platform library that runs on Windows, macOS, 
and Linux. Use it with 
[Avalonia UI][avalonia] or [in the server application][console].

### WPF and overlapping Controls

Both WebView2 and DotNetBrowser can put WPF elements on top of the browser.
WebView2 does it with a second WPF control. DotNetBrowser does it with a
rendering mode that works in every UI toolkit it supports.

The standard WebView2 control can't put WPF elements on top of the browser. It
embeds a foreign window, and WPF doesn't support overlapping between regions
rendered in different windows. Elements placed over the browser stay hidden.

In [SDK 1.0.2957.106][webview2-sdk-composition] (January 2025), WebView2 added
[`WebView2CompositionControl`][webview2-composition], a drop-in replacement for
the standard control that lets WPF elements draw on top of the browser. Read
more in [WebView2 in WPF apps][webview2-wpf].

WebView2's composition control doesn't embed a window. It captures the browser's
output as images with a Windows graphics-capture session and draws them itself.
Microsoft names two costs: frame rates can be lower than with the standard
control, and DRM-protected video doesn't display.

Outside WPF, WebView2 has no such control. In WinForms, it isn't needed: a
button or any other opaque control draws over WebView2 and DotNetBrowser alike.
A transparent control is another story. In both, it shows the form behind it,
not the page.

Win32 apps can use WebView2's visual hosting mode and compose the browser into
their own UI. In WinUI 3, WebView2 is [external content][winui-visual-layer].
XAML elements can sit on top of it, but nothing behind it shows through, so the
browser background can't be transparent.

DotNetBrowser has two [rendering modes][browser-view-rendering]. In the
off-screen rendering mode, the rendered pixels are copied to the .NET process
memory and drawn by a regular control. So WPF, WinForms, WinUI 3, and Avalonia
controls can overlap the browser. In this mode, DRM-protected video (Widevine)
plays and stays visible, as the screenshot below shows.

In DotNetBrowser, off-screen rendering lowers the frame rate too. The other
mode, hardware-accelerated, embeds a native window, so it has the same overlap
limit as WebView2's standard control.

![A WPF control bar on top of a Widevine-protected video in DotNetBrowser's off-screen rendering mode](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/wpf-controls-over-drm-video.webp)
<p class="image-caption">WPF controls on top of a Widevine-protected video in the off-screen rendering mode. Sintel &copy; Blender Foundation | <a href="https://durian.blender.org/">durian.blender.org</a>, <a href="https://creativecommons.org/licenses/by/3.0/">CC BY 3.0</a>.</p>

### Calling JavaScript from .NET

In both solutions, you can execute JavaScript right from the .NET code. The 
difference is in what happens when the result travels back from Chromium to the 
.NET world.

WebView2 converts the result to JSON:

```cs
string result = await coreWebView2.ExecuteScriptAsync(@"'example'");
Debug.Assert(result == "\"example\"");
```

Since [SDK 1.0.2277.86][webview2-sdk-script] (February 2024), WebView2's
`ExecuteScriptWithResultAsync` can return the result as a plain string instead
of JSON and report script exceptions. It still can't return a reference to a
JavaScript object.

DotNetBrowser automatically [converts][js-to-net] simple types. It replaces 
the complex types with proxies to actual V8 objects:

```cs
string title = await browser.MainFrame.ExecuteJavaScript<string>("document.title");
IJsObject window = await browser.MainFrame.ExecuteJavaScript<IJsObject>("window");

// Or just use dynamic types.
dynamic document = browser.MainFrame.ExecuteJavaScript("document").Result;
document.write("Hello world!");
```

### Calling .NET from JavaScript

Both solutions allow using .NET objects from within JavaScript, but each with a
catch.

In WebView2, the object reaches JavaScript through COM, so it only works for
types that COM can handle. A plain class, an array, or a WPF button works, but
adding a `List<string>` or a WinForms button throws an exception. WebView2 also
lets the page and the app exchange web messages, but a message carries a string
or JSON: JavaScript gets a copy of the data, not an object it can call.

In DotNetBrowser, you can [inject any object][javascript], including the
`List<string>` and the WinForms button that WebView2 rejected. In JavaScript,
you will have access to the injected object's public members and indexed
properties. Calls from JavaScript run on background threads, so code that
touches a UI control has to switch to the UI thread: `Dispatcher` in WPF,
`Invoke` in WinForms.

### Intercepting traffic

Both WebView2 and DotNetBrowser intercept traffic. WebView2 does it on the UI
thread. DotNetBrowser does it on background threads.

WebView2 has the [`WebResourceRequested`][webview2-intercept] event. In its
handler, you can change the request's URL, method, headers, or body, or return
your own response. Source maps for the content you return are not loaded. The
`WebResourceResponseReceived` event lets you inspect, but not change, the
response.

`WebResourceRequested` fires only for requests that match a filter you register:
a URL pattern and a resource type. Since [SDK 1.0.2365.46][webview2-sdk-filter]
(February 2024), a filter can also catch requests from service workers, shared
workers, and cross-origin iframes. The older two-argument
[filter][webview2-filter] overload is deprecated because it misses those
iframes.

WebView2 raises this event on the app's [UI thread][webview2-local-content]. A
handler that blocks for three seconds freezes the window and delays the page
load for three seconds. The handler can call `GetDeferral()` and finish the work
in async code, but the request still waits until you complete the deferral.

DotNetBrowser has a handler for each step of a request, plus events for the
response. With them, you can:

* [Filter HTTP requests][navigation-filtering].
* [Redirect HTTP requests][before-url-request].
* Override the HTTP [request][before-start-transaction]
  and [response][receive-headers] headers.
* [Override request upload data][before-upload].
* [Filter cookies][suppress-cookies].
* Authenticate requests.
* Verify certificates.
* Get events for the response start, received bytes, and completion.

To return your own responses in DotNetBrowser, you register a [handler per
scheme][engine-scheme], including `https`, when you create the engine. Every
request of that scheme reaches it, so there is no filter list to maintain.

You can find more examples of networking in DotNetBrowser in our
[GitHub][examples-network].

### Printing API

Both WebView2 and DotNetBrowser have a printing API. The difference is who is in
charge when the page calls `window.print()`.

Since [SDK 1.0.1518.46][webview2-sdk-print] (January 2023), WebView2 prints to a
named printer with [`PrintAsync`][webview2-print] and
[`CoreWebView2PrintSettings`][webview2-print-settings]. It also prints to PDF,
to a file or a stream. The settings cover the printer name, page ranges, copies,
duplex, collation, color mode, media size, pages per side, margins, header, and
footer. `ShowPrintUI` opens WebView2's print preview or the system print dialog.

What WebView2 lacks is an API to read a printer's capabilities, such as paper
sizes or duplex. You query the system yourself.

When the page's JavaScript calls `window.print()`, WebView2 opens its preview,
and there is no event to intercept it. One workaround is to replace
`window.print` with your own function that sends a message to the app.

In DotNetBrowser, `RequestPrintHandler` receives print requests from both .NET
and JavaScript. In this handler, you decide whether to cancel the request, show
the print preview, or print silently.

If you choose to print, `PrintHtmlContentHandler` or `PrintPdfContentHandler`
runs next, depending on the content. In it, you can:

* Choose a printer.
* Read the printer's capabilities: paper sizes, color models, duplex modes, and
  copies.
* Configure page ranges, paper size, margins, headers, and footers.

DotNetBrowser also has a built-in PDF printer. Read more in the
[printing guide][printing].

## Try for free

Get your free license and choose one of our getting started guides. 



It takes 5 minutes to start using DotNetBrowser:

* [DotNetBrowser in WPF][wpf]
* [DotNetBrowser in Avalonia][avalonia]
* [DotNetBrowser in WinForms][winforms]
* [DotNetBrowser in the console][console], useful for Windows services and 
  server applications.

[extensions-article]: https://teamdev.com/dotnetbrowser/blog/chrome-extensions-in-dotnetbrowser/
[extensions-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/extensions/
[dotnetbrowser-vs-cefsharp-article]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/
[privacy]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/#privacy-of-end-users
[support]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/#fixes-features-and-assistance
[migration-guide]: https://teamdev.com/dotnetbrowser/blog/from-webview2-to-dotnetbrowser-part-1/
[getting-help]: https://teamdev.com/dotnetbrowser/#getting-help
[premium-services]: https://teamdev.com/dotnetbrowser/#getting-help
[privacy-practices]: https://teamdev.com/dotnetbrowser/docs/guides/privacy/
[js-to-net]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/#javascript-to-net
[javascript]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/
[navigation-filtering]: https://teamdev.com/dotnetbrowser/docs/guides/gs/navigation/#filtering-resources
[before-url-request]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-url-request
[before-start-transaction]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-start-transaction
[receive-headers]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#receive-headers
[before-upload]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-send-upload-data
[suppress-cookies]: https://teamdev.com/dotnetbrowser/docs/guides/gs/cookies/#suppressing-cookies
[examples-network]: https://github.com/TeamDev-IP/DotNetBrowser-Examples#network
[wpf]: https://teamdev.com/dotnetbrowser/docs/quickstart/wpf/
[avalonia]: https://teamdev.com/dotnetbrowser/docs/quickstart/avalonia/
[winforms]: https://teamdev.com/dotnetbrowser/docs/quickstart/winforms/
[console]: https://teamdev.com/dotnetbrowser/docs/quickstart/console/
[webview2-download]: https://developer.microsoft.com/microsoft-edge/webview2/
[webview2-privacy]: https://learn.microsoft.com/microsoft-edge/webview2/concepts/data-privacy
[webview2-sdk]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-4258-31
[webview2-extensions]: https://learn.microsoft.com/dotnet/api/microsoft.web.webview2.core.corewebview2profile.addbrowserextensionasync
[webview2-sdk-extensions]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-2210-55
[webview2-service]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/3458
[webview2-osr]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/547
[webview2-macos]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/1314
[webview2-linux]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/645
[webview2-composition]: https://learn.microsoft.com/dotnet/api/microsoft.web.webview2.wpf.webview2compositioncontrol
[webview2-wpf]: https://learn.microsoft.com/microsoft-edge/webview2/platforms/wpf
[winui-visual-layer]: https://learn.microsoft.com/windows/apps/develop/composition/visual-layer#differences-from-uwp
[browser-view-rendering]: https://teamdev.com/dotnetbrowser/docs/guides/gs/browser-view/#rendering
[webview2-intercept]: https://learn.microsoft.com/microsoft-edge/webview2/how-to/webresourcerequested
[webview2-filter]: https://learn.microsoft.com/dotnet/api/microsoft.web.webview2.core.corewebview2.addwebresourcerequestedfilter
[webview2-local-content]: https://learn.microsoft.com/microsoft-edge/webview2/concepts/working-with-local-content
[engine-scheme]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#intercept-request-per-uri-scheme
[webview2-print]: https://learn.microsoft.com/microsoft-edge/webview2/how-to/print
[webview2-sdk-print]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-1518-46
[webview2-sdk-script]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-2277-86
[webview2-sdk-filter]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-2365-46
[webview2-sdk-composition]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-2957-106
[webview2-print-settings]: https://learn.microsoft.com/dotnet/api/microsoft.web.webview2.core.corewebview2printsettings
[printing]: https://teamdev.com/dotnetbrowser/docs/guides/gs/printing/
