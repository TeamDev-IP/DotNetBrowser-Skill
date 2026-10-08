# Project setup

Paths are relative to the skill folder, the one that holds `SKILL.md`.

## Packages and templates

Single-platform UI variants exist too, for example `DotNetBrowser.Wpf.x64`.
See `references/site/docs/guides/installation/nuget/index.md` for the full
list. For a new project using this skill's version, install the matching
templates:
`dotnet new install DotNetBrowser.Templates::4.3.3`, then
`dotnet new dotnetbrowser.wpf.app` (also `winforms`, `winui`, `avalonia`,
`avalonia12`, `blazor.avalonia`, `console`).

## Avalonia on Windows

For Avalonia apps on Windows, keep or add the `app.manifest` with
`PerMonitorV2` DPI awareness, as the "Avalonia UI" section of
`references/site/docs/guides/gs/browser-view/index.md` describes. Avalonia's
own templates do not declare DPI awareness.

## Runtimes and platforms

Core library runtimes: .NET Framework 4.6.2-4.8.1 (Windows only) and .NET 5-10;
UI integrations can require a newer runtime, as with Avalonia UI 12 (.NET 8 or
later). Windows x86/x64/ARM64, Linux x64/ARM64, macOS x64/ARM64. Headless Linux
and Docker need an X server
(`references/site/docs/guides/headless-linux/index.md`); macOS cannot run
headless.
