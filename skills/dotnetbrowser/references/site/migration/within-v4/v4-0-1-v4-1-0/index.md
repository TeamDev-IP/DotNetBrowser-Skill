
# Migrating from 4.0.1 to 4.1.0

DotNetBrowser 4.1.0 introduces a breaking API change in `IHttpCache` and adds Avalonia 12 support.
If you use `IHttpCache.DiskCacheCleared` event, follow the steps below. Otherwise no code changes are required.

## Removed API

### `IHttpCache.DiskCacheCleared` event

The `IHttpCache.DiskCacheCleared` event has been removed.
The `IHttpCache.Clear()` method returns a `Task` that completes when the cache has been cleared.
Use the returned task to react to the completion instead of subscribing to the removed event.

## Avalonia 12 support

In 4.1.0, Avalonia 12 integration is available in addition to Avalonia 11.

If you migrate your UI application from Avalonia 11 to Avalonia 12, switch to the corresponding DotNetBrowser integration artifact:

- NuGet package: use `DotNetBrowser.AvaloniaUi.v12` instead of `DotNetBrowser.AvaloniaUi`.
- ZIP distribution: reference `DotNetBrowser.AvaloniaUi.v12.dll` instead of `DotNetBrowser.AvaloniaUi.dll`.
- Project templates: use the `dotnetbrowser.avalonia12.app` template.

## Deployment notes

For Avalonia applications, include the framework-specific integration artifact that matches your UI version:

- Avalonia 11: `DotNetBrowser.AvaloniaUi.dll` / `DotNetBrowser.AvaloniaUi`
- Avalonia 12: `DotNetBrowser.AvaloniaUi.v12.dll` / `DotNetBrowser.AvaloniaUi.v12`

All other platform binaries remain selected the same way as in 4.0.1.