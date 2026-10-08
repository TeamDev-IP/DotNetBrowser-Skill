# DotNetBrowser 4.3.0

Version 4.3.0 · Posted on 2026-08-28

## Default fonts configuration

DotNetBrowser now lets you retrieve the fonts available on the system and
use them as the browser's default standard, serif, sans-serif, fixed-width,
or mathematical font.

```csharp
IReadOnlyList<Font> fonts = browser.Settings.DefaultFonts.Available;

Font font = fonts.First();

browser.Settings.DefaultFonts.Standard = font;
browser.Settings.DefaultFonts.Serif = font;
browser.Settings.DefaultFonts.SansSerif = font;
browser.Settings.DefaultFonts.FixedWidth = font;
browser.Settings.DefaultFonts.Mathematical = font;

string displayName = font.DisplayName;
```

## Chromium 152.0.7977.65

We upgraded Chromium to a newer version, which introduces 349 security
fixes. Among them:

* [CVE-2026-76034: Buffer overflow in WebGL][cve-2026-76034]
* [CVE-2026-76036: Buffer overflow in Dawn][cve-2026-76036]
* [CVE-2026-76017: Use after free in Chromoting][cve-2026-76017]
* [CVE-2026-79282: Use after free in ANGLE][cve-2026-79282]
* [CVE-2026-76033: Inappropriate implementation in CORS][cve-2026-76033]

See the Chromium release announcements for more details.

* [August 18][chromium-aug-18-2026]
* [August 20][chromium-aug-20-2026]
* [August 25][chromium-aug-25-2026]

## Quality enhancements

* Fixed a video playback failure on pages that deliver video through a
  custom scheme handled by `InterceptRequestHandler`.
* Fixed `BrowserView` flickering when resizing WinUI 3 windows in
  hardware-accelerated rendering mode.
* Fixed blurry rendering in Avalonia UI applications on scaled monitors by
  adding a per-monitor DPI awareness declaration to the application
  manifest template.


[cve-2026-76034]: https://nvd.nist.gov/vuln/detail/CVE-2026-76034
[cve-2026-76036]: https://nvd.nist.gov/vuln/detail/CVE-2026-76036
[cve-2026-76017]: https://nvd.nist.gov/vuln/detail/CVE-2026-76017
[cve-2026-79282]: https://nvd.nist.gov/vuln/detail/CVE-2026-79282
[cve-2026-76033]: https://nvd.nist.gov/vuln/detail/CVE-2026-76033
[chromium-aug-18-2026]: https://chromereleases.googleblog.com/2026/08/stable-channel-update-for-desktop_0826575033.html
[chromium-aug-20-2026]: https://chromereleases.googleblog.com/2026/08/stable-channel-update-for-desktop_0404570826.html
[chromium-aug-25-2026]: https://chromereleases.googleblog.com/2026/08/stable-channel-update-for-desktop_0256176589.html
