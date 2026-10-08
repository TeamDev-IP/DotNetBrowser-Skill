# Web view for WPF

Windows Presentation Foundation (WPF) continues to be a widely used framework
for developing desktop applications due to its flexibility. As applications
evolve, the integration of modern web content within WPF has become essential.
DotNetBrowser, a .NET library, addresses this need by allowing developers to
embed a Chromium-based web view within WPF applications. This makes it possible
to display and interact with web content natively inside your .NET desktop
applications.

In this article, we’ll walk you through the steps of integrating DotNetBrowser
into a WPF project.

## Why choose DotNetBrowser

WPF is already great for building rich user interfaces, but what if your app
needs to interact with dynamic web content or display interactive HTML5
features? DotNetBrowser truly proves its value here. With its Chromium-based
engine, DotNetBrowser:

* Ensures full compatibility with modern web standards, including HTML5,
  JavaScript, and CSS3.
* Integrates seamlessly into WPF, enabling developers to focus on UI and
  interaction instead of managing browser complexities.
* Implements sandboxing and security protocols to maintain application safety
  when processing web content.

## Getting started

Let’s dive into the process of integrating DotNetBrowser with a WPF project. 
Begin the process by creating a new WPF project in Visual Studio:

1. Open Visual Studio and select Create a new project.
2. Choose "WPF App (.NET Core)" or "WPF App (.NET Framework)", depending on
   your preference.
3. Name your project `Examples.Wpf` and click Create.

Install DotNetBrowser via NuGet:

1. Right-click on your project in Solution Explorer and choose "Manage NuGet
   Packages".
2. In the Browse tab, search for the `DotNetBrowser.Wpf` package and install
   it. This will automatically include all the necessary dependencies as
   well.
3. After installation, you can check the `packages.config` or `Project.csproj` 
   file to confirm it has been added successfully.

Add DotNetBrowser web view to your WPF application:

Now that you have DotNetBrowser installed, let’s embed it into your WPF window. 
In your `MainWindow.xaml` file, add a `WPF:BrowserView` control to host the
browser:

```xml
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:WPF="clr-namespace:DotNetBrowser.Wpf;assembly=DotNetBrowser.Wpf"
    x:Class="Examples.Wpf.MainWindow"
    mc:Ignorable="d"
    Title="MainWindow" Height="480" Width="800" Closed="Window_Closed">
    <Grid>
        <WPF:BrowserView Name="browserView" />
    </Grid>
</Window>
```

Next, go to the `MainWindow.xaml.cs` file and create the engine and browser instances:

```cs
using System;
using System.Windows;
using DotNetBrowser.Browser;
using DotNetBrowser.Engine;

namespace Examples.Wpf
{
    public partial class MainWindow : Window
    {
        private const string Url = "https://html5test.teamdev.com/";
        private readonly IBrowser browser;
        private readonly IEngine engine;

        public MainWindow()
        {
            // Start the Chromium main process.
            EngineOptions engineOptions = new EngineOptions.Builder
            {
                RenderingMode = RenderingMode.HardwareAccelerated,
                LicenseKey = "license key"
            }.Build();
            engine = EngineFactory.Create(engineOptions);

            browser = engine.CreateBrowser();

            InitializeComponent();

            // Connect the BrowserView control with the actual browser.
            browserView.InitializeFrom(browser);
            browser.Navigation.LoadUrl(Url);
        }

        private void Window_Closed(object sender, EventArgs args)
        {
            browser?.Dispose();
            engine?.Dispose();
        }
    }
}
```

Now, you can run the application. Upon launch, you will see that the browser is
successfully embedded in your window, displaying the web content specified.

## Benefits of DotNetBrowser

DotNetBrowser integration in a WPF project offers a range of technical capabilities:

* It supports JavaScript, HTML5, and CSS3, allowing the incorporation of
  web-based UI components into desktop applications.

* It enables .NET-to-JavaScript communication, facilitating direct interaction
  between the application's logic and web content.

* With hardware-accelerated rendering, it guarantees smooth performance even
  when handling heavy web content.

## Conclusion

DotNetBrowser is a web view component for .NET. Integrating it with WPF enables
developers to enhance desktop applications by embedding interactive web content
directly into the user interface. This approach supports a range of use cases,
from enterprise solutions to consumer-facing applications, allowing .NET
developers to leverage both desktop and web technologies for more versatile
functionality.

---

Ready to take your WPF applications to the next level? Get the evaluation
license key for DotNetBrowser and start building modern .NET solutions today! 



Do you consider using WebView2? Read our article on why [DotNetBrowser
is a better choice for a commercial use][webview2-article].

[webview2-article]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/ 
