
# Installing from VSIX

**Lead**
This guide describes how to add DotNetBrowser BrowserView control to Visual Studio ToolBox.


## WinForms

To add the DotNetBrowser BrowserView control to the Visual Studio Toolbox, download and install the required VSIX package:

[DotNetBrowser](https://teamdev.download/downloads/dotnetbrowser/4.3.3/vsix/DotNetBrowser.WinForms.Package.vsix)<br>
[DotNetBrowser x64](https://teamdev.download/downloads/dotnetbrowser/4.3.3/vsix/DotNetBrowser.WinForms.x64.Package.vsix)<br>
[DotNetBrowser x86](https://teamdev.download/downloads/dotnetbrowser/4.3.3/vsix/DotNetBrowser.WinForms.x86.Package.vsix)<br>
[DotNetBrowser ARM64](https://teamdev.download/downloads/dotnetbrowser/4.3.3/vsix/DotNetBrowser.WinForms.arm64.Package.vsix)

After completing installation, the BrowserView control will appear in the VS ToolBox and can be dragged and dropped onto the form:

![WinForms ToolBox](https://teamdev.com/dotnetbrowser/img/articles/installation/vsix/vsix-winforms.webp)

**Note**
BrowserView control also appears in the VS ToolBox after installing the corresponding [`DotNetBrowser.WinForms`](https://teamdev.com/dotnetbrowser/docs/guides/installation/nuget/#nuget-package-manager-in-visual-studio) NuGet package.


## WPF

There is no VSIX package for WPF applications.
To add the DotNetBrowser BrowserView control to the Visual Studio Toolbox, install the appropriate [`DotNetBrowser.Wpf`](https://teamdev.com/dotnetbrowser/docs/guides/installation/nuget/#nuget-package-manager-in-visual-studio) NuGet package.

After installing the above package, you will see BrowserView control in VS ToolBox. It can be dragged and dropped onto the Grid:

![WPF ToolBox](https://teamdev.com/dotnetbrowser/img/articles/installation/vsix/vsix-wpf.webp)
