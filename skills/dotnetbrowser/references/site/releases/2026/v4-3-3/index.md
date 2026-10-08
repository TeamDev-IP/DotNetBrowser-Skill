# DotNetBrowser 4.3.3

Version 4.3.3 · Posted on 2026-10-08

## Chromium 155.0.8059.40

We upgraded Chromium to a newer version, which introduces 290 security fixes.

* [CVE-2026-102331: Buffer overflow in ANGLE][cve-2026-102331]
* [CVE-2026-103628: Out of bounds write in WebGL][cve-2026-103628]
* [CVE-2026-106382: Use after free in Chromecast][cve-2026-106382]
* [CVE-2026-106197: Use after free in Browser][cve-2026-106197]
* [CVE-2026-102317: Improper privilege management in Mojo][cve-2026-102317]

See the Chromium release announcements for more details.

* [September 29][chromium-sep-29-2026]
* [October 1][chromium-oct-1-2026]
* [October 6][chromium-oct-6-2026]

## Quality enhancements

* Screen sharing now captures browser audio on macOS and Linux.
* Fixed a crash that could occur during engine shutdown while a screen or window
  capture device was starting.
* Fixed an issue where switching back to a WPF application with Alt+Tab moved
  focus to the first tabbable element.
* Fixed an issue where middle-clicking a link could open Chromium split view.

[cve-2026-102331]: https://nvd.nist.gov/vuln/detail/CVE-2026-102331
[cve-2026-103628]: https://nvd.nist.gov/vuln/detail/CVE-2026-103628
[cve-2026-106382]: https://nvd.nist.gov/vuln/detail/CVE-2026-106382
[cve-2026-106197]: https://nvd.nist.gov/vuln/detail/CVE-2026-106197
[cve-2026-102317]: https://nvd.nist.gov/vuln/detail/CVE-2026-102317
[chromium-sep-29-2026]: https://chromereleases.googleblog.com/2026/09/stable-channel-update-for-desktop_01807488085.html
[chromium-oct-1-2026]: https://chromereleases.googleblog.com/2026/10/stable-channel-update-for-desktop.html
[chromium-oct-6-2026]: https://chromereleases.googleblog.com/2026/10/stable-channel-update-for-desktop_086471744.html
