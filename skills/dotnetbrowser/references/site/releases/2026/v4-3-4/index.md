# DotNetBrowser 4.3.4

Version 4.3.4 · Posted on 2026-10-22

## Chromium 156.0.8078.48

We upgraded Chromium to a newer version, which introduces 400 security fixes.
Among them:

* [CVE-2026-110152: Buffer overflow in ANGLE][cve-2026-110152]
* [CVE-2026-110149: Use after free in Browser][cve-2026-110149]
* [CVE-2026-110136: Use after free in PDF][cve-2026-110136]
* [CVE-2026-110161: Use after free in Network][cve-2026-110161]
* [CVE-2026-110162: Use after free in Desktop][cve-2026-110162]

See the Chromium release announcements for more details.

* [October 13][chromium-oct-13-2026]
* [October 15][chromium-oct-15-2026]
* [October 20][chromium-oct-20-2026]

## Quality enhancements

* Fixed an issue where PDF form fields and cross-site iframes did not accept
  text input in Avalonia off-screen views on Windows.
* Fixed CORS preflight failures caused by extensions using
  `declarativeNetRequest` header rules.
* Fixed an issue where popup windows, such as date pickers, could remain
  invisible on Windows in hardware-accelerated rendering mode.
* On-device Web Speech recognition is now reported as unavailable.
  `SpeechRecognition.install()` resolves to `false` without downloading models.
* Fixed an `InvalidCastException` when converting browser bitmaps to images
  in WPF and Avalonia applications.
* Text input now works after closing a Chromium dialog in Avalonia off-screen
  views on Windows.
* Avalonia off-screen views on Linux now report focus loss when switching
  to another application.

[cve-2026-110152]: https://nvd.nist.gov/vuln/detail/CVE-2026-110152
[cve-2026-110149]: https://nvd.nist.gov/vuln/detail/CVE-2026-110149
[cve-2026-110136]: https://nvd.nist.gov/vuln/detail/CVE-2026-110136
[cve-2026-110161]: https://nvd.nist.gov/vuln/detail/CVE-2026-110161
[cve-2026-110162]: https://nvd.nist.gov/vuln/detail/CVE-2026-110162
[chromium-oct-13-2026]: https://chromereleases.googleblog.com/2026/10/stable-channel-update-for-desktop_01668083673.html
[chromium-oct-15-2026]: https://chromereleases.googleblog.com/2026/10/stable-channel-update-for-desktop_01886704284.html
[chromium-oct-20-2026]: https://chromereleases.googleblog.com/2026/10/stable-channel-update-for-desktop_02018666648.html
