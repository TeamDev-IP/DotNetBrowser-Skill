
# Installing from ZIP

**Lead**
This guide describes how to add DotNetBrowser downloaded in ZIP archive to .NET project.


To include DotNetBrowser into your project, download the required archive, extract assemblies and include them into your project.

[Download DotNetBrowser 4.3.3 (.NET Framework)](https://teamdev.download/downloads/dotnetbrowser/4.3.3/dotnetbrowser-net462-4.3.3.zip)<br>
[Download DotNetBrowser 4.3.3 (.NET Core)](https://teamdev.download/downloads/dotnetbrowser/4.3.3/dotnetbrowser-netcore30-4.3.3.zip)<br>
[Download DotNetBrowser 4.3.3 (Cross-platform)](https://teamdev.download/downloads/dotnetbrowser/4.3.3/dotnetbrowser-netstandard20-4.3.3.zip)

## Assemblies list

The library consists of the following assemblies:
* `DotNetBrowser.dll` &mdash; data classes and interfaces;
* `DotNetBrowser.Core.dll` &mdash; the core implementation;
* `DotNetBrowser.Logging.dll` &mdash; the DotNetBrowser Logging API implementation;
* `DotNetBrowser.WinForms.dll` &mdash; the classes and interfaces for embedding into a WinForms app;
* `DotNetBrowser.Wpf.dll` &mdash; the classes and interfaces for embedding into a WPF app;
* `DotNetBrowser.AvaloniaUi.dll` &mdash; the classes and interfaces for embedding into an Avalonia 11 app;
* `DotNetBrowser.AvaloniaUi.v12.dll` &mdash; the classes and interfaces for embedding into an Avalonia 12 app;
* `DotNetBrowser.Chromium.Win-x86.dll` &mdash; the Chromium 32-bit binaries for Windows;
* `DotNetBrowser.Chromium.Win-x64.dll` &mdash; the Chromium 64-bit binaries for Windows;
* `DotNetBrowser.Chromium.Win-arm64.dll` &mdash; the Chromium ARM64 binaries for Windows;
* `DotNetBrowser.Chromium.Linux-x64.dll` &mdash; the Chromium 64-bit binaries for Linux;
* `DotNetBrowser.Chromium.Linux-arm64.dll` &mdash; the Chromium ARM64 binaries for Linux;
* `DotNetBrowser.Chromium.macOS-x64.dll` &mdash; the Chromium 64-bit binaries for macOS.
* `DotNetBrowser.Chromium.macOS-arm64.dll` &mdash; the Chromium ARM64 binaries for macOS.

DotNetBrowser itself depends on [Google.Protobuf](https://www.nuget.org/packages/Google.Protobuf), and you can find the corresponding assemblies in the distribution archive.

### Platform-specific
If you need DotNetBrowser to work only on a specific platform, you can add the appropriate assemblies to the project references listed below.

**Note**
If your application runs only on 64-bit platforms, and you do not need to support 32-bit platform, you can add only 64-bit binaries.


#### Cross Platform

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Win-x86.dll`<br>
`DotNetBrowser.Chromium.Win-x64.dll`<br>
`DotNetBrowser.Chromium.Win-arm64.dll`<br>
`DotNetBrowser.Chromium.Linux-x64.dll`<br>
`DotNetBrowser.Chromium.Linux-arm64.dll`<br>
`DotNetBrowser.Chromium.macOS-x64.dll`<br>
`DotNetBrowser.Chromium.macOS-arm64.dll`

#### Windows AnyCPU

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Win-x86.dll`<br>
`DotNetBrowser.Chromium.Win-x64.dll`<br>
`DotNetBrowser.Chromium.Win-arm64.dll`

#### Windows x86

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Win-x86.dll`

#### Windows x64

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Win-x64.dll`

#### Windows ARM64

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Win-arm64.dll`

#### Linux x64

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Linux-x64.dll`

#### Linux ARM64

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Linux-arm64.dll`

#### macOS x64

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.macOS-x64.dll`

#### macOS ARM64

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.macOS-arm64.dll`

### UI framework

If you develop a desktop application where you want to display some web content, add one more assembly to your project references depending on the UI framework you use.

#### WPF

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Win-x86.dll`<br>
`DotNetBrowser.Chromium.Win-x64.dll`<br>
`DotNetBrowser.Chromium.Win-arm64.dll`<br>
`DotNetBrowser.Wpf.dll`

**Note**
If your WPF application runs on 64-bit platforms, and 32-bit ones are not supported, it is enough to reference only `DotNetBrowser.Chromium.Win-x64.dll` along with the rest above-mentioned assemblies.


#### WinForms

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Win-x86.dll`<br>
`DotNetBrowser.Chromium.Win-x64.dll`<br>
`DotNetBrowser.Chromium.Win-arm64.dll`<br>
`DotNetBrowser.WinForms.dll`

**Note**
If your WinForms application runs on 32-bit platforms, and 64-bit platforms are not supported, it is enough to reference `DotNetBrowser.WinForms.x86.dll` along with the rest above-mentioned assemblies.


#### Avalonia UI

`DotNetBrowser.dll`<br>
`DotNetBrowser.Core.dll`<br>
`DotNetBrowser.Logging.dll`<br>
`DotNetBrowser.Chromium.Win-x86.dll`<br>
`DotNetBrowser.Chromium.Win-x64.dll`<br>
`DotNetBrowser.Chromium.Win-arm64.dll`<br>
`DotNetBrowser.Chromium.Linux-x64.dll`<br>
`DotNetBrowser.Chromium.Linux-arm64.dll`<br>
`DotNetBrowser.Chromium.macOS-x64.dll`<br>
`DotNetBrowser.Chromium.macOS-arm64.dll`<br>
`DotNetBrowser.AvaloniaUi.dll`<br>
OR<br>
`DotNetBrowser.AvaloniaUi.v12.dll`<br>

**Note**
If your Avalonia UI application runs on a certain platform only, and the other platforms are not supported, it is enough to reference the `DotNetBrowser.Chromium.Xxx` DLL for that platform only.


## Adding referenced assemblies to project

1. In **Solution Explorer**, right-click **References** and select the **Add Reference...** menu item:

    ![Add Reference](https://teamdev.com/dotnetbrowser/img/articles/installation/assemblies/add-reference.webp)

2. In the opened **Reference Manager** dialog, click the **Browse...** button:

    ![Browse](https://teamdev.com/dotnetbrowser/img/articles/installation/assemblies/browse-button.webp)

3. Select the desired assemblies and click **Add**: 

    ![Select Assemblies](https://teamdev.com/dotnetbrowser/img/articles/installation/assemblies/select-assemblies.webp)

4. Double-check all selected references are added and appear in the **Reference Manager** dialog and click **OK**:

    ![Confirm Reference](https://teamdev.com/dotnetbrowser/img/articles/installation/assemblies/confirm-reference.webp)

**Note**
Adding `DotNetBrowser.Chromium.xx-yy.dll` is optional; `DotNetBrowser.Chromium.xx-yy.dll` is found automatically if it is located in the same folder as DotNetBrowser.dll.

