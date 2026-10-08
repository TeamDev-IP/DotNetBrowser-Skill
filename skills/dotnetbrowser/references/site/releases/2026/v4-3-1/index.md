# DotNetBrowser 4.3.1

Version 4.3.1 · Posted on 2026-09-15

## Windows geolocation

On Windows 10 version 1809, Windows Server 2019, and later, Chromium now
respects the system-level location permission. If location access is
turned off in Windows Settings › Privacy › Location, web pages cannot obtain
the location even when the application grants geolocation permission.

If your application uses geolocation on these Windows versions, make sure that
location access is enabled in Windows settings and handle cases where the
operating system blocks access.

## Chromium 153.0.8010.37

We upgraded Chromium to a newer version, which introduces 268 security
fixes. Among them:

* [CVE-2026-87464: Use after free in WebGL][cve-2026-87464]
* [CVE-2026-87488: Use after free in WebGL][cve-2026-87488]
* [CVE-2026-87438: Out of bounds write in WebGL][cve-2026-87438]
* [CVE-2026-85046: Type confusion in V8][cve-2026-85046]
* [CVE-2026-87491: Out of bounds write in V8][cve-2026-87491]

Google is aware that exploits for CVE-2026-85046 and CVE-2026-87491 exist in
the wild.

See the Chromium release announcements for more details.

* [September 1][chromium-sep-1-2026]
* [September 3][chromium-sep-3-2026]
* [September 8][chromium-sep-8-2026]

## Quality enhancements

* Chromium password leak detection is now disabled, preventing requests to
  `passwordsleakcheck-pa.googleapis.com`.
* Off-screen rendering on Apple silicon now uses Skia Graphite, restoring
  WebGL, WebGPU, and hardware acceleration.
* Closing a browser with a pending media permission request no longer
  crashes the engine.
* Mapping an off-screen surface while the GPU swaps a frame no
  longer causes a race-related crash on Windows.
* Improved the Chromium binary extraction algorithm for better performance and reduced memory usage.
* Improved native input handling for complex IMEs on macOS.

[cve-2026-87464]: https://nvd.nist.gov/vuln/detail/CVE-2026-87464
[cve-2026-87488]: https://nvd.nist.gov/vuln/detail/CVE-2026-87488
[cve-2026-87438]: https://nvd.nist.gov/vuln/detail/CVE-2026-87438
[cve-2026-85046]: https://nvd.nist.gov/vuln/detail/CVE-2026-85046
[cve-2026-87491]: https://nvd.nist.gov/vuln/detail/CVE-2026-87491
[chromium-sep-1-2026]: https://chromereleases.googleblog.com/2026/09/stable-channel-update-for-desktop.html
[chromium-sep-3-2026]: https://chromereleases.googleblog.com/2026/09/stable-channel-update-for-desktop_01882797386.html
[chromium-sep-8-2026]: https://chromereleases.googleblog.com/2026/09/stable-channel-update-for-desktop_0808145027.html
