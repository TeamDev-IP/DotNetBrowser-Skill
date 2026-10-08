
# System requirements

**Lead**
This page describes the software and hardware configurations required to run a program based on DotNetBrowser.


## Software requirements

### .NET

* .NET Framework 4.6.2 — 4.8.1  (Windows only)
* .NET 5 - 10

### Avalonia UI

* 11.2.0 and higher

### Windows

DotNetBrowser supports x86, x64, and ARM64:

 * Windows 11
 * Windows 10
 * Windows Server 2022
 * Windows Server 2019
 * Windows Server 2016
 
**Note**
Starting with Chromium 110 and DotNetBrowser 2.21, 
Windows 7/8/8.1 and the corresponding Windows Server versions are not supported.


### Linux

DotNetBrowser supports the following Linux distributions (x64 and ARM64):

 * Ubuntu 18.04 or later
 * Debian 10 or later
 * Fedora Linux 38 or later
 * openSUSE 15.5 or later
 * RedHat Enterprise Linux 8.9 or later

 **Note**
Chromium does not work in the headless environment. In order to use DotNetBrowser in headless environments including Linux-based Docker containers and WSL, you need to [start X server](https://teamdev.com/dotnetbrowser/docs/guides/headless-linux/).


### macOS

DotNetBrowser supports the following macOS distributions (x64 and ARM64):
 * Tahoe 26
 * Sequoia 15
 * Sonoma 14
 * Ventura 13

**Note**
macOS must run in the non-headless mode, because Chromium does not support the headless mode on this platform.


## Hardware requirements

### HiDPI monitors

DotNetBrowser recognizes the device scale factor that is used in the environments with HiDPI displays and renders HTML content with the respect to that scale factor.

The WPF and WinForms `BrowserView` controls are compatible with different [DPI awareness modes](https://learn.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#dpi-awareness-mode). DotNetBrowser gets the DPI awareness settings from the application configuration where it is used and configures Chromium processes to use the same DPI awareness mode.

**Note**
DotNetBrowser supports high DPI only if your .NET desktop application supports it.


These MSDN articles describe how to create DPI-aware .NET desktop applications:

- [High DPI desktop application development on Windows](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx)
- [Creating a DPI-Aware Application](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/ms701681(v=vs.85))
- [Developing a Per-Monitor DPI-Aware WPF Application](https://learn.microsoft.com/en-gb/windows/win32/hidpi/declaring-managed-apps-dpi-aware?redirectedfrom=MSDN)
- [High DPI support in Windows Forms](https://learn.microsoft.com/en-us/dotnet/framework/winforms/high-dpi-support-in-windows-forms)

### Android/iOS

DotNetBrowser does not support mobile devices with iOS and Android.

## Other Environments

You can try running DotNetBrowser on other platforms or versions not listed here, but we do not guarantee that all DotNetBrowser functionality will work properly there.

**Note**
DotNetBrowser cannot be used in the environments that prevent the User32/GDI32 APIs from being called, such as Azure App Services or Azure Functions. With these limitations, it is not possible to launch the Chromium engine.

