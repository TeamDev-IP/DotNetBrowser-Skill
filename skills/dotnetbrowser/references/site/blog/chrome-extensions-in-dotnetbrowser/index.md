# Chrome extensions in DotNetBrowser

We're happy to announce that Chrome extensions in DotNetBrowser are in public 
preview!

This article give a quick overview on how to install and use extensions in 
DotNetBrowser.

![uBlock extension in DotNetBrowser](https://teamdev.com/dotnetbrowser/blog/chrome-extensions-in-dotnetbrowser/ublock-in-dotnetbrowser.webp#small "loading=eager")
<p class="image-caption">An extension launched in DotNetBrowser</p>

Chrome extensions in a web view bring new capabilities into your software at no 
cost. With extensions, you can block ads, improve accessibility, use developer 
tools of JavaScript libraries, and many more.

## Clone the demo application

Here's how to get the demo application:

1. Clone [DotNetBrowser-Examples](https://github.com/TeamDev-IP/DotNetBrowser-Examples) 
   repository.

   ```shell
   git clone https://github.com/TeamDev-IP/DotNetBrowser-Examples.git
   ```
2. Get a free 30-day trial license. Fill out the form,
   and you will receive an email with the license key immediately.



3. Put your license key into the `dotnetbrowser.license` file in the root of the
   repository. 
4. Open the solution in Visual Studio 2019 or newer.
5. Right-click the solution in "Solution Explorer" and select 
   "Restore NuGet Packages."
6. Build the solution and run the `Extensions` project.

## Use in the existing project

If you already use DotNetBrowser, you can get the latest build from NuGet:

```shell
dotnet add package DotNetBrowser -v "4.3.3"
dotnet add package DotNetBrowser.WPF -v "4.3.3"
```

## Install the extension

Installing an extension is straightforward:

```csharp
// The path to the extension file.
string crx = Path.GetFullPath("path/to/extension.crx");

// Install the extension and wait until installed.
var extensions = engine.Profiles.Default.Extensions;
IExtension extension = await extensions.Install(crx);
```

## Interact with extension

Every extension has an icon in the Chrome toolbar. When a user clicks on the 
icon, the extension usually does something. For example, it may show a small 
pop-up or silently change the content of the page.

In DotNetBrowser, there isn't a toolbar or icon to click on. So instead, we 
provide the API to "click on the icon" from code:

```csharp
extension.GetAction(browser)?.Click();
```

If the extension wants to show a pop-up, DotNetBrowser will open it as a new 
window. But you can change this behavior.

The extension's pop-up is a regular IBrowser instance. So you can do anything: 
show it inside the existing window, make it [transparent](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/master/csharp/wpf/TransparentWebPage),
or turn it into a modal dialog. In fact, you may decide not to show it at all.

In this example, we don't display the pop-up and do some automation instead:

```csharp
using DotNetBrowser.Browser.Handlers;
...
Browser.OpenExtensionActionPopupHandler = 
    new Handler<OpenExtensionActionPopupParameters>(p =>
    {
        IBrowser popupBrowser = p.PopupBrowser;
        // As soon as the frame is loaded, automate necessary actions.
        popupBrowser.Navigation.FrameLoadFinished += (s, e) =>
        {
            if (e.Frame.IsMain)
            {
                // Click on the button switch button.
                e.Frame.Document.GetElementById("switch").Click();
            }
        };
    });
```

## Give us extensions to check

Integrating Chrome extensions into DotNetBrowser marks a significant step 
forward, offering more possibilities for enhancing .NET applications. With this 
update, we invite developers to explore and provide feedback.

[Let us know](https://teamdev.com/contacts/) 
your thoughts and which extensions you want to use.
