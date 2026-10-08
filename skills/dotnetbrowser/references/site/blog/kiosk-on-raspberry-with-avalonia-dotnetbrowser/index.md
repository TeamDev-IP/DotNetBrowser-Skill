# Kiosk app on Raspberry Pi with Avalonia and DotNetBrowser

This guide explains how to build a kiosk app for Raspberry Pi 5 using 
Avalonia and DotNetBrowser.

Kiosk applications often rely on lockdown browsers — browsers that where users 
can’t navigate away, open new windows, or access operating system controls. 

In this guide, the kiosk is locked down at the architectural level. 
The application runs without a desktop environment, and fully controls
the display and input.

The application is written in C#. It uses Avalonia UI to create a full-screen 
window and DotNetBrowser web view component to show web content.

You’ll set up the development environment, configure the operating system, and
deploy an app for kiosks with a touch display.

## What you'll need

You’ll need a **Raspberry Pi 5**, ideally with **8 or 16 GB of RAM**. 
Chromium, which DotNetBrowser is built on, uses considerable memory during 
runtime, so the extra capacity won't hurt.

Development and deployment start on your regular computer. You can work on
Windows, macOS, or Linux with the .NET 8 SDK installed. Use any modern IDE you
prefer:

* Visual Studio 2022 or later;
* Visual Studio Code;
* JetBrains Rider.

## Creating application

### Install the DotNetBrowser templates

DotNetBrowser offers templates that help you quickly set up a new Avalonia 
application with DotNetBrowser.

In your development environment, open the command line, and install 
DotNetBrowser templates:

```shell
dotnet new install DotNetBrowser.Templates
```

### Get the trial license

Before you can create a new project, you'll need a DotNetBrowser license.
DotNetBrowser is a commercial library. To evaluate it, you can request a free
30-day trial license.

To get a free 30-day trial license, fill out the form. 
You'll receive your license key by email.



### Generate the lockdown browser application

Use the `dotnetbrowser.avalonia.app` template to generate a starter Avalonia
project with all the necessary dependencies. Run this command to create 
a project from the template in the `RaspberryKiosk` folder:

```shell
dotnet new dotnetbrowser.avalonia.app -o RaspberryKiosk -li <your_license_key>
```

By default, the project targets `net8.0`. You change the target to `net9.0`, 
`net7.0`, or `net6.0` using the `-f` flag:

```shell
dotnet new dotnetbrowser.avalonia.app -o RaspberryKiosk -li <your_license_key> -f net9.0
```

### Configure the application window

The project template already creates a working Avalonia window with an embedded
DotNetBrowser control and handles its initialization in the code-behind.
What remains is to adapt this window for kiosk use.

Because the app will run in a kiosk, it must open in fullscreen, stay on top,
and prevent the user from minimizing or closing it. 
In <nobr>the `MainWindow.axaml`</nobr> file, configure the main window to be:

* borderless, 
* fullscreen, 
* without window decorations, 
* or taskbar access. 

Add the following attributes to the window in <nobr>`MainWindow.axaml`</nobr>:

```xml {hl_lines=["3-7"]}
<Window
    ... 
    WindowState="FullScreen"
    Topmost="True"
    ExtendClientAreaToDecorationsHint="True"
    ExtendClientAreaChromeHints="NoChrome"
    ShowInTaskbar="False"
>
    <app:BrowserView x:Name="BrowserView"/>
</Window>
```

### Configure the web view

Here you’ll start the Chromium engine and adjust a few settings that affect how
it runs on the Raspberry Pi. Two of them are worth pointing out:

* `HardwareAccelerated` rendering mode — lets Chromium draw straight into the
  window using the GPU, which is faster and uses less CPU.
* Disable pinch-to-zoom (`--disable-pinch`) — turns off pinch-to-zoom so users
  can’t accidentally change the page scale.

**MainWindow.xaml.cs**

