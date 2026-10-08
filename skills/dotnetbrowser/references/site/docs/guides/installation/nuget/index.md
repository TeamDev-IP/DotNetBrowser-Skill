
# Installing from NuGet

**Lead**
This guide describes how to add DotNetBrowser to your .NET project from NuGet.


To add DotNetBrowser to project, install the appropriate NuGet packages listed below.

**Note**
DotNetBrowser itself depends on [Google.Protobuf](https://www.nuget.org/packages/Google.Protobuf). The corresponding package is automatically fetched while installing DotNetBrowser NuGet packages.


## Cross-platform

If you need DotNetBrowser to work on all supported platforms, you can install the appropriate packages listed below.

[`DotNetBrowser.CrossPlatform`](https://www.nuget.org/packages/DotNetBrowser.CrossPlatform/)<br>
[`DotNetBrowser.Chromium.Win-x86`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x86/)<br>
[`DotNetBrowser.Chromium.Win-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x64/)<br>
[`DotNetBrowser.Chromium.Win-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-arm64/)<br>
[`DotNetBrowser.Chromium.Linux-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Linux-x64/)<br>
[`DotNetBrowser.Chromium.Linux-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Linux-arm64/)<br>
[`DotNetBrowser.Chromium.macOS-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.macOS-x64/)<br>
[`DotNetBrowser.Chromium.macOS-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.macOS-arm64/)

**Note**
Installing `DotNetBrowser.CrossPlatform` fetches the rest required packages.


## Platform-specific

If you need DotNetBrowser to work only on a specific platform, you can install the appropriate packages listed below.

### Windows AnyCPU

[`DotNetBrowser`](https://www.nuget.org/packages/DotNetBrowser/)<br>
[`DotNetBrowser.Chromium.Win-x86`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x86/)<br>
[`DotNetBrowser.Chromium.Win-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x64/)<br>
[`DotNetBrowser.Chromium.Win-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-arm64/)

**Note**
Installing `DotNetBrowser` fetches the required Chromium binaries depending on the target platform automatically.


### Windows x86

[`DotNetBrowser.Win-x86`](https://www.nuget.org/packages/DotNetBrowser.Win-x86/)<br>
[`DotNetBrowser.Chromium.Win-x86`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x86/)

### Windows x64

[`DotNetBrowser.Win-x64`](https://www.nuget.org/packages/DotNetBrowser.Win-x64/)<br>
[`DotNetBrowser.Chromium.Win-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x64/)

### Windows ARM64

[`DotNetBrowser.Win-arm64`](https://www.nuget.org/packages/DotNetBrowser.Win-arm64/)<br>
[`DotNetBrowser.Chromium.Win-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-arm64/)

### Linux x64

[`DotNetBrowser.Linux-x64`](https://www.nuget.org/packages/DotNetBrowser.Linux-x64/)<br>
[`DotNetBrowser.Chromium.Linux-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Linux-x64/)

### Linux ARM64

[`DotNetBrowser.Linux-arm64`](https://www.nuget.org/packages/DotNetBrowser.Linux-arm64/)<br>
[`DotNetBrowser.Chromium.Linux-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Linux-arm64/)

### macOS x64

[`DotNetBrowser.macOS-x64`](https://www.nuget.org/packages/DotNetBrowser.macOS-x64/)<br>
[`DotNetBrowser.Chromium.macOS-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.macOS-x64/)

### macOS ARM64

[`DotNetBrowser.macOS-arm64`](https://www.nuget.org/packages/DotNetBrowser.macOS-arm64/)<br>
[`DotNetBrowser.Chromium.macOS-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.macOS-arm64/)

## UI framework

If you develop a desktop application where you want to display some web content, install one more package depending on the UI framework you use.

### WPF

[`DotNetBrowser`](https://www.nuget.org/packages/DotNetBrowser/)<br>
[`DotNetBrowser.Chromium.Win-x86`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x86/)<br>
[`DotNetBrowser.Chromium.Win-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x64/)<br>
[`DotNetBrowser.Chromium.Win-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-arm64/)<br>
[`DotNetBrowser.Wpf`](https://www.nuget.org/packages/DotNetBrowser.Wpf/)

**Note**
Installing `DotNetBrowser.Wpf` fetches the rest required packages.


**Note**
If your WPF application runs on 64-bit platforms, and 32-bit platforms are not supported, you can install [`DotNetBrowser.Wpf.x64`](https://www.nuget.org/packages/DotNetBrowser.Wpf.x64/) package. `DotNetBrowser.Win-x64`, `DotNetBrowser.Chromium.Win-x64` packages are fetched and installed automatically.


**Note**
If your WPF application runs on ARM64 platforms, you can install [`DotNetBrowser.Wpf.arm64`](https://www.nuget.org/packages/DotNetBrowser.Wpf.arm64/) package. `DotNetBrowser.Win-arm64`, `DotNetBrowser.Chromium.Win-arm64` packages are fetched and installed automatically.


### WinForms

[`DotNetBrowser`](https://www.nuget.org/packages/DotNetBrowser/)<br>
[`DotNetBrowser.Chromium.Win-x86`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x86/)<br>
[`DotNetBrowser.Chromium.Win-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x64/)<br>
[`DotNetBrowser.Chromium.Win-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-arm64/)<br>
[`DotNetBrowser.WinForms`](https://www.nuget.org/packages/DotNetBrowser.WinForms/)

**Note**
Installing `DotNetBrowser.WinForms` fetches the rest required packages.


**Note**
If your WinForms application runs on 32-bit platforms, and 64-bit platforms are not supported, you can install [`DotNetBrowser.WinForms.x86`](https://www.nuget.org/packages/DotNetBrowser.WinForms.x86/) package. `DotNetBrowser.Win-x86`, `DotNetBrowser.Chromium.Win-x86` packages are fetched and installed automatically.


**Note**
If your WinForms application runs on ARM64 platforms, you can install [`DotNetBrowser.WinForms.arm64`](https://www.nuget.org/packages/DotNetBrowser.WinForms.arm64/) package. `DotNetBrowser.Win-arm64`, `DotNetBrowser.Chromium.Win-arm64` packages are fetched and installed automatically.


### WinUI 3

[`DotNetBrowser`](https://www.nuget.org/packages/DotNetBrowser/)<br>
[`DotNetBrowser.Chromium.Win-x86`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x86/)<br>
[`DotNetBrowser.Chromium.Win-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x64/)<br>
[`DotNetBrowser.Chromium.Win-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-arm64/)<br>
[`DotNetBrowser.WinUi3`](https://www.nuget.org/packages/DotNetBrowser.WinUi3/)

**Note**
Installing `DotNetBrowser.WinUi3` fetches the rest required packages.


**Note**
If your WinUi3 application runs on 32-bit platforms, and 64-bit platforms are not supported, you can install [`DotNetBrowser.WinUi3.x86`](https://www.nuget.org/packages/DotNetBrowser.WinUi3.x86/) package. `DotNetBrowser.Win-x86`, `DotNetBrowser.Chromium.Win-x86` packages are fetched and installed automatically.


**Note**
If your WinUi3 application runs on ARM64 platforms, you can install [`DotNetBrowser.WinUi3.arm64`](https://www.nuget.org/packages/DotNetBrowser.WinUi3.arm64/) package. `DotNetBrowser.Win-arm64`, `DotNetBrowser.Chromium.Win-arm64` packages are fetched and installed automatically.


### Avalonia UI

[`DotNetBrowser.CrossPlatform`](https://www.nuget.org/packages/DotNetBrowser.CrossPlatform/)<br>
[`DotNetBrowser.Chromium.Win-x86`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x86/)<br>
[`DotNetBrowser.Chromium.Win-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-x64/)<br>
[`DotNetBrowser.Chromium.Win-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Win-arm64/)<br>
[`DotNetBrowser.Chromium.Linux-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Linux-x64/)<br>
[`DotNetBrowser.Chromium.Linux-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.Linux-arm64/)<br>
[`DotNetBrowser.Chromium.macOS-x64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.macOS-x64/)<br>
[`DotNetBrowser.Chromium.macOS-arm64`](https://www.nuget.org/packages/DotNetBrowser.Chromium.macOS-arm64/)<br>
[`DotNetBrowser.AvaloniaUi`](https://www.nuget.org/packages/DotNetBrowser.AvaloniaUi/)<br>
OR<br>
[`DotNetBrowser.AvaloniaUi.v12`](https://www.nuget.org/packages/DotNetBrowser.AvaloniaUi.v12/)<br>

**Note**
Installing `DotNetBrowser.AvaloniaUi` or `DotNetBrowser.AvaloniaUi.v12` fetches the rest required packages.


**Note**
If your Avalonia UI application runs on a certain subset of the platforms only, and the other platforms are not supported, you can later exclude the corresponding `DotNetBrowser.Chromium.Xxx` DLLs when preparing your application for deployment.


## NuGet Package Manager in Visual Studio

To install the required NuGet packages, follow the below instructions:

1. In **Solution Explorer**, right-click **References** and choose **Manage NuGet Packages**:

    ![Manage NuGet Packages](https://teamdev.com/dotnetbrowser/img/articles/installation/nuget/manage_nuget.webp)

2. Choose "nuget.org" as the **Package source**, select the **Browse** tab, search for "DotNetBrowser", select the required package and hit **Install**:

    ![Install package](https://teamdev.com/dotnetbrowser/img/articles/installation/nuget/install_nuget_package.webp)

3. Accept the prompted license agreement to continue installation.

## Install NuGet Packages using the dotnet CLI

To install the required NuGet packages, follow the below instructions:

1. Open a command line and switch to the directory that contains your project file.

2. Run  the following command to install the needed package:
```
dotnet add package <DotNetBrowser_package_name>
```
3. After the command completes, the package reference will appear in the `.csproj` file.

For additional information visit the following [link](https://learn.microsoft.com/en-us/nuget/consume-packages/install-use-packages-dotnet-cli)
