# DotNetBrowser 4.0.1

Version 4.0.1 · Posted on 2026-05-04

## Chromium 147.0.7727.138

We upgraded Chromium to a newer version, which introduces 30 security
fixes. Among them:

* [CVE-2026-7363: Use after free in Canvas][cve-2026-7363]
* [CVE-2026-7361: Use after free in iOS][cve-2026-7361]
* [CVE-2026-7344: Use after free in Accessibility][cve-2026-7344]
* [CVE-2026-7343: Use after free in Views][cve-2026-7343]
* [CVE-2026-7333: Use after free in GPU][cve-2026-7333]

You can read more about it in the Chromium
[blog post][chromium-apr-28-2026].

## Quality enhancements

* Fixed a crash that occurred on macOS 26.4.1 when creating an `IEngine`.
* Fixed a crash that occurred on macOS when triggering the screen
  capture dialog.
* In WinUI 3, the combobox drop-down now hides properly.

[cve-2026-7363]: https://nvd.nist.gov/vuln/detail/CVE-2026-7363
[cve-2026-7361]: https://nvd.nist.gov/vuln/detail/CVE-2026-7361
[cve-2026-7344]: https://nvd.nist.gov/vuln/detail/CVE-2026-7344
[cve-2026-7343]: https://nvd.nist.gov/vuln/detail/CVE-2026-7343
[cve-2026-7333]: https://nvd.nist.gov/vuln/detail/CVE-2026-7333
[chromium-apr-28-2026]: https://chromereleases.googleblog.com/2026/04/stable-channel-update-for-desktop_28.html
