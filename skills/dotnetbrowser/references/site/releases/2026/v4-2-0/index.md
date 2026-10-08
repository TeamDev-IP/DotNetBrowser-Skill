# DotNetBrowser 4.2.0

Version 4.2.0 · Posted on 2026-07-07

## Touch ID on macOS

DotNetBrowser now supports the built-in macOS Touch ID platform authenticator
using the WebAuthn API. Users on Mac can authenticate to sites that support
passkeys using Touch ID directly through the browser.

As part of enabling this feature, the Chromium bundle ID changed from
`org.chromium.Chromium` to `com.teamdev.Platinum`. Because macOS identifies
applications by their bundle ID, it now treats this as a different application
than previous builds. Developers and users may see macOS permission prompts on
the first launch after an update — camera, microphone, screen recording,
notifications, and accessibility access may each be re-requested. This is
expected one-time behavior; granting the permissions restores normal operation.

Learn more in the [migration guide][guide-migration].

## Chromium 150.0.7871.47

We upgraded Chromium to a newer version, which introduces 433 security
fixes. Among them:

* [CVE-2026-13774: Use after free in Extensions][cve-2026-13774]
* [CVE-2026-13775: Use after free in GPU][cve-2026-13775]
* [CVE-2026-14398: Use after free in ANGLE][cve-2026-14398]
* [CVE-2026-13776: Type Confusion in Dawn][cve-2026-13776]
* [CVE-2026-13777: Insufficient validation of untrusted input in iOSWeb][cve-2026-13777]

See the Chromium [release announcement][chromium-jun-30-2026] for more
details.

## Quality enhancements

* Capture lists for `Screens` and `ApplicationWindows` sources are no longer empty
  on macOS when using StartSessionHandler.
* The sharing source picker dialog now appears in offscreen mode on macOS.

[guide-migration]: https://teamdev.com/dotnetbrowser/migration/within-v4/v4-1-1-v4-2-0/
[chromium-jun-30-2026]: https://chromereleases.googleblog.com/2026/06/stable-channel-update-for-desktop_0175352312.html
[cve-2026-13774]: https://nvd.nist.gov/vuln/detail/CVE-2026-13774
[cve-2026-13775]: https://nvd.nist.gov/vuln/detail/CVE-2026-13775
[cve-2026-14398]: https://nvd.nist.gov/vuln/detail/CVE-2026-14398
[cve-2026-13776]: https://nvd.nist.gov/vuln/detail/CVE-2026-13776
[cve-2026-13777]: https://nvd.nist.gov/vuln/detail/CVE-2026-13777