```java
public partial class MainWindow : Window
{
    private readonly IBrowser browser;
    private readonly IEngine engine;

    public MainWindow()
    {          
        // Start the Chromium process.
        EngineOptions engineOptions = new EngineOptions.Builder
        {
            LicenseKey = "",
            RenderingMode = RenderingMode.HardwareAccelerated,
            ChromiumSwitches =
            {
                "--disable-pinch",
            }
        }.Build();
        engine = EngineFactory.Create(engineOptions);

        // Create the browser instance.
        browser = engine.CreateBrowser();

        // Initialize the Avalonia component
        InitializeComponent();

        // Initialize the BrowserView control.
        BrowserView.InitializeFrom(browser);

        // Disable the context menu.
        browser.ShowContextMenuHandler = null;

        // Navigate to amy page to make sure it's working.
        browser.Navigation.LoadUrl("https://google.com");
     }
 }
```

![A web page opened in full-screen Avalonia window](https://teamdev.com/dotnetbrowser/blog/kiosk-on-raspberry-with-avalonia-dotnetbrowser/web-ui-in-avalonia.webp)
<p class="image-caption">A web page opened in full-screen Avalonia window.</p>

### Create a debug close button

Because the kiosk runs in fullscreen without system controls, there’s no
straightforward way to close the application during development. To make
debugging easier, you can add a utility debug bar that appears only in debug builds.

![An automatically added bar for the debug mode.](https://teamdev.com/dotnetbrowser/blog/kiosk-on-raspberry-with-avalonia-dotnetbrowser/debug-bar.webp)
<p class="image-caption">An automatically added bar for the debug mode.</p>

Here's the script that creates a fixed on-screen button that stays visible and
closes the application when clicked:

**MainWindow.xaml.cs**

```java
browser.navigation.FrameDocumentLoadFinished += (s, e) => 
{
#if DEBUG
    IFrame frame = e.Frame;

    IJsObject window = 
        args.Frame.ExecuteJavaScript<IJsObject>("window").Result;
    // Add function that closes the application.
    window.Properties["closeApplication"] = 
         () => Dispatcher.UIThread.InvokeAsync(Close);

    // Adds a debug bar with the close link.
    browser.MainFrame.ExecuteJavaScript<>(@" 
        (() => {
          const bar = document.createElement('div');
          Object.assign(bar.style, {
            position: 'fixed',
            top: '0',
            left: '0',
            width: '100%',
            padding: '5px 0 5px 0px',
            background: 'pink',
            textAlign: 'center',
            zIndex: '9999'
          });
          bar.innerHTML = 
             'DEBUG MODE. <a onclick="closeApp()">Close application.</a>';
          document.body.appendChild(bar);
        })();
    ");
#else
#endif
};
```

This way, the release build remains locked down, but you can still conveniently
exit the app while testing.

### Add the web page

There are several ways to load web pages into DotNetBrowser on 
the Raspberry Pi, depending on how your kiosk should access its 
content:

* **Load a remote URL.** The simplest option, suitable for kiosks that stay
  online.
* **Run a local web server.** Works well for offline setups, letting the browser
  load pages served from the same device.
* **Open local HTML files**. You can use the `file://` protocol for simple
  cases, but Chromium limits local access, so it’s not ideal for complex apps.
* **Serve pages from app resources**. You can use
  DotNetBrowser [scheme interceptors][guides-interceptors]
  to serve pages directly from your app’s resources.

### Configure runtime and deployment

The application requires .NET runtime, which you won't usually find in Linux 
out of the box. So, instead of installing the runtime, you can publish your 
application as a self-contained build — a package that includes the .NET runtime 
alongside your app.

In the `RaspberryKiosk/RaspberryKiosk.csproj` file, add the 
<nobr>`linux-arm64`</nobr> runtime identifier and make the project 
self-contained:

```xml {hl_lines=["5-7"]}
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <OutputType>WinExe</OutputType>
    <TargetFramework>net8.0</TargetFramework>
    <RuntimeIdentifiers>win-x64;linux-arm64</RuntimeIdentifiers>
    <SelfContained>true</SelfContained>
    <PublishSingleFile>true</PublishSingleFile>
  </PropertyGroup>
</Project>
```

This setup bundles the full .NET 8 runtime and publishes your app as a
single-file executable.

### Publish the application

To prepare the app for the Raspberry Pi, publish it for the Linux ARM64 
platform using the following command:

```shell
dotnet publish RaspberryKiosk/RaspberryKiosk.csproj \
       -c Release -r linux-arm64 --self-contained true -o ./publish/rpi
```

This creates an executable file in the `./publish/rpi` directory, ready to
deploy to Raspberry Pi 5.

## Configuring the Raspberry Pi

To keep the system efficient and stable, the kiosk will run on 
Raspberry Pi OS Lite — with only the components required for 
graphics. Instead of installing a full desktop environment, you’ll use 
the X server and a minimal window manager.

The X server is the part of Linux that provides graphical output and handles
input devices such as the keyboard and mouse. It doesn’t draw windows itself; it
just manages the display surface. A window manager sits on top of it and
controls how windows appear and behave — placement, focus, borders, and stacking
order.

This minimalistic setup prevents users from leaving the kiosk application and
avoids the overhead of extra software that comes with desktop environments.

### Install the operating system

Follow the [official guide][raspberry-guide]
and install Raspberry Pi OS Lite 64-bit on your device. It's 
available in the official Raspberry Pi Imager:

![Raspberry Pi OS Lite in the official imager.](https://teamdev.com/dotnetbrowser/blog/kiosk-on-raspberry-with-avalonia-dotnetbrowser/pi-imager-screenshot.webp)
<p class="image-caption">Raspberry Pi OS Lite in the official imager.</p>

### Install system dependencies

To run Avalonia apps with DotNetBrowser on Raspberry Pi OS Lite, 
install the X server and OpenBox, a lightweight window manager:

```shell
sudo apt update && sudo apt upgrade -y
sudo apt install --no-install-recommends \
     xserver-xorg xinit openbox gldriver-test
```

> The `gldriver-test` package configures GPU usage in X server.

Add your Raspberry Pi user to the tty group so X server can launch:

```shell
sudo useradd -G tty username
```

### Install Chromium dependencies

DotNetBrowser needs several Chromium dependencies. Install them with 
the following command:

```shell
sudo apt install libgtk2.0-0 \
        libgtk-3-0 \
        libgbm1 \
        libnotify4 \
        libnss3 \
        libxss1 \
        libasound2 
```

### Deploy the application

Now, you can copy the published application from the development machine to the
Raspberry Pi. You can use a USB stick, or copy it using `scp`:

```shell
scp -r ./publish/rpi username@<your-host-name>:~/
```

On the Raspberry Pi, give this file executable permissions:

```shell
cd rpi
chmod +x RaspberryKiosk
```

Now you can launch the app. In `~/rpi` directory, use the `startx` command to
run it in the X server session:

```shell
startx ./RaspberryKiosk
```

### Configure auto-start

The proper kiosk application should start on its own after boot. For that, in
the home directory, create a simple script called `start-kiosk.sh` that launches
the app:

```shell
#!/bin/bash
cd ~/rpi
startx ./RaspberryKiosk
```

And make it executable:

```shell
chmod +x ~/start-kiosk.sh
```

Next, configure the system to run your script at boot. For that, add the
following snippet to the `~/.bashrc` file:

```shell
if [ "$(tty)" = "/dev/tty1" ]; then
  ~/start-kiosk.sh
fi
```

And finally, set up automatic login. Open the `raspi-config` utility:

```shell
sudo raspi-config
```

In the utility, select **"System Options"** > **"Auto Login"**. In the dialog,
select **"Yes"** and press `Enter` to save the changes. Then, select 
**"Finish"** to exit.



## Launching the kiosk

Now, you can restart the Raspberry Pi and the kiosk application will be
automatically launched on the start.

![The kiosk app made with Avalonia and DotNetBrowser launched on Raspberry Pi 5](https://teamdev.com/dotnetbrowser/blog/kiosk-on-raspberry-with-avalonia-dotnetbrowser/avalonia-kiosk-raspberry.webp#medium)
<p class="image-caption">The kiosk app made with Avalonia and DotNetBrowser launched on Raspberry Pi 5.</p>

## Conclusion

With Avalonia and DotNetBrowser on Raspberry Pi, you get a lightweight
and dependable kiosk system. You control both hardware and software, keep
resource use low, and let the app start automatically after boot. Because the UI
and deployment are separate, updates are easy to roll out.

The kiosk can load local HTML files or show remote pages, so you can manage
what’s displayed from a single place. It’s a simple setup for digital signage,
dashboards, or any screen that needs fresh content without hands-on upkeep.

[guides-interceptors]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#intercept-request-per-uri-scheme
[raspberry-guide]: https://www.raspberrypi.com/documentation/computers/getting-started.html#installing-the-operating-system
