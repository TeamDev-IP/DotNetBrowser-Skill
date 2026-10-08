# DotNetBrowser or CefSharp

When selecting the browser component for WPF or WinForms applications, 
[DotNetBrowser](https://teamdev.com/dotnetbrowser?utm_campaign=dotnetbrowser-vs-cefsharp&utm_medium=article&utm_source=product-blog) 
and CefSharp are among the obvious choices.

In this article, we explain the difference between DotNetBrowser and CefSharp
and how to choose between them.

## In a nutshell

<div class="table-wrapper comparison-table">

|                                          | <img src="/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/cef-logo.svg" alt="CEF logo" width="28" height="28"/> CefSharp | <img class="product-logo" src="/images/product-logos/dotnetbrowser.svg" alt="DotNetBrowser logo" width="22" height="22"/> DotNetBrowser |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| License                                  | Open-source                                                                                                            | Commercial                                                                                                                              |
| Supported OS                             | Windows-only                                                                                                           | Windows, macOS, Linux                                                                                                                   |
| Supported UI toolkits                    | WinForms, WPF                                                                                                          | WinForms, WPF, Avalonia, Win UI 3                                                                                                       |
| [Process memory isolation][architecture] | No                                                                                                                     | Yes                                                                                                                                     |
| Releases (per year)                      | 19                                                                                                                     | 12                                                                                                                                      |
| [Technical support][support]             | No                                                                                                                     | Yes, confidential, with SLA.                                                                                                            |

</div>

Choose open-source CefSharp when:

* You have to use free software.

Choose commercial DotNetBrowser when:

* You need a custom feature.
* You want to get assistance with product use.
* You want to report issues confidentially and have them fixed.
* You need to run on Linux and macOS.
* You need to embed a browser into Office applications.
* You have requirements for software security.

## Linux and macOS

DotNetBrowser runs natively on Linux and macOS, both on x86-64 and ARM 
platforms.

DotNetBrowser supports Avalonia UI framework and can be used in [Blazor Hybrid
applications][blazor-hybrid].

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

CefSharp starts the Chromium engine inside the .NET process. 
The library requires the engine to be started and shutdown in the main 
application thread and only once in the process lifetime.

DotNetBrowser starts the Chromium engine as a separate process. 
There is no requirement to do this on the main UI thread — even the 
worker thread will do. You can start and shutdown Chromium anytime. You can use 
several Chromium engines simultaneously. 

![DotNetBrowser architecture](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/dotnetbrowser-architecture.webp#small)
<p class="image-caption">DotNetBrowser architecture</p>

![CefSharp architecture](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/cefsharp-architecture.webp)
<p class="image-caption">CefSharp architecture</p>

### Stability and security

The CefSharp model allows you to start the application faster, but it has major 
drawbacks:
 
 * CefSharp doesn't support the built-in Chromium sandbox.
 * CefSharp consumes the memory and CPU of the .NET process.
 * If CefSharp crashes, the whole application crashes too.
 * The .NET process becomes susceptible to security vulnerabilities in Chromium, 
   as they use the same address space.

In DotNetBrowser, an error inside Chromium doesn't lead to a crash in your 
.NET application. Instead, you can detect and handle the crash appropriately:

```cs
engine.Disposed += (s, e) => 
{
    long exitCode = e.ExitCode;
    // If the exit code is non-zere, the engine crashed.
};
```

## Distribution and deployment

CefSharp requires the Microsoft Visual C++ Runtime to be installed in the 
environment.

DotNetBrowser comes with all required Chromium binaries and DLLs already 
packaged. You don't need to pre-install Microsoft Visual C++ Runtime to work 
with DotNetBrowser.

## Embedding into Office

DotNetBrowser works in non-default AppDomains and thus can be embedded into 
Office applications using VSTO add-ins or Excel-DNA.

CefSharp works only in the default AppDomain.

## Proprietary codecs

Proprietary codes work in DotNetBrowser out of the box. They're disabled by 
default, but you can enable them in the code:

```cs
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    ProprietaryFeatures = ProprietaryFeatures.H264 | ProprietaryFeatures.Aac
}.Build());
```

CefSharp is distributed without proprietary codec supports.

## High DPI

In CefSharp, the default DPI awareness for the browser subprocess is 
Per-Monitor. This requires the whole application to be DPI aware, which may be 
an issue for older software.

DotNetBrowser automatically detects DPI awareness of the .NET process and 
complies with it.

## DOM access

In CefSharp, the only way to access DOM is to use JavaScript. DotNetBrowser 
provides API for manipulating DOM directly your code:

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
and allow you to use extension actions.

Read more in the [guide on extensions][extensions-guide] 
and [try it in practice][extensions-article]. 

![uBlock extension in DotNetBrowser](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/ublock-in-dotnetbrowser.webp#small)
<p class="image-caption">An extension launched in DotNetBrowser</p>

CefSharp has a very limited support for extensions.

## Support and updates

CefSharp is an open-source project. If you see a bug or need a feature, you can
file a report or contribute. In 2024, the project had 19 major and minor
releases.

DotNetBrowser is a commercial product designed and created for commercial
companies. In 2024, the project has 12 major releases with Chromium upgrades.

We have a private helpdesk system where reports from clients remain
confidential. The guaranteed first response time, or SLA, is one business day.

The technical support includes:

* Help with product use.
* Timely bug fixes.
* Assistance with troubleshooting.
* Considering feature requests.

All your support requests will be processed by DotNetBrowser software engineers.

A new version of DotNetBrowser is released almost every month. We upgrade
Chromium to the latest stable version (with the latest security patches and
fixed vulnerabilities) within 3–4 weeks after its official release.

## Try for free



Get your free license and choose one of our getting started guides. It takes 
5 minutes to start using DotNetBrowser:

* [DotNetBrowser in WPF][in-wpf]
* [DotNetBrowser in WinForms][in-winforms]
* [DotNetBrowser in the console][in-console]

[in-wpf]: https://teamdev.com/dotnetbrowser/docs/quickstart/wpf/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[in-winforms]: https://teamdev.com/dotnetbrowser/docs/quickstart/winforms/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[in-console]: https://teamdev.com/dotnetbrowser/docs/quickstart/console/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[blazor-hybrid]: https://teamdev.com/dotnetbrowser/blog/blazor-hybrid-apps-in-avalonia-ui/
[extensions-article]: https://teamdev.com/dotnetbrowser/blog/chrome-extensions-in-dotnetbrowser/
[extensions-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/extensions/
[architecture]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/#architecture
[support]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/#support-and-updates
