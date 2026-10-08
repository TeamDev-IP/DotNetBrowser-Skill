
# DotNetBrowser in WinUI 3

**Lead**
This guide shows how to start working with DotNetBrowser and embed it in a simple WinUI 3 application.


Before you begin make sure that your system meets [software and hardware requirements](https://teamdev.com/dotnetbrowser/docs/guides/requirements/).

## 1. Install DotNetBrowser templates

Open the Command Line prompt, and install DotNetBrowser templates if not installed yet:

```bash
dotnet new install DotNetBrowser.Templates
```

After installation, the template projects will be available in both .NET CLI and Visual Studio.

## 2. Get trial license

To get a free 30-day trial license, fill in the [web form](https://teamdev.com/dotnetbrowser#evaluate) and click the **Get my free trial** button. You will receive an email with the license key.

## 3. Create a WinUI 3 application with DotNetBrowser

Create a new application:

```bash
dotnet new dotnetbrowser.winui.app -o Example.WinUi -li <your_license_key>
```

The project will be created in the folder `Example.WinUi`.

By default, this project will target `net8.0`. Use `-f` option to specify `net10.0`, `net9.0`, `net7.0`, or `net6.0` instead.

The DotNetBrowser agent skill tells AI coding agents how to write code with
DotNetBrowser. To add it to the project, use the `--agent` option with
`ClaudeCode`, `Codex`, `Cursor`, or `Copilot`. Building the project copies the
skill to the agent's skills directory in the project folder. For other ways to
install the skill, see [Installing the agent skill][guides-agent-skill].

## 4. Run the application

To launch application, use:

```bash
dotnet run --project Example.WinUi
```

![WinUI 3](https://teamdev.com/dotnetbrowser/img/articles/quickstart/winui3/winui3.webp)

[guides-agent-skill]: https://teamdev.com/dotnetbrowser/docs/guides/installation/agent-skill/
