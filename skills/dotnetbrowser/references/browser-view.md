# Displaying a browser

Paths are relative to the skill folder, the one that holds `SKILL.md`.

Each UI package has a `BrowserView` control (`DotNetBrowser.Wpf.BrowserView`,
`DotNetBrowser.WinForms.BrowserView`, `DotNetBrowser.WinUi3.BrowserView`,
`DotNetBrowser.AvaloniaUi.BrowserView`). Bind it with
`browserView.InitializeFrom(browser)` on the UI thread. `InitializeFrom` is an
extension method in `DotNetBrowser.Browser.BrowserViewExtensions`, so it is
not listed on the `BrowserView` pages and needs `using DotNetBrowser.Browser;`.
One view per browser:
a second `InitializeFrom` with the same browser detaches the first view. A
view stays bound to its browser until that browser is disposed or moved to
another view; calling `InitializeFrom` on a bound view with a different
browser throws `InvalidOperationException` ("This view is already initialized
by another Browser"). Prefer one browser per view and navigate it. To switch
browsers, dispose the old one first, on the UI thread (disposing detaches the
view), then call `InitializeFrom` with the new one. Views never dispose the
browser or the engine, so dispose both on application shutdown
(`browser.Dispose(); engine.Dispose();`), or the Chromium processes keep the
application alive.

A WPF window adds `<WPF:BrowserView Name="browserView" />`
with `xmlns:WPF="clr-namespace:DotNetBrowser.Wpf;assembly=DotNetBrowser.Wpf"`,
then calls `browserView.InitializeFrom(browser)` after `InitializeComponent()`
and disposes the browser and engine in the window's `Closed` handler. Window
code for Windows Forms, WPF, WinUI 3 (including `SetWindow`), and Avalonia UI
(including the Avalonia 12 assembly and XAML namespace) is in
`references/site/docs/guides/gs/browser-view/index.md`. The quick starts in
`references/site/docs/quickstart/<wpf|winforms|winui3|avalonia|avalonia12|console>/index.md`
only show how to create a project from the `dotnet new` templates.

## WinUI 3 shutdown

When a WinUI 3 window creates the engine with `CreateAsync`, follow the
`DispatcherShutdownMode.OnExplicitShutdown` steps in the "WinUI 3" section of
`references/site/docs/guides/gs/browser-view/index.md`. Closing the last
window stops its message loop, so code after `await` may never run, and
`engine?.Dispose()` on a still-null field does not clean up the pending engine.
