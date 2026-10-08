
# DotNetBrowser in WinForms

**Lead**
This guide shows how to start working with DotNetBrowser and embed it in a simple WinForms application.


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

### 3. Create a Windows Forms application with DotNetBrowser

Create a new application:


**C#**
```bash
dotnet new dotnetbrowser.winforms.app -o Example.WinForms -li <your_license_key>
```

**VB**
```bash
dotnet new dotnetbrowser.winforms.app -o Example.WinForms -lang VisualBasic -li <license_key>
```



The project will be created in the folder `Example.WinForms`.

By default, this project will target `net8.0`. Use `-f` option to specify `net10.0` or `net9.0` instead.

The DotNetBrowser agent skill tells AI coding agents how to write code with
DotNetBrowser. To add it to the project, use the `--agent` option with
`ClaudeCode`, `Codex`, `Cursor`, or `Copilot`. Building the project copies the
skill to the agent's skills directory in the project folder. For other ways to
install the skill, see [Installing the agent skill][guides-agent-skill].

### 4. Run the application

To launch application, use:

```bash
dotnet run --project Example.WinForms
```
![Application Launch](https://teamdev.com/dotnetbrowser/img/articles/guides/browserview/winforms-view.webp)

## .NET Framework

### 1. Create a Windows Forms application

Create a new `Embedding.WinForms` WinForms Application C# Project or WinForms Application Visual Basic Project:

![Winforms Project](https://teamdev.com/dotnetbrowser/img/articles/quickstart/winforms/winforms-project.webp)

### 2. Add DotNetBrowser to project.

In the **Solution Explorer**, right-click **References** and select the **Manage NuGet Packages** option:

![Manage NuGet Packages](https://teamdev.com/dotnetbrowser/img/articles/quickstart/winforms/manage-nuget.webp)

Choose "nuget.org" as the **Package source**, select the **Browse** tab, search for "DotNetBrowser", select the **DotNetBrowser.WinForms** package and hit **Install**:

![WinForms package](https://teamdev.com/dotnetbrowser/img/articles/quickstart/winforms/winforms-package.webp)

Accept license prompt to continue installation.

### 3. Change the source code

Insert the following code into the 
<span class="code-tab-content inline" lang="C#">**Form1.cs**</span>
<span class="code-tab-content inline" lang="VB">**Form1.vb**</span>
 file:


**C#**

```csharp
using System.Windows.Forms;
using DotNetBrowser.Browser;
using DotNetBrowser.Engine;
using DotNetBrowser.WinForms;

namespace Embedding.WinForms
{
    /// <summary>
    ///     This example demonstrates how to embed DotNetBrowser
    ///     into a Windows Forms application.
    /// </summary>
    public partial class Form1 : Form
    {
        private const string Url = "https://html5test.teamdev.com/";
        private readonly IBrowser browser;
        private readonly IEngine engine;

        public Form1()
        {
            // Create the Windows Forms BrowserView control.
            BrowserView browserView = new BrowserView
            {
                Dock = DockStyle.Fill
            };

            // Create and initialize the IEngine instance.
            EngineOptions engineOptions = new EngineOptions.Builder
            {
                RenderingMode = RenderingMode.HardwareAccelerated
            }.Build();
            engine = EngineFactory.Create(engineOptions);

            // Create the IBrowser instance.
            browser = engine.CreateBrowser();

            InitializeComponent();

            // Add the BrowserView control to the Form.
            Controls.Add(browserView);
            FormClosed += Form1_FormClosed;

            // Initialize the Windows Forms BrowserView control.
            browserView.InitializeFrom(browser);
            browser.Navigation.LoadUrl(Url);
        }

        private void Form1_FormClosed(object sender, FormClosedEventArgs e)
        {
            browser?.Dispose();
            engine?.Dispose();
        }
    }
}
```

**VB**

```vb
Imports System.Windows.Forms
Imports DotNetBrowser.Browser
Imports DotNetBrowser.Engine
Imports DotNetBrowser.WinForms

Namespace Embedding.WinForms
    ''' <summary>
    '''     This example demonstrates how to embed DotNetBrowser
    '''     into a Windows Forms application.
    ''' </summary>
    Partial Public Class Form1
        Inherits Form

        Private Const Url As String = "https://html5test.teamdev.com/"
        Private ReadOnly browser As IBrowser
        Private ReadOnly engine As IEngine

        Public Sub New()
            ' Create the Windows Forms BrowserView control.
            Dim browserView As New BrowserView With {.Dock = DockStyle.Fill}

            ' Create and initialize the IEngine instance.
            Dim engineOptions As EngineOptions = New EngineOptions.Builder With {
                .RenderingMode = RenderingMode.HardwareAccelerated
            }.Build()
            engine = EngineFactory.Create(engineOptions)

            ' Create the IBrowser instance.
            browser = engine.CreateBrowser()

            InitializeComponent()

            ' Add the BrowserView control to the Form.
            Controls.Add(browserView)
            AddHandler FormClosed, AddressOf Form1_FormClosed

            ' Initialize the Windows Forms BrowserView control.
            browserView.InitializeFrom(browser)
            browser.Navigation.LoadUrl(Url)
        End Sub

        Private Sub Form1_FormClosed(sender As Object, e As FormClosedEventArgs)
            browser?.Dispose()
            engine?.Dispose()
        End Sub
    End Class
End Namespace
```



The complete project is available in our repository: [C#](https://github.com/TeamDev-IP/DotNetBrowser-QuickStart/tree/v4/csharp/Embedding.WinForms), [VB](https://github.com/TeamDev-IP/DotNetBrowser-QuickStart/tree/v4/vbnet/Embedding.WinForms).

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

To run the application, press **F5** or click the **Start** button on the toolbar. The **Form1** window opens:

![Application Launch](https://teamdev.com/dotnetbrowser/img/articles/guides/browserview/winforms-view.webp)

[guides-agent-skill]: https://teamdev.com/dotnetbrowser/docs/guides/installation/agent-skill/
