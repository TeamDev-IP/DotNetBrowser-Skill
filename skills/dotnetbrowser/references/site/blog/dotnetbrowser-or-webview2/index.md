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
[migration guide][migration-guide] that will guide you through this process 
the most important things you need to know.

## In a nutshell


<div class="table-wrapper comparison-table">

|                              | <img class="product-logo" src="/dotnetbrowser/blog/dotnetbrowser-or-webview2/edge-logo.svg" alt="CEF logo" width="22" height="22"/> WebView2 | <img class="product-logo" src="/images/product-logos/dotnetbrowser.svg" alt="DotNetBrowser logo" width="22" height="22"/> DotNetBrowser |
|:-----------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| License                      | Proprietary                                                                                                                                  | Commercial                                                                                                                              |
| Supported OS                 | Windows-only                                                                                                                                 | Windows, macOS, Linux                                                                                                                   |
| Supported UI toolkits        | WinForms, WPF, Win UI 3, MAUI                                                                                                                | WinForms, WPF, Avalonia, Win UI 3                                                                                                       |
| [Data collection][privacy]   | Yes                                                                                                                                          | No                                                                                                                                      |
| Headless mode                | No                                                                                                                                           | Yes, works in the console or as a service.                                                                                              |
| [Technical support][support] | No                                                                                                                                           | Yes, confidential, with SLA.                                                                                                            |

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
* You need to print programmatically.

## Difference in approaches

WebView2 is a control from Microsoft. It's free, but — as one expects from
Microsoft — it's also proprietary. It comes as a replacement for a Trident-based
WebView and uses Edge instead.

WebView2 is a control: an item in the Visual Studio toolbox, classes from the
`Microsoft.Web.WebView2.Core.dll` file. But it is not a Microsoft product like
Office or PowerBI. So you don't get customer care, technical support, or
assistance.

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

How do you get help if you find a bug or need a feature? Let's take a look
at what WebView2 and DotNetBrowser have to offer.

WebView2 gathers feedback from the public in a dedicated GitHub repository. When 
you have a report to make, you create an issue there. If Microsoft developers 
find your report worthy, they transfer it to their internal system. You will 
know by the "tracked" label they use for such issues.

Microsoft developers quickly react to new reports, but they address them much 
slower. For example, almost 80% of tracked issues stayed unresolved for more 
than 6 months at the moment of writing.

DotNetBrowser has a private helpdesk system where reports from clients remain 
confidential. The guaranteed first response time, or SLA, is one business day.

The technical support includes: help with product use, assistance with 
troubleshooting, bug fixing, and considering feature requests. All your support 
requests will be processed by DotNetBrowser software engineers.

### Privacy of end users

> This article was written in October 2022 and described the version of EULA as of this date. 

When an end user installs WebView2 in their environment, the installer shows
them EULA. Two things may concern you:

 1. Microsoft may collect information about your end users.
 2. You're required to warn them about it.

Section 3.a of the EULA states that WebView2 may collect information about you
and the end user's use of the software. This information is then can be sent to
Microsoft.

The fact that Microsoft gathers the end user's information obliges you to show
the corresponding notice and get their consent (Section 9 of the EULA).

DotNetBrowser does not collect information about you and your end users.
Furthermore, it prevents data collection by Google. Read more about how
DotNetBrowser handles data and gives you control over privacy in the [Privacy
Practices][privacy-practices].

## Technical differences

From a technical standpoint, DotNetBrowser and WebView2 are not that different.
Both have a similar architecture where Chromium runs in a separate process. Both
have hundreds of features, most of which overlap.

The differences, however, exist. And they can be essential when choosing the
solution that fits your case. So let's take a look.

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
provides a very basic functionality, DotNetBrowser gives developers more options
and full control over the extension lifecycle and activity.

In WebView2, a developer can install an extension from an unpacked CRX file,
enable/disable the extension, and uninstall it.

In DotNetBrowser, a developer can install an extension directly from the CRX 
file, programmatically "click" on the extension icon, interact with a pop-up and 
new "tabs" the extension may open. 

Also, you can let users interact with extensions directly:

* Enable using Chrome Web Store.
* Display the extension icon, with badges and labels.
* Show pop-ups and "tabs" creates by the extension.

Read more in the [guide on extensions][extensions-guide]
and [try it in practice][extensions-article].

### Running without UI

For use cases such as automation or generating PDF reports, it's unnecessary to
have a user interface. Instead, it's simpler and more efficient to run headless.

WebView2 doesn't support running without UI, as it requires an application
window.

In DotNetBrowser, this works out of the box. You can use it in the console
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

In 2024, Microsoft officially rejected the plan to support macOS and Linux in 
WebView2.

DotNetBrowser is a cross-platform library that runs on Windows, macOS, 
and Linux. Use it with 
[Avalonia UI][avalonia] or [in the server application][console].

### WPF and overlapping Controls

Putting any WPF control on top of a WebView2 control is impossible. This is 
caused by the natural WPF limitations and how WebView2 works.

WPF doesn't support overlapping between regions rendered in different windows, 
and WebView2 works precisely by embedding a foreign window into WPF control.

For DotNetBrowser, this is not a problem. Besides using the native window like 
WebView2, it can render directly within the WPF window.

It's called the off-screen rendering mode. In this mode, the rendered pixels are 
copied to the .NET process memory and displayed in a regular WPF widget.

### Calling JavaScript from .NET

In both solutions, you can execute JavaScript right from the .NET code. The 
difference is in what happens when the result travels back from Chromium to the 
.NET world.

WebView2 converts the result to JSON:

```cs
string result = await coreWebView2.ExecuteScriptAsync(@"'example'");
Debug.Assert(result == "\"example\"");
```

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

Both solutions allow using .NET objects from within JavaScript, but with a catch.

In WebView2, an injected object should be COM visible and implement `IDispatch`. 
This requirement limits the range of what you can inject and multiplies the 
boilerplate code.

In DotNetBrowser, you can [inject any object][javascript]: 
standard .NET objects, collections, and even WPF controls. In JavaScript, you 
will have access to the injected object's public members and indexed properties.

### Intercepting traffic

WebView2 doesn't have an API for intercepting, filtering or modifying HTTP 
requests.

DotNetBrowser, on the other hand, has a broad functionality for managing HTTP 
traffic. With this functionality, you can implement the following:

* [Filter HTTP requests][navigation-filtering].
* [Redirect HTTP requests][before-url-request].
* Override the HTTP [request][before-start-transaction]
  and response headers.
* [Override request upload data][before-upload].
* [Filter cookies][suppress-cookies].

You can find more examples  of networking in DotNetBrowser in our 
[GitHub][examples-network].

### Printing API

WebView2 has a limited printing API. It can print to PDF and allows you to 
manipulate a handful of settings. Alas, it is pretty limited:

* You can't choose a specific system printer.
* You can't configure page ranges.
* You can't control printing dialogs displayed to the user.

DotNetBrowser provides complete control over the printing process. You can:

* Choose a printer.
* Handle printing initiated by JavaScript and .NET code.
* Seeing the capabilities of a printer to avoid using unsupported features.
* Configure print settings, including page ranges, paper size, margins, headers, 
  footers, etc.

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
