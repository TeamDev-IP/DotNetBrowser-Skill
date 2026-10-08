# Browser control for WinForms

Do you need to display web pages in WinForms? You can do that by using a browser
control. You have many controls to choose from — both free and commercial. They
are different in what they can do and which use case they cover best.

In this blog post, we show how to use DotNetBrowser, a Chromium-based browser
control created for projects with critical use cases and high standards for
software and vendors.

Do you consider using WebView2 or CefSharp in the WinForms application? Check
out comparison articles:

* [Choosing between WebView2 and DotNetBrowser][webview2-article].
* [Choosing between CefSharp and DotNetBrowser][cefsharp-article].

## When to choose DotNetBrowser

DotNetBrowser is commercial software that was designed with enterprise use cases
in mind. Along with the library, the clients get confidential technical support
with a reaction time of **one business day**.

Choose DotNetBrowser when you need:

* an easy-to-use library;
* prompt bug fixes;
* technical support and assistance;
* one of the Chromium features like extensions, printing API, screen sharing,
  proprietary audio and video codecs, and more.

## Installing dependencies

DotNetBrowser comes as a set of DLL files and is available on NuGet.

Choose "nuget.org" as the package source, search for `DotNetBrowser.WinForms`
package, and hit the "Install" button.

![The list of DotNetBrowser's NuGet packages](https://teamdev.com/dotnetbrowser/blog/browser-control-for-winforms/dotnetbrowser-in-nuget.webp)
<p class="image-caption">DotNetBrowser packages in NuGet.</p>

## Add a browser to the WinForms application

To add a DotNetBrowser control to a WinForms application, use this code snippet
as a reference:

```cs
using System.Windows.Forms;
using DotNetBrowser.Browser;
using DotNetBrowser.Engine;
using DotNetBrowser.WinForms;

namespace Embedding.WinForms
{
    public partial class WebViewForm : Form
    {
        private const string Url = "https://teamdev.com/dotnetbrowser";
        private readonly IBrowser browser;
        private readonly IEngine engine;

        public WebViewForm()
        {
            InitializeComponent();

            engine = EngineFactory.Create(RenderingMode.HardwareAccelerated);
            browser = engine.CreateBrowser();
            browser.Navigation.LoadUrl(Url);
            FormClosed += WebViewForm_FormClosed;

            BrowserView browserView = new BrowserView
            {
                Dock = DockStyle.Fill
            };
            Controls.Add(browserView);
            browserView.InitializeFrom(browser);
        }

        private void WebViewForm_FormClosed(object s, FormClosedEventArgs e)
        {
            browser?.Dispose();
            engine?.Dispose();
        }
    }
}
```

This results in the following:

![WinForms application with DotNetBrowser control](https://teamdev.com/dotnetbrowser/blog/browser-control-for-winforms/dotnetbrowser-in-winforms.webp)
<p class="image-caption">WinForms application with DotNetBrowser control.</p>

In this snippet above, we created three objects at once: `IEngine`, `IBrowser`, 
and `BrowserView`. Let me explain.

DotNetBrowser gives you fine-grained control over the underlying browser engine
and provides the respective hierarchy of abstractions.

![The architecture of DotNetBrowser](https://teamdev.com/dotnetbrowser/blog/browser-control-for-winforms/dotnetbrowser-architecture.svg)
<p class="image-caption">The architecture of DotNetBrowser.</p>

The `IEngine` starts the main Chromium process. You may want to create multiple
engine instances if you need to create many browsers that are perfectly isolated
from each other.

Creating an engine takes time because it starts the Chromium process. You can
create `IEngine` on any thread, but the calling thread waits until Chromium
starts. When you call `EngineFactory.Create` on the UI thread, the form doesn't
respond during that time. To avoid this, use `EngineFactory.CreateAsync`. In
this blog post, we use the synchronous method to keep the example code simple.

Every engine has one or more `IProfile`'s, that allow to isolate browsers within
the same engine by keeping the browser data and settings separate. You can
manage cache, proxy, networking, downloads, permissions, and [other features on
the profile level][profile-features].

Within an `IProfile`, you can create multiple `IBrowser` instances. 
An `IBrowser` is best compared to a browser tab in Chromium. These 
instances function as fully-fledged browsers, allowing you to load web pages, 
simulate mouse and keyboard input, open developer tools, 
and [more][browser-features].

And finally, `BrowserView` is an actual control that shows the browser. 
This abstraction is separate from the `IBrowser` because the latter works 
independently of the UI, rendering in memory even when not visible to the user.

## Conclusion

This explains how to use DotNetBrowser, a Chromium-based browser control for
WinForms. It is a control designed for companies with critical use cases, 
needing technical support, custom features, or advanced features like Chrome
extensions or Printing API.



[webview2-article]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/
[cefsharp-article]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/
[profile-features]: https://teamdev.com/dotnetbrowser/docs/guides/gs/profile/
[browser-features]: https://teamdev.com/dotnetbrowser/docs/guides/gs/browser/
