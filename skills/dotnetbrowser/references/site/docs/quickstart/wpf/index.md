
# DotNetBrowser in WPF

**Lead**
This guide shows how to start working with DotNetBrowser and embed it in a simple WPF application.


Before you begin make sure that your system meets [software and hardware requirements](https://teamdev.com/dotnetbrowser/docs/guides/requirements/).

## .NET 6 and higher

### 1. Install DotNetBrowser templates

Open the Command Line prompt, and install DotNetBrowser templates if not installed yet:

```bash
dotnet new install DotNetBrowser.Templates
```

After installation, the template projects will be available in both .NET CLI and Visual Studio.

### 2. Get trial license

To get a free 30-day trial license, fill in the [web form](https://teamdev.com/dotnetbrowser#evaluate) and click the **Get my free trial** button. You will receive an email with the license key.

### 3. Create a WPF application with DotNetBrowser

Create a new application:


**C#**
```bash
dotnet new dotnetbrowser.wpf.app -o Example.Wpf -li <your_license_key>
```

**VB**
```bash
dotnet new dotnetbrowser.wpf.app -o Example.Wpf -lang VisualBasic -li <license_key>
```



The project will be created in the folder `Example.Wpf`.

By default, this project will target `net8.0`. Use `-f` option to specify `net10.0` or `net9.0` instead.

The DotNetBrowser agent skill tells AI coding agents how to write code with
DotNetBrowser. To add it to the project, use the `--agent` option with
`ClaudeCode`, `Codex`, `Cursor`, or `Copilot`. Building the project copies the
skill to the agent's skills directory in the project folder. For other ways to
install the skill, see [Installing the agent skill][guides-agent-skill].

### 4. Run the application

To launch application, use:

```bash
dotnet run --project Example.Wpf
```
![Application Launch](https://teamdev.com/dotnetbrowser/img/articles/guides/browserview/wpf-view.webp)

## .NET Framework

### 1. Create a WPF application

Create a new `Embedding.Wpf` WPF Application C# Project or WPF Application Visual Basic Project:

![WPF Project](https://teamdev.com/dotnetbrowser/img/articles/quickstart/wpf/wpf-project.webp)

### 2. Add DotNetBrowser to project

In the **Solution Explorer**, right-click **References** and select the **Manage NuGet Packages** option:

![Manage NuGet Packages](https://teamdev.com/dotnetbrowser/img/articles/quickstart/wpf/manage-nuget.webp)

Choose "nuget.org" as the **Package source**, select the **Browse** tab, search for "DotNetBrowser", select the **DotNetBrowser.Wpf** package and hit **Install**:

![WPF package](https://teamdev.com/dotnetbrowser/img/articles/quickstart/wpf/wpf-package.webp)

Accept license prompt to continue installation.

### 3. Change the source code

Insert the following code into the **MainWindow.xaml** file:


```xml
﻿<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:WPF="clr-namespace:DotNetBrowser.Wpf;assembly=DotNetBrowser.Wpf"
    x:Class="Embedding.Wpf.MainWindow"
    mc:Ignorable="d"
    Title="DotNetBrowser — WPF" Height="480" Width="800" Closed="Window_Closed">
    <Grid>
        <WPF:BrowserView Name="browserView" />
    </Grid>
</Window>
```

Use the code sample below for the 
<span class="code-tab-content inline" lang="C#">[**MainWindow.xaml.cs**](https://github.com/TeamDev-IP/DotNetBrowser-QuickStart/blob/v4/csharp/Embedding.Wpf/MainWindow.xaml.cs)</span>
<span class="code-tab-content inline" lang="VB">[**MainWindow.xaml.vb**](https://github.com/TeamDev-IP/DotNetBrowser-QuickStart/blob/v4/vbnet/Embedding.Wpf/MainWindow.xaml.vb)</span>
 file:


**C#**

```csharp
using System;
using System.Windows;
using DotNetBrowser.Browser;
using DotNetBrowser.Engine;

namespace Embedding.Wpf
{
    /// <summary>
    ///     This example demonstrates how to embed DotNetBrowser
    ///     into a WPF application.
    /// </summary>
    public partial class MainWindow : Window
    {
        private const string Url = "https://html5test.teamdev.com/";
        private readonly IBrowser browser;
        private readonly IEngine engine;

        public MainWindow()
        {
            // Create and initialize the IEngine instance.
            EngineOptions engineOptions = new EngineOptions.Builder
            {
                RenderingMode = RenderingMode.HardwareAccelerated
            }.Build();
            engine = EngineFactory.Create(engineOptions);

            // Create the IBrowser instance.
            browser = engine.CreateBrowser();

            InitializeComponent();

            // Initialize the WPF BrowserView control.
            browserView.InitializeFrom(browser);
            browser.Navigation.LoadUrl(Url);
        }

        private void Window_Closed(object sender, EventArgs e)
        {
            browser?.Dispose();
            engine?.Dispose();
        }
    }
}
```

**VB**

```vb
Imports System.Windows
Imports DotNetBrowser.Browser
Imports DotNetBrowser.Engine

Namespace Embedding.Wpf
    ''' <summary>
    '''     This example demonstrates how to embed DotNetBrowser
    '''     into a WPF application.
    ''' </summary>
    Partial Public Class MainWindow
        Inherits Window

        Private Const Url As String = "https://html5test.teamdev.com/"
        Private ReadOnly browser As IBrowser
        Private ReadOnly engine As IEngine

        Public Sub New()
            ' Create and initialize the IEngine instance.
            Dim engineOptions As EngineOptions = New EngineOptions.Builder With {
                .RenderingMode = RenderingMode.HardwareAccelerated
            }.Build()
            engine = EngineFactory.Create(engineOptions)

            ' Create the IBrowser instance.
            browser = engine.CreateBrowser()

            InitializeComponent()

            ' Initialize the WPF BrowserView control.
            browserView.InitializeFrom(browser)
            browser.Navigation.LoadUrl(Url)
        End Sub

        Private Sub Window_Closed(sender As Object, e As EventArgs)
            browser?.Dispose()
            engine?.Dispose()
        End Sub
    End Class
End Namespace
```



The complete project is available in our repository: [C#](https://github.com/TeamDev-IP/DotNetBrowser-QuickStart/tree/v4/csharp/Embedding.Wpf), [VB](https://github.com/TeamDev-IP/DotNetBrowser-QuickStart/tree/v4/vbnet/Embedding.Wpf).

### 4. Get trial license

To get a free 30-day trial license, fill the [web form](https://teamdev.com/dotnetbrowser#evaluate) and click the **Get my free trial** button. You will receive an email with the license key.

### 5. Add license

To embed the license key into your project, copy the license key string from the email and insert it as shown below:


**C#**
```csharp
EngineOptions engineOptions = new EngineOptions.Builder
{
    RenderingMode = RenderingMode.HardwareAccelerated,
    LicenseKey = "your_license_key"
}.Build();
```

**VB**
```vb
Dim engineOptions As EngineOptions = New EngineOptions.Builder With {
    .RenderingMode = RenderingMode.HardwareAccelerated,
    .LicenseKey = "your_license_key"
}.Build()
```



For more information on license installation, refer to this [article](https://teamdev.com/dotnetbrowser/docs/guides/installation/license/).

### 6. Run the application

To run the application, press **F5** or click the **Start** button on the toolbar. The **MainWindow** opens:

![Application Launch](https://teamdev.com/dotnetbrowser/img/articles/guides/browserview/wpf-view.webp)

[guides-agent-skill]: https://teamdev.com/dotnetbrowser/docs/guides/installation/agent-skill/
