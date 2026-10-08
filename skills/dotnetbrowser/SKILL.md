---
name: dotnetbrowser
description: Use when writing, reviewing, or debugging .NET code that embeds a Chromium browser with DotNetBrowser (WPF, Windows Forms, WinUI 3, Avalonia UI, or headless/console) - choosing NuGet packages, engine and browser lifecycle, BrowserView, handlers and events, navigation, DOM, JavaScript bridge, printing, network interception, deployment, licensing, and API lookups. Bundles API references and an offline snapshot of the guides, release notes, migration guides, and blog for DotNetBrowser 4.3.3.
metadata:
  product: DotNetBrowser
  product-version: "4.3.3"
  chromium-version: "155.0.8059.40"
  generated: "2026-10-08"
---

# DotNetBrowser

DotNetBrowser is a commercial .NET library from TeamDev that embeds a
Chromium-based web browser into .NET applications. It renders web pages built
with HTML5, CSS3, and JavaScript and gives programmatic access to the browser,
the DOM, JavaScript, the network, printing, and more. Using it requires a
license key; a free 30-day evaluation license is available from
https://www.teamdev.com/dotnetbrowser#evaluate.

This skill describes DotNetBrowser 4.3.3 (Chromium
155.0.8059.40). Everything here was generated from the product on
2026-10-08. Prefer the bundled references over memory: the API changes
between major versions, and code written for DotNetBrowser 1.x or 2.x is
mostly wrong for 4.x.

## What is in this skill

Paths in this skill are relative to the skill folder, the one that holds this
file.

| Path | Use it for |
| --- | --- |
| `references/<topic>.md` | Detailed rules for one area; see "Topic notes" below. |
| `references/api/INDEX.md` | Find a covered public type: namespace, kind, one-line summary, file name. |
| `references/api/<Namespace>.<Type>.md` | Complete members of one type (587 types): signatures, remarks, parameters. |
| `references/site/INDEX.md` | Find a guide, quick start, tutorial, release note, migration guide, or blog post. |
| `references/site/**/index.md` | The pages themselves (137 pages), with C# and VB.NET samples. |
| `references/site/llms.txt` | The same list with live URLs, for when a newer page might exist online. |

Workflow for most tasks:

1. Check the project's DotNetBrowser package version, target framework, and UI
   framework version (including centrally managed package versions). Preserve
   them unless the task calls for an upgrade. If the package version differs
   from 4.3.3, verify APIs against that version's documentation
   or installed assemblies before using these references.
2. Read every topic note below that matches the task.
3. Search `references/site/INDEX.md` for the needed topic, then read the
   relevant guide sections. Guides are the source of truth for *how* to use
   the API, except where a topic note contradicts them: notes carry
   corrections that the guides may not have yet.
4. Before the first API lookup, read `references/lookup.md`: it explains file
   names and what the API reference does not cover. Then search
   `references/api/INDEX.md` for the types the guide mentions and read the
   relevant sections for exact signatures and overloads.
5. If tool output is truncated, retrieve the missing sections before relying
   on it.
6. Write code that follows the guide's sample; do not invent members.

## Topic notes

Each note holds rules that agents got wrong without it. Before writing or
reviewing code in an area, read its note; the short rules in this file do not
replace it.

| Before you | Read |
| --- | --- |
| Choose packages, create a project, or target Avalonia, headless Linux, or Docker | [references/project-setup.md](references/project-setup.md) |
| Create, configure, or dispose an engine, profile, or browser | [references/engine-and-browser.md](references/engine-and-browser.md) |
| Show a browser in WPF, Windows Forms, WinUI 3, or Avalonia, or shut such an app down | [references/browser-view.md](references/browser-view.md) |
| Assign a handler, subscribe to an event, or update UI from either | [references/handlers-and-threading.md](references/handlers-and-threading.md) |
| Load a page or decide whether a navigation succeeded | [references/navigation.md](references/navigation.md) |
| Run JavaScript, read its result, or expose .NET objects to it | [references/javascript.md](references/javascript.md) |
| Look up an API type or guide, follow a link inside a page, or upgrade versions | [references/lookup.md](references/lookup.md) |
| Diagnose a startup failure, blank view, hang, or crash | [references/troubleshooting.md](references/troubleshooting.md) |

