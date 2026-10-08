# DotNetBrowser 4.1.0

Version 4.1.0 · Posted on 2026-05-28

## Breaking changes

### `IHttpCache.DiskCacheCleared` event removed

`IHttpCache.DiskCacheCleared` has been removed.

`IHttpCache.Clear()` returns a `Task` that completes once the cache clearing operation finishes.
Use the returned task to track completion instead of subscribing to the removed event.

## Avalonia 12 support

Added support for Avalonia 12 via the new `DotNetBrowser.AvaloniaUi.v12` NuGet package.

This package provides integration components compatible with Avalonia 12 applications while preserving support for existing Avalonia 11 integrations through the separate `DotNetBrowser.AvaloniaUi` package.

You can read more about it in the [migration guide](https://teamdev.com/dotnetbrowser/migration/within-v4/v4-0-1-v4-1-0/).

## Simplified data clearing via IProfile.ClearAllData()

You can now completely clear browsing data at the profile level with a single API call using the new `IProfile.ClearAllData()` method.
The method removes cache, cookies, browsing history, and other stored profile data.

## Per-browser zoom

By default, zoom level changes apply to all browsers that share
the same origin within a profile. Starting with DotNetBrowser 4.1.0,
you can scope zoom to an individual browser so that changing the
zoom level in one browser does not affect others:

```csharp
Browser.Zoom.Mode = ZoomMode.PerBrowser;
Browser.Zoom.In();
```

The default mode is `ZoomMode.PerOrigin`, which preserves the
previous behavior.

Learn more in the [zoom guide][guides-zoom].

## Chromium 148.0.7778.179

We upgraded Chromium to a newer version, which introduces major
security fixes, including:

* [CVE-2026-9111: Use after free in WebRTC][cve-2026-9111]
* [CVE-2026-9110: Inappropriate implementation in UI][cve-2026-9110]
* [CVE-2026-9112: Use after free in GPU][cve-2026-9112]
* [CVE-2026-9113: Out of bounds read in GPU][cve-2026-9113]
* [CVE-2026-9114: Use after free in QUIC][cve-2026-9114]

See the Chromium [release announcement][chromium-may-19-2026] for more details.

## Quality enhancements

* Fixed handling of system keys in `OffScreen` mode for `WinForms` and `Avalonia`.

[guides-zoom]: https://teamdev.com/dotnetbrowser/docs/guides/gs/zoom/
[chromium-may-19-2026]: https://chromereleases.googleblog.com/2026/05/stable-channel-update-for-desktop_0841193308.html
[cve-2026-9111]: https://nvd.nist.gov/vuln/detail/CVE-2026-9111
[cve-2026-9110]: https://nvd.nist.gov/vuln/detail/CVE-2026-9110
[cve-2026-9112]: https://nvd.nist.gov/vuln/detail/CVE-2026-9112
[cve-2026-9113]: https://nvd.nist.gov/vuln/detail/CVE-2026-9113
[cve-2026-9114]: https://nvd.nist.gov/vuln/detail/CVE-2026-9114
