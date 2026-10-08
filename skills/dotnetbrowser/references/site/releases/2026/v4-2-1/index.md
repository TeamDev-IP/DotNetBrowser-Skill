# DotNetBrowser 4.2.1

Version 4.2.1 · Posted on 2026-07-21

## Chromium 150.0.7871.125

We upgraded Chromium to a newer version, which introduces 42 security
fixes. Among them:

* [CVE-2026-15764: Use after free in Ozone][cve-2026-15764]
* [CVE-2026-15765: Use after free in Ozone][cve-2026-15765]
* [CVE-2026-15766: Uninitialized Use in Skia][cve-2026-15766]
* [CVE-2026-15767: Heap buffer overflow in libyuv][cve-2026-15767]
* [CVE-2026-15768: Insufficient policy enforcement in HTML-in-Canvas][cve-2026-15768]

See the Chromium release announcements for more details.

* [July 14][chromium-july-14-2026]
* [July 8][chromium-july-8-2026]

## Quality enhancements

* Improved Tab key focus traversal behavior in the `WPF` framework.

[cve-2026-15764]: https://nvd.nist.gov/vuln/detail/CVE-2026-15764
[cve-2026-15765]: https://nvd.nist.gov/vuln/detail/CVE-2026-15765
[cve-2026-15766]: https://nvd.nist.gov/vuln/detail/CVE-2026-15766
[cve-2026-15767]: https://nvd.nist.gov/vuln/detail/CVE-2026-15767
[cve-2026-15768]: https://nvd.nist.gov/vuln/detail/CVE-2026-15768
[chromium-july-14-2026]: https://chromereleases.googleblog.com/2026/07/stable-channel-update-for-desktop_0353146366.html
[chromium-july-8-2026]: https://chromereleases.googleblog.com/2026/07/stable-channel-update-for-desktop_01162222768.html