## Choosing packages

For a desktop application, install the package for the UI framework. It
fetches the engine and the Chromium binaries, so one package is enough:

| UI framework | Package |
| --- | --- |
| WPF | `DotNetBrowser.Wpf` |
| Windows Forms | `DotNetBrowser.WinForms` |
| WinUI 3 | `DotNetBrowser.WinUi3` |
| Avalonia UI 11.2 up to, but excluding, 12 | `DotNetBrowser.AvaloniaUi` |
| Avalonia UI 12.x (.NET 8 or later) | `DotNetBrowser.AvaloniaUi.v12` |

For a console, service, or headless application, install one engine package:

| Target platforms | Package |
| --- | --- |
| Windows, any CPU | `DotNetBrowser` |
| Windows, Linux, and macOS | `DotNetBrowser.CrossPlatform` |
| One platform only | `DotNetBrowser.Win-x64`, `DotNetBrowser.Linux-arm64`, `DotNetBrowser.macOS-arm64`, and so on |

Avalonia apps on Windows also need the DotNetBrowser template's `app.manifest`;
templates, single-platform packages, and supported runtimes are in
`references/project-setup.md`.

## Core rules

- Create the engine with `EngineFactory.Create(...)` (or `CreateAsync`) and a
  browser with `engine.Profiles.Default.CreateBrowser()`. `IBrowser` is not a
  visual control: show it in a `BrowserView` with
  `browserView.InitializeFrom(browser)` on the UI thread, which needs
  `using DotNetBrowser.Browser;`.
- Call `Dispose()` on what you created that implements `IDisposable` (the
  engine, browsers); never on `IAutoDisposable`-only objects such as
  `IProfile` or `IFrame`. Views never dispose the browser or engine; an
  undisposed engine keeps the application alive.
- `LoadResult.Completed` from `LoadUrl` means the main frame fired its `load`
  event. It does not mean that content added by scripts is there or that HTTP
  succeeded. `NavigationResult` has no status code: check `ResponseCode` from
  the `NavigationFinished` event too. Waiting for content and tracking status
  from events have more traps; see `references/navigation.md`.
- `ExecuteJavaScript<T>` casts, not converts: JavaScript numbers are `double`,
  and `null`/`undefined` need a nullable `T` such as `double?`.
- A handler property holds one handler; an async handler must complete its
  task. Handlers and events almost always run off the UI thread: check thread
  access and post UI updates without blocking (`Dispatcher.BeginInvoke` in
  WPF, `Control.BeginInvoke` in Windows Forms, `DispatcherQueue.TryEnqueue`
  in WinUI 3, `Dispatcher.UIThread.Post` in Avalonia); never block a handler
  on `Invoke`. Some handlers forbid calls back into the
  browser or engine; check their API remarks.
- If the window can close while `CreateAsync` is running, do not dispose the
  arriving engine in code after `await` on the UI thread: after the last window
  closes, that code may never run (WPF by default, WinUI 3). See
  `references/engine-and-browser.md` and, for WinUI 3,
  `references/browser-view.md`.
- The API reference has no separate pages for `DotNetBrowser.AvaloniaUi.v12`.
  Use the Avalonia UI 11 pages; members that come from Avalonia UI follow
  Avalonia UI 12.

## Minimal example

