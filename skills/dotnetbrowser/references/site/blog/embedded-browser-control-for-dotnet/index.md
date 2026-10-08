# Embedded browser control for .NET

In this article, we explain the embedded browser controls for .NET: what they 
are and what they are good for.

## What is an embedded browser?

It is a fully functional web browser inside your software that you control with 
code. An embedded browser doesn't have an address bar, tabs, or other attributes 
of a regular browser. In fact, it may not be on the screen at all.

But when it's on the screen, it looks like a rectangle with a web page 
inside.

![DotNetBrowser in WPF](https://teamdev.com/dotnetbrowser/blog/embedded-browser-control-for-dotnet/dotnetbrowser-wpf.webp "loading=eager")
<p class="image-caption">DotNetBrowser in WPF</p>

## What are the use cases?

A browser has many capabilities you won't find in the standard library or a 
desktop toolkit. An embedded browser brings those capabilities to your 
application.

This section describes some of the challenges made easy by DotNetBrowser.

### Automation and scraping

Many web systems don't have an API and are designed to be used by people. 
Working with such systems means manually repeating monotonous 
operations — a perfect job for a computer.

DotNetBrowser provides capabilities to simulate user actions and retrieve any 
information from the page, including pictures. With that, one can automate their 
work with any website, including single-page applications.

### Integrating third-party apps

The software infrastructure of an organization can become convoluted with time.

For example, when processing a patient's request, a hospital employee may need 
to see their medical and insurance records. This data can be spread across 
multiple applications from different vendors — which the employee uses 
simultaneously.

A single WPF or WinForms window can accommodate multiple DotNetBrowser controls, 
each of which hosts an application. Then, you can interconnect the browsers and 
exchange information between them automatically.

### Generating PDF

Generating nice-looking PDF files is a tricky task. However, with 
the browser, it's simple to generate a PDF document: design a web page, open 
and print it as PDF.

With DotNetBrowser, you get the rendering capabilities of Chromium and rich API 
with full control over printing settings.

## How to get started?

[Get your free license](https://teamdev.com/dotnetbrowser?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog#evaluate) 
and choose one of our getting started guides. It takes 5 minutes to start using 
DotNetBrowser:

* [DotNetBrowser in WPF](https://teamdev.com/dotnetbrowser/docs/quickstart/wpf/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog)
* [DotNetBrowser in WinForms](https://teamdev.com/dotnetbrowser/docs/quickstart/winforms/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog)
* [DotNetBrowser in the console](https://teamdev.com/dotnetbrowser/docs/quickstart/console/?utm_campaign=embedded-browser&utm_medium=article&utm_source=product-blog), useful for Windows services and server applications.


