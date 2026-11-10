# DotNetBrowser or CefSharp

When selecting a browser component for .NET desktop applications, 
[DotNetBrowser](https://teamdev.com/dotnetbrowser?utm_campaign=dotnetbrowser-vs-cefsharp&utm_medium=article&utm_source=product-blog) 
and CefSharp are among the obvious choices.

In this article, we explain the difference between DotNetBrowser and CefSharp
and how to choose between them. If you already use CefSharp and want to switch,
the [migration guide][migration-guide] walks you through the process.

## In a nutshell

<div class="table-wrapper comparison-table">

|                                          | <img src="/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/cef-logo.svg" alt="CEF logo" width="28" height="28"/> CefSharp | <img class="product-logo" src="/images/product-logos/dotnetbrowser.svg" alt="DotNetBrowser logo" width="22" height="22"/> DotNetBrowser |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| License                                  | Open-source                                                                                                            | Commercial                                                                                                                              |
| Supported OS                             | Windows-only                                                                                                           | Windows, macOS, Linux                                                                                                                   |
| Supported UI toolkits                    | WinForms, WPF                                                                                                          | WinForms, WPF, WinUI 3, Avalonia                                                                                                   |
| Headless mode                            | Yes, with the separate CefSharp.OffScreen package                                                                      | Yes, works in the console or [as a service][blog-windows-service]                                                                       |
| [Process memory isolation][architecture] | Partial: Chromium's main (browser) process runs inside the .NET process                                                | Yes                                                                                                                                     |
| [Days behind Chrome stable][support]     | 14–21                                                                                                                  | 2–7                                                                                                                                     |
| [Technical support][support]             | Community: GitHub issues and discussions                                                                               | Yes, confidential, with SLA                                                                                                             |

</div>

Choose open-source CefSharp when:

* You have to use free software.
* Your app runs only on Windows, and community support is enough for you.

Choose commercial DotNetBrowser when:

* You need a custom feature.
* You want to get assistance with product use.
* You want to report issues confidentially and have them fixed.
* You need to run on Linux and macOS.
* You need to embed a browser into Office applications.
* You need the Chromium sandbox, Chromium outside your .NET process, and
  security fixes within days of each Chrome release.

## Linux and macOS

DotNetBrowser runs natively on Linux and macOS, both on x64 and ARM64. On
Windows, it runs on x86, x64, and ARM64.

DotNetBrowser supports Avalonia UI, including Avalonia 12, and can be used in
[Blazor Hybrid applications][blazor-hybrid].

CefSharp runs only on Windows, on x86, x64, and ARM64.

![DotNetBrowser on macOS in Avalonia](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/macos.webp)
<p class="image-caption">DotNetBrowser with Avalonia on macOS</p>

![DotNetBrowser on Linux in Avalonia](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/linux.webp)
<p class="image-caption">DotNetBrowser with Avalonia on Linux</p>

## Architecture

CefSharp is a .NET wrapper around the Chromium Embedded Framework or CEF.
The wrapping is done via C++/CLI.

DotNetBrowser doesn't use CEF or C++/CLI under the hood. Instead, it brings its
own approach to integrating with Chromium directly.

### In-process vs. out-of-process 

Chromium runs as several processes, and the main one, the browser process,
manages the rest.

CefSharp runs the browser process inside your .NET process, and the others as
separate processes. The library requires Chromium to be started and shut down in
the main application thread and only once in the process lifetime.

DotNetBrowser starts all Chromium processes, including the browser process,
outside your .NET process, as one Chromium engine. You can start the engine on
any thread, including a worker thread, shut it down anytime, and run several
engines at once.

![DotNetBrowser architecture](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/dotnetbrowser-architecture.webp#small)
<p class="image-caption">DotNetBrowser architecture</p>

![CefSharp architecture](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/cefsharp-architecture.webp)
<p class="image-caption">CefSharp architecture</p>

### Stability and security

Running the browser process inside the .NET process has drawbacks:
 
 * CefSharp doesn't support the Chromium sandbox: all its processes, renderers
   included, run unsandboxed.
 * The browser process consumes the memory and CPU of the .NET process.
 * A crash in the browser process takes the whole application down.
 * The .NET process becomes susceptible to security vulnerabilities in the
   browser process, as they use the same address space.

CefSharp has a separate [CefSharp.OutOfProcess][cefsharp-out-of-process]
project that moves the browser process out, but it isn't published on NuGet.

In DotNetBrowser, the [Chromium sandbox][sandbox] is on by default on Windows,
Linux, and macOS. If Chromium crashes, your .NET application keeps running,
and you can detect and handle the crash:

```cs
engine.Disposed += (s, e) => 
{
    long exitCode = e.ExitCode;
    // The engine has crashed if this exit code is non-zero.
};
```

## Distribution and deployment

CefSharp needs the Microsoft Visual C++ 2022 Runtime, installed on the target
machine or shipped next to your app. It works with .NET Framework 4.6.2 or
later, and its `.NETCore` packages need .NET 6 or later.

DotNetBrowser comes with all required Chromium binaries and DLLs already 
packaged. You don't need to install or ship the Microsoft Visual C++ Runtime
to work with DotNetBrowser. It works with .NET Framework 4.6.2 to 4.8.1 and
.NET 5 to 10. See the [system requirements][requirements].

## Embedding into Office

DotNetBrowser works in non-default AppDomains and thus can be embedded into 
Office applications using VSTO add-ins or Excel-DNA.

CefSharp works only in the default AppDomain.

## Proprietary codecs

DotNetBrowser supports the proprietary H.264, HEVC, and AAC codecs. They're
disabled by default because you need licenses to use them in your product. Once
you have the licenses, enable the codecs in the code:

```cs
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ProprietaryFeatures = ProprietaryFeatures.H264 
                          | ProprietaryFeatures.Hevc 
                          | ProprietaryFeatures.Aac
}.Build());
```

Read more in the [media guide][media-guide].

CefSharp ships without proprietary codecs.

## High DPI

In CefSharp, if your application doesn't declare its DPI awareness,
`Cef.Initialize` makes the whole .NET process Per-Monitor DPI aware. This may
be an issue for older software that isn't ready for it.

DotNetBrowser automatically detects DPI awareness of the .NET process and 
complies with it.

## DOM access

CefSharp has no DOM API of its own. You access the DOM through JavaScript or
the separate [CefSharp.Dom][cefsharp-dom] package, which works over the DevTools
protocol. DotNetBrowser provides an API for manipulating the DOM directly from
your code:

```cs
IDocument document = browser.MainFrame.Document;
document.GetElementById("button").Click();

PointInspection inspection = browser.MainFrame.Inspect(new Point(100, 150));
INode nodeAtPoint = inspection.Node;
```

## Chrome extensions

DotNetBrowser supports Chrome extensions. Developers can install extensions from
CRX files, or let their users use the Chrome Web Store.

DotNetBrowser provides full control over the pop-ups opened by extensions, 
and allows you to use extension actions.

Read more in the [guide on extensions][extensions-guide] 
and [try it in practice][extensions-article]. 

![uBlock extension in DotNetBrowser](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/ublock-in-dotnetbrowser.webp#small)
<p class="image-caption">An extension launched in DotNetBrowser</p>

CefSharp lost its .NET API for extensions in version 128, when CEF dropped the
extension API. You can still load unpacked extensions with Chromium's
`--load-extension` switch, but your code can't list, remove, or control them. In
the WinForms and `Wpf.HwndHost` controls, you can opt in to the Chrome runtime
style, which gives users the `chrome://extensions` page to manage extensions.
The `Wpf` and `OffScreen` controls don't support this style, so they have no
extensions page.

## Support and updates

CefSharp is an open-source project. If you see a bug or need a feature, you can
file a report or contribute. Questions go to GitHub Discussions.

DotNetBrowser is a commercial product designed and created for commercial
companies. We have a private helpdesk system where reports from clients remain
confidential. The guaranteed first response time, or SLA, is one business day.

The technical support includes:

* Help with product use.
* Timely bug fixes.
* Assistance with troubleshooting.
* Considering feature requests.

All your support requests will be processed by DotNetBrowser software engineers.

A new version of DotNetBrowser is released every one to three weeks. Since
September 2026, Chrome has shipped a new major version
[every two weeks][chrome-cadence], and we upgrade Chromium within days of each
release. The table shows how many days after each Chrome release the two
libraries shipped the same Chromium major version, as of November 5, 2026:

| Chromium | Chrome stable | DotNetBrowser       | CefSharp               |
|:---------|:--------------|:--------------------|:-----------------------|
| 150      | June 30       | 4.2.0, 7 days       | 150.0.110, 17 days     |
| 151      | July 28       | 4.2.2, 6 days       | 151.3.170, 19 days     |
| 152      | August 25     | 4.3.0, 3 days       | 152.0.60, 21 days      |
| 153      | September 8   | 4.3.1, 7 days       | No CEF build           |
| 154      | September 22  | 4.3.2, 6 days       | 154.0.340, 20 days     |
| 155      | October 6     | 4.3.3, 2 days       | No CEF build           |
| 156      | October 20    | 4.3.4, 2 days       | 156.0.150, 14 days     |

CefSharp depends on CEF, so it can follow only the Chromium versions that CEF
ships. The dates come from the [Chrome schedule][chrome-schedule], our [release
notes][dotnetbrowser-releases], and CefSharp's first release of each version on
[GitHub][cefsharp-releases] or [NuGet][cefsharp-nuget].

Both projects track Chromium vulnerabilities. CefSharp publishes
[security advisories][cefsharp-advisories] on GitHub, and every DotNetBrowser
release note lists the Chromium security fixes it brings.

## Try for free



Get your free license and choose one of our getting started guides. It takes 
5 minutes to start using DotNetBrowser:

* [DotNetBrowser in WPF][in-wpf]
* [DotNetBrowser in WinForms][in-winforms]
* [DotNetBrowser in Avalonia][in-avalonia]
* [DotNetBrowser in WinUI 3][in-winui3]
* [DotNetBrowser in the console][in-console]

Moving an existing CefSharp app? Follow the [migration guide][migration-guide].

[in-wpf]: https://teamdev.com/dotnetbrowser/docs/quickstart/wpf/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[in-winforms]: https://teamdev.com/dotnetbrowser/docs/quickstart/winforms/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[in-avalonia]: https://teamdev.com/dotnetbrowser/docs/quickstart/avalonia/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[in-winui3]: https://teamdev.com/dotnetbrowser/docs/quickstart/winui3/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[in-console]: https://teamdev.com/dotnetbrowser/docs/quickstart/console/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[blazor-hybrid]: https://teamdev.com/dotnetbrowser/blog/blazor-hybrid-apps-in-avalonia-ui/
[extensions-article]: https://teamdev.com/dotnetbrowser/blog/chrome-extensions-in-dotnetbrowser/
[extensions-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/extensions/
[architecture]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/#architecture
[support]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/#support-and-updates
[migration-guide]: https://teamdev.com/dotnetbrowser/blog/migrating-from-cefsharp-to-dotnetbrowser/
[blog-windows-service]: https://teamdev.com/dotnetbrowser/blog/chromium-in-windows-service/
[sandbox]: https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#sandbox
[requirements]: https://teamdev.com/dotnetbrowser/docs/guides/requirements/
[media-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/media/
[dotnetbrowser-releases]: https://teamdev.com/dotnetbrowser/releases/
[chrome-cadence]: https://developer.chrome.com/blog/chrome-two-week-release
[chrome-schedule]: https://chromiumdash.appspot.com/schedule
[cefsharp-releases]: https://github.com/cefsharp/CefSharp/releases
[cefsharp-nuget]: https://www.nuget.org/packages/CefSharp.Common/#versions-body-tab
[cefsharp-advisories]: https://github.com/cefsharp/CefSharp/security/advisories
[cefsharp-dom]: https://github.com/cefsharp/CefSharp.Dom
[cefsharp-out-of-process]: https://github.com/cefsharp/CefSharp.OutOfProcess
