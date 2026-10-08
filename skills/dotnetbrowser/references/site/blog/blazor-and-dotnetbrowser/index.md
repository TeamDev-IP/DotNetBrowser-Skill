# Blazor and DotNetBrowser

What is Blazor? What is DotNetBrowser? Can one replace another? 
Can they work together?

We regularly hear these questions from developers curious about DotNetBrowser. 
In this article, we want to clarify the difference between the two.

## What is Blazor?

Blazor is a framework for developing interactive client-side web UI with C# 
instead of JavaScript.

With Blazor, you can host the same application in three different ways:

* As a WebAssembly right in the browser.
* As the server application in ASP.NET Core.
* As a native application with MAUI, WPF, and WinForms.

## What is DotNetBrowser?

DotNetBrowser is a browser control that you can embed into Avalonia UI, 
WinForms, and WPF. Besides client applications, you can use DotNetBrowser on 
the server side.

DotNetBrowser is based on Chromium and enables you to use the latest web 
technologies in .NET software.

You may want to use DotNetBrowser for:

* A web view for Blazor Hybrid applications. 
* Generating PDF.
* Automation and scraping.
* Integration with third-party applications.
* Displaying WebGL charts and other graphics.
* And many other things.

## Can DotNetBrowser replace Blazor?

No.

Blazor is a complex web framework, and one of its many features is creating 
native applications. Also known as Blazor Hybrid applications. These 
applications run on desktop and mobile platforms. To show them, Blazor utilizes 
web view controls available in the environment.

DotNetBrowser is a desktop-only web view control. The scope of DotNetBrowser is 
different and clear: embedding Chromium and providing API to control it. 

## Can DotNetBrowser work with Blazor?

Absolutely.

You can create Blazor Hybrid applications with Avalonia UI and DotNetBrowser.
With these technologies, the Blazor Hybrid works on Linux, in addition to macOS 
and Windows.

Read more in 
[Blazor Hybrid apps with Avalonia UI][avalonia-article] article.

## Get started with DotNetBrowser

[Get your free license][evaluation]
and choose one of our getting started guides. It takes 5 minutes to start using
DotNetBrowser:

* [DotNetBrowser in WPF][in-wpf]
* [DotNetBrowser in WinForms][in-winforms]
* [DotNetBrowser in the console][in-console], useful for Windows services and server applications.

[evaluation]: https://teamdev.com/dotnetbrowser#evaluate
[in-wpf]: https://teamdev.com/dotnetbrowser/docs/quickstart/wpf/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[in-winforms]: https://teamdev.com/dotnetbrowser/docs/quickstart/winforms/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[in-console]: https://teamdev.com/dotnetbrowser/docs/quickstart/console/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog
[avalonia-article]: https://teamdev.com/dotnetbrowser/blog/blazor-hybrid-apps-in-avalonia-ui/


