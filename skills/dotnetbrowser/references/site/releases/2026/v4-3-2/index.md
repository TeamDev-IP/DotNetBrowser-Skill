# DotNetBrowser 4.3.2

Version 4.3.2 · Posted on 2026-09-28

## Breaking changes

### Windows registry extensions

On Windows, DotNetBrowser no longer installs extensions registered in the
Windows registry. This prevents an embedded browser from loading extension
code that the application did not request.

Applications that need an extension should install it through their own
application-controlled extension setup instead of relying on Chrome extension
registry entries.

## Chromium 154.0.8037.58

We upgraded Chromium to a newer version, which introduces 166 security fixes.

* [CVE-2026-91726: Out of bounds read in WebGL][cve-2026-91726]
* [CVE-2026-91721: Use after free in Internals][cve-2026-91721]
* [CVE-2026-91749: Use after free in Workers][cve-2026-91749]
* [CVE-2026-93374: Use after free in Dawn][cve-2026-93374]
* [CVE-2026-91724: Use after free in Input][cve-2026-91724]

See the Chromium release announcements for more details.

* [September 15][chromium-sep-15-2026]
* [September 17][chromium-sep-17-2026]
* [September 22][chromium-sep-22-2026]

## Quality enhancements

* Fixed memory growth in the .NET process when an application made repeated DOM or other calls from a long-running event handler.
* Fixed a memory leak that kept disposed page contexts, DOM contexts, and JS contexts in memory after navigation.
* Fixed a Chromium process crash that could occur after a web page started a
  Presentation API request and the application answered
  `StartPresentationHandler`.
* Compressed response bodies written by `UrlRequestJob` in
  `InterceptRequestResponse` are now decoded according to the
  `Content-Encoding` header. This lets intercepted HTML, scripts, and styles
  load as decoded content instead of raw compressed bytes.
* Fixed `Browser.DevTools.Show()` on macOS so the DevTools window is visible
  again.
* Disabled network requests from Chromium's on-device AI component to Google's
  update service.
* Improved native input handling for complex IMEs on Windows and Linux.

[cve-2026-91726]: https://nvd.nist.gov/vuln/detail/CVE-2026-91726
[cve-2026-91721]: https://nvd.nist.gov/vuln/detail/CVE-2026-91721
[cve-2026-91749]: https://nvd.nist.gov/vuln/detail/CVE-2026-91749
[cve-2026-93374]: https://nvd.nist.gov/vuln/detail/CVE-2026-93374
[cve-2026-91724]: https://nvd.nist.gov/vuln/detail/CVE-2026-91724
[chromium-sep-15-2026]: https://chromereleases.googleblog.com/2026/09/stable-channel-update-for-desktop_0541751186.html
[chromium-sep-17-2026]: https://chromereleases.googleblog.com/2026/09/stable-channel-update-for-desktop_0194356994.html
[chromium-sep-22-2026]: https://chromereleases.googleblog.com/2026/09/stable-channel-update-for-desktop_0856730748.html
