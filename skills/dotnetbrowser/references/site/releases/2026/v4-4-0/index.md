# DotNetBrowser 4.4.0

Version 4.4.0 · Posted on 2026-11-06

## Google.Protobuf update

We updated the [Google.Protobuf][docs-google-protobuf] dependency from 3.32.0
to 3.36.2. DotNetBrowser NuGet packages now depend on version 3.36.2 or later.

If your project directly references an earlier version of Google.Protobuf,
update the reference to 3.36.2 or a compatible later version when upgrading
DotNetBrowser. NuGet resolves package versions across the project, so check
that other packages using Google.Protobuf are compatible with the selected
version.

## Chromium 157.0.8103.39

We upgraded Chromium to a newer version, which introduces 234 security fixes.
Among them:

* [CVE-2026-76024: Use after free in MediaStream][cve-2026-76024]
* [CVE-2026-121156: Buffer overflow in Dawn][cve-2026-121156]
* [CVE-2026-121229: Memory corruption in ANGLE][cve-2026-121229]
* [CVE-2026-121246: Use after free in WebGL][cve-2026-121246]
* [CVE-2026-76025: Incorrect authorization in FileSystem][cve-2026-76025]

See the Chromium release announcements for more details.

* [October 29][chromium-oct-29-2026]
* [November 3][chromium-nov-3-2026]

## Quality enhancements

* On Windows, the engine now reports why it failed to start when Chromium
  de-elevates itself in an application running with administrator rights.
* Fixed keyboard input in Chromium dialogs in off-screen rendering mode on
  Windows and Linux. On Windows, focus also returns to the page after a dialog
  closes.

[docs-google-protobuf]: https://www.nuget.org/packages/Google.Protobuf/3.36.2
[cve-2026-76024]: https://nvd.nist.gov/vuln/detail/CVE-2026-76024
[cve-2026-121156]: https://nvd.nist.gov/vuln/detail/CVE-2026-121156
[cve-2026-121229]: https://nvd.nist.gov/vuln/detail/CVE-2026-121229
[cve-2026-121246]: https://nvd.nist.gov/vuln/detail/CVE-2026-121246
[cve-2026-76025]: https://nvd.nist.gov/vuln/detail/CVE-2026-76025
[chromium-oct-29-2026]: https://chromereleases.googleblog.com/2026/10/stable-channel-update-for-desktop_02107719452.html
[chromium-nov-3-2026]: https://chromereleases.googleblog.com/2026/11/stable-channel-update-for-desktop.html