```csharp
using System;
using DotNetBrowser.Browser;
using DotNetBrowser.Dom;
using DotNetBrowser.Engine;
using DotNetBrowser.Navigation;

EngineOptions.Builder builder = new EngineOptions.Builder();
builder.LicenseKey = "<LICENSE_KEY>";

using (IEngine engine = EngineFactory.Create(builder.Build()))
{
    IBrowser browser = engine.Profiles.Default.CreateBrowser();
    NavigationResult result = browser.Navigation
        .LoadUrl("https://quotes.toscrape.com/random").Result;
    if (result.LoadResult != LoadResult.Completed)
    {
        throw new InvalidOperationException($"Navigation did not complete: {result.LoadResult}");
    }

    IDocument document = browser.MainFrame.Document;
    string quote = document.GetElementByClassName("text")?.InnerText;
    string author = document.GetElementByClassName("author")?.InnerText;

    Console.WriteLine(quote);
    Console.WriteLine($"— {author}");
}
```

The window setup for each UI framework is in `references/browser-view.md`.
Complete window code for Windows Forms, WPF, WinUI 3, and Avalonia UI is in
`references/site/docs/guides/gs/browser-view/index.md`. The quick starts in
`references/site/docs/quickstart/<wpf|winforms|winui3|avalonia|avalonia12|console>/index.md`
only show how to create a project from the `dotnet new` templates.

## Licensing

Provide the key one of three ways: `EngineOptions.Builder.LicenseKey`; a
`dotnetbrowser.license` file (plain text with the key) added as an
**Embedded Resource**; or the same file copied to the application output
directory (`AppContext.BaseDirectory`). For the file-based option, set
**Copy to Output Directory** to **Copy if newer** or **Copy always** so the
build places the file there. The API key overrides the file. Missing keys raise
`NoLicenseException`; `InvalidLicenseException` carries the reason (expired,
wrong product version, and so on). A Project license is tied to a namespace:
create the engine in a class inside that namespace or its inner namespaces.
Top-level statements have no namespace, so move the engine creation into a
class in the licensed namespace.

A license key is a secret. Never write a customer's key into source code,
committed configuration, or a license file that is under version control.
Prefer the configuration or secret store the project already uses (for
example, .NET user secrets or the CI secret store), read the value at
runtime, and pass it to `LicenseKey`. If the project uses a license file,
make sure it is git-ignored.

## Frequently needed guides

All pages below are under `references/site/docs/guides/`.

| Topic | Page |
| --- | --- |
| Object model, handlers, threading | `design/index.md` |
| Processes and lifecycle | `architecture/index.md` |
| Engine options (user data dir, language, proxy, switches, remote debugging) | `gs/engine/index.md` |
| Browser, settings, user agent, input simulation, DevTools | `gs/browser/index.md` |
| Embedding `BrowserView` per framework, rendering modes, limitations | `gs/browser-view/index.md` |
| Navigation, POST, loading HTML and files, back/forward, filtering page navigations | `gs/navigation/index.md` |
| DOM access, XPath, query selectors, events, form automation | `gs/dom/index.md` |
| JavaScript execution, `IJsObject`, promises, calling .NET from JS | `gs/javascript/index.md` |
| Network handlers: blocking or redirecting any request, including images and scripts (`SendUrlRequestHandler`, `ResourceType`; see also "Filtering resources" in `gs/navigation/index.md`), request and response headers, network events, TLS, client certificates | `gs/network/index.md` |
| Printing and PDF | `gs/printing/index.md` |
| Pop-ups, dialogs, context menu, downloads, permissions | `gs/popups/`, `gs/dialogs/`, `gs/context-menu/`, `gs/downloads/`, `gs/permissions/` |
| Deployment, Chromium binaries, trimming and Native AOT | `gs/deployment/index.md`, `gs/chromium/index.md`, `gs/aot-support/index.md` |
| Logging, common exceptions, startup failures, crashes | `troubleshoot/logging/index.md`, `troubleshoot/common-exceptions/index.md`, `troubleshoot/startup-failure/index.md`, `troubleshoot/unexpected-termination/index.md` |
| Migrating from 3.x, from CefSharp or WebView2 | `../../migration/from-v3-to-v4/overview/index.md`, `../../blog/migrating-from-cefsharp-to-dotnetbrowser/index.md`, `../../blog/from-webview2-to-dotnetbrowser-part-1/index.md` |
