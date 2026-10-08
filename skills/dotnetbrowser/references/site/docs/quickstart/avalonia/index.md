
# DotNetBrowser in Avalonia UI

**Lead**
This guide shows how to embed DotNetBrowser into a cross-platform desktop application created with Avalonia 11.


Before you begin make sure that your system meets [software and hardware requirements](https://teamdev.com/dotnetbrowser/docs/guides/requirements/).

## 1. Install DotNetBrowser templates

Open the Terminal or Command Line prompt, and install DotNetBrowser templates if not installed yet:

```bash
dotnet new install DotNetBrowser.Templates
```

For .NET 6.0, use a slightly different command:

```bash
dotnet new --install DotNetBrowser.Templates
```

After installation, the template projects will be available in both .NET CLI and Visual Studio.

## 2. Get trial license

To get a free 30-day trial license, fill in the [web form](https://teamdev.com/dotnetbrowser#evaluate) and click the **Get my free trial** button. You will receive an email with the license key.

## 3. Create Avalonia app with DotNetBrowser

Create a new application:


**C#**
```bash
dotnet new dotnetbrowser.avalonia.app -o Embedding.AvaloniaUi -li <your_license_key>
```

**VB**
```bash
dotnet new dotnetbrowser.avalonia.app -o Embedding.AvaloniaUi -lang VisualBasic -li <license_key>
```



The project will be created in the folder `Embedding.AvaloniaUi`.

By default, this project will target `net8.0`. Use `-f` option to specify `net10.0` or `net9.0` instead.

The DotNetBrowser agent skill tells AI coding agents how to write code with
DotNetBrowser. To add it to the project, use the `--agent` option with
`ClaudeCode`, `Codex`, `Cursor`, or `Copilot`. Building the project copies the
skill to the agent's skills directory in the project folder. For other ways to
install the skill, see [Installing the agent skill][guides-agent-skill].

## 4. Run your application

Finally, launch the application by running the following command in the terminal:

```bash
dotnet run --project Embedding.AvaloniaUi
```

Here’s how the result will look on different platforms:

![DotNetBrowser and Avalonia on Windows](https://teamdev.com/dotnetbrowser/img/articles/quickstart/avalonia/windows.webp)
**Image-Caption**
DotNetBrowser + Avalonia on Windows


![DotNetBrowser and Avalonia on macOS](https://teamdev.com/dotnetbrowser/img/articles/quickstart/avalonia/macos.webp)
**Image-Caption**
DotNetBrowser + Avalonia on macOS
<br>

![DotNetBrowser and Avalonia on Linux](https://teamdev.com/dotnetbrowser/img/articles/quickstart/avalonia/linux.webp)
**Image-Caption**
DotNetBrowser + Avalonia on Linux


[guides-agent-skill]: https://teamdev.com/dotnetbrowser/docs/guides/installation/agent-skill/
