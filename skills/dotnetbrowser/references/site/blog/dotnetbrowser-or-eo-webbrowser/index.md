# DotNetBrowser or EO.WebBrowser

Do you need a web view control for a .NET app? Well, you are in luck. The .NET
ecosystem has plenty to offer. There are free web view controls, both
open-source and proprietary. And there are commercial web views — an option
often chosen by businesses.

In this blog post, we compare the commercial solutions: DotNetBrowser 
and EO.WebBrowser.

For comparisons with free solutions, check out the following blog posts:

* [DotNetBrowser vs WebView2][webview-article]
* [DotNetBrowser vs CefSharp][cefsharp-article]

## In a nutshell

<div class="table-wrapper comparison-table">

|                                       | EO.WebBrowser | DotNetBrowser                         |
|:--------------------------------------|:--------------|:--------------------------------------|
| Chromium security upgrades (per year) | 3             | 12                                    |
| Supported UI frameworks               | WinForms, WPF | Avalonia, WinForms, WinUI 3, WPF |
| Operating systems                     | Windows-only  | Windows, macOS, Linux                 |
| LGPL compliance                       | Undisclosed   | [LGPL compliance page][lgpl]          |
| Open source components                | Undisclosed   | [The list of OSS components][oss]     |

</div>

## Frequency of Chromium upgrades

DotNetBrowser and EO.WebBrowser both use Chromium under the hood and bundle the
browser engine inside the distribution. This way, Chromium becomes a part of
your application, which makes you responsible for delivering Chromium updates to
the users. And you can update Chromium only as often as 
the web view does it.

Why is that important? It's all about security. Researchers regularly find
vulnerabilities of different severity in browsers, and Chromium does a great job
of fixing them in time. That drives a high release cadence: monthly major
releases and biweekly security updates.

DotNetBrowser releases at least **12 times a year**, covering every major 
Chromium update and important minor updates. EO.WebBrowser updates Chromium 
from **2 to 3 times a year** on average. 

## UI frameworks

DotNetBrowser provides a web view control for  [WinForms][winforms], 
[WPF][wpf], [Avalonia UI][avalonia], and [WinUI 3][winui]. 
There's ongoing work on MAUI support.

EO.WebBrowser provides controls for WinForms and WPF only.

## Operating systems

DotNetBrowser works on Windows, macOS, and Linux operating systems. It can be
used alongside Avalonia UI to create applications with the user interface. 
For the headless tasks, DotNetBrowser doesn't require a UI toolkit and 
can be used as-is [on a Linux server][headless] or in a Windows service.

EO.WebBrowser is a Windows-only web view that can work both in the user
interface and headlessly.

## Runtimes

DotNetBrowser officially supports .NET Framework 4.6.2+ and .NET 5-9, 
as described the [system requirements][requirements].

EO.WebBrowser supports .NET Framework 2+ and theoretically .NET 5-9, 
as briefly mentioned on the website.

## Features

DotNetBrowser is based on a fully functional unabridged Chromium build. 
It uses an in-house integration technology that provides most of Chromium 
features to the developers.

EO.WebBrowser uses Chromium Embedded Framework with a proprietary integration
layer. This is a capable solution.

DotNetBrowser and EO.WebBrowser have a similar 
[out-of-process architecture][arch] and generally provide similar features with 
a few noteworthy exceptions.

### Chrome extensions

DotNetBrowser supports Chrome extensions. You can install and fully use most
Chrome extensions manually or programmatically. Extensions give you 
the abilities to use developer tools for JavaScript libraries, improve
accessibility, block ads, and do many other things. You can read more in the 
[Chrome extensions in DotNetBrowser][extensions-article] blog post.

![A Chrome extension opened in DotNetBrowser](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-eo-webbrowser/ublock-in-dotnetbrowser.webp#small)
<p class="image-caption">A Chrome extension opened in DotNetBrowser.</p>

### Overlay on top of web view

DotNetBrowser can render web content in two modes: directly on the surface or to
a lightweight component. Rendering directly to a surface performs well but
suffers from the so-called airspace issue: you can't overlay the web view with
other controls in frameworks like WPF and Avalonia UI.

Rendering to a lightweight component, on the other hand, allows other controls
to appear on top of the web view. This rendering mode is present exclusively 
in DotNetBrowser. You can read about choosing the correct mode in the 
[guide on rendering modes][rendering-modes].

![WPF Canvas rendered on top of DotNetBrowser](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-eo-webbrowser/dotnetbrowser-overlay.webp)
<p class="image-caption">WPF Canvas rendered on top of DotNetBrowser.</p>

## Legal compliance

TeamDev performs regular review of the licenses associated with the Chromium
components used by DotNetBrowser. This is necessary in order to make sure there
are no restrictions on commercial distribution of both DotNetBrowser 
and clients’ products.

This information is public and is always available on TeamDev official website,
so it's possible to check the [list of components][oss] and accompanying 
licenses for each version of Chromium used in DotNetBrowser.

Following the requirements of LGPL, TeamDev has an LGPL compliance procedure in
place to ensure proper use of LGPL components included into DotNetBrowser. For
more details, you can see our [DotNetBrowser Compliance with LGPL page][lgpl].

At the moment of writing, the list of open source components used in
EO.WebBrowser is not available on their website and in the distribution package.
Also, we were not able to locate any public statement regarding LGPL compliance
or compliance procedures.



[avalonia]: https://teamdev.com/dotnetbrowser/docs/quickstart/avalonia/
[wpf]: https://teamdev.com/dotnetbrowser/docs/quickstart/wpf/
[winforms]: https://teamdev.com/dotnetbrowser/docs/quickstart/winforms/
[winui]: https://teamdev.com/dotnetbrowser/docs/quickstart/winui3/
[headless]: https://teamdev.com/dotnetbrowser/docs/guides/headless-linux/
[oss]: https://teamdev.com/dotnetbrowser/docs/guides/licensing/#chromium-open-source-components-licenses
[lgpl]: https://teamdev.com/dotnetbrowser/lgpl-compliance/
[arch]: https://teamdev.com/dotnetbrowser/docs/guides/architecture/#overview
[webview-article]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/
[cefsharp-article]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/
[extensions-article]: https://teamdev.com/dotnetbrowser/blog/chrome-extensions-in-dotnetbrowser/
[rendering-modes]: https://teamdev.com/dotnetbrowser/docs/guides/gs/browser-view/#rendering
[requirements]: https://teamdev.com/dotnetbrowser/docs/guides/requirements/
