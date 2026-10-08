# DotNetBrowser 4.2.3

Version 4.2.3 · Posted on 2026-08-17

## Chromium 151.0.7922.138

We upgraded Chromium to a newer version, which introduces 46
security fixes. Among them:

* [CVE-2026-19137: Use after free in WebGL][cve-2026-19137]
* [CVE-2026-19149: Use after free in Aura][cve-2026-19149]
* [CVE-2026-19154: Use after free in Skia][cve-2026-19154]
* [CVE-2026-19157: Out of bounds write in ANGLE][cve-2026-19157]
* [CVE-2026-19170: Use after free in WebGL][cve-2026-19170]

See the Chromium release announcements for more details.

* [August 11][chromium-aug-11-2026]
* [August 6][chromium-aug-6-2026]
* [August 4][chromium-aug-4-2026]

## Quality enhancements

* Improved IME behavior in Avalonia applications on Linux when using off-screen
  rendering.
* Input focus is now restored correctly after minimizing and restoring WinUI 3
  applications in hardware-accelerated rendering mode.
* On macOS, editing shortcuts such as Cmd+A, Cmd+C, and Cmd+V now apply to the
  focused frame, including iframe content.


[cve-2026-19137]: https://nvd.nist.gov/vuln/detail/CVE-2026-19137
[cve-2026-19149]: https://nvd.nist.gov/vuln/detail/CVE-2026-19149
[cve-2026-19154]: https://nvd.nist.gov/vuln/detail/CVE-2026-19154
[cve-2026-19157]: https://nvd.nist.gov/vuln/detail/CVE-2026-19157
[cve-2026-19170]: https://nvd.nist.gov/vuln/detail/CVE-2026-19170
[chromium-aug-11-2026]: https://chromereleases.googleblog.com/2026/08/stable-channel-update-for-desktop_01815628406.html
[chromium-aug-6-2026]: https://chromereleases.googleblog.com/2026/08/stable-channel-update-for-desktop_01193673229.html
[chromium-aug-4-2026]: https://chromereleases.googleblog.com/2026/08/stable-channel-update-for-desktop.html
