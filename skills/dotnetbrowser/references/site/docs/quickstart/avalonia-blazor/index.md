
# DotNetBrowser in Blazor Hybrid Avalonia app

**Lead**
This guide shows how to create a Blazor Hybrid cross-platform desktop application with Avalonia 11 and DotNetBrowser.


Before you begin make sure that your system meets [software and hardware requirements](https://teamdev.com/dotnetbrowser/docs/guides/requirements/).

## 1. Install DotNetBrowser templates

Open the Terminal or Command Line prompt, and install DotNetBrowser templates if not installed yet:

```bash
dotnet new install DotNetBrowser.Templates
```

After installation, the template projects will be available in both dotnet CLI and Visual Studio.

## 2. Get trial license

To get a free 30-day trial license, fill in the [web form](https://teamdev.com/dotnetbrowser#evaluate) and click the **Get my free trial** button. You will receive an email with the license key.

## 3. Create Blazor Hybrid Avalonia application from template

Create a new application:

```bash
dotnet new dotnetbrowser.blazor.avalonia.app -o BlazorHybrid.AvaloniaUi -li <license_key>
```

The project will be created in the folder `BlazorHybrid.AvaloniaUi`.

By default, this project will target `net8.0`. Use `-f` option to specify `net10.0` or `net9.0` instead.

The DotNetBrowser agent skill tells AI coding agents how to write code with
DotNetBrowser. To add it to the project, use the `--agent` option with
`ClaudeCode`, `Codex`, `Cursor`, or `Copilot`. Building the project copies the
skill to the agent's skills directory in the project folder. For other ways to
install the skill, see [Installing the agent skill][guides-agent-skill].

## 4. Run your application

Finally, launch the application by running the following command in the terminal:

```bash
dotnet run --project BlazorHybrid.AvaloniaUi
```

Here’s how the result will look on different platforms:

![DotNetBrowser and Avalonia on Windows](https://teamdev.com/dotnetbrowser/img/articles/quickstart/avalonia/windows-blazor.webp)
**Image-Caption**
DotNetBrowser + Avalonia + Blazor on Windows


![DotNetBrowser and Avalonia on macOS](https://teamdev.com/dotnetbrowser/img/articles/quickstart/avalonia/macos-blazor.webp)
**Image-Caption**
DotNetBrowser + Avalonia + Blazor on macOS
<br>

![DotNetBrowser and Avalonia on Linux](https://teamdev.com/dotnetbrowser/img/articles/quickstart/avalonia/linux-blazor.webp)
**Image-Caption**
DotNetBrowser + Avalonia + Blazor on Linux


[guides-agent-skill]: https://teamdev.com/dotnetbrowser/docs/guides/installation/agent-skill/
