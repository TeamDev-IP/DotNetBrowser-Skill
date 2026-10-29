# DotNetBrowser 4.3.5

Version 4.3.5 · Posted on 2026-10-28

## Chromium 156.0.8078.74

We upgraded Chromium to a newer version, which introduces 52
security fixes. Among them:

* [CVE-2026-118306: Memory corruption in FileSystem][cve-2026-118306]
* [CVE-2026-118331: Improper input validation in FileAPI][cve-2026-118331]
* [CVE-2026-118348: Improper input validation in Skia][cve-2026-118348]
* [CVE-2026-118344: Use after free in Layout][cve-2026-118344]
* [CVE-2026-118357: Use after free in FileSystem][cve-2026-118357]

See the Chromium [release announcement][chromium-oct-27-2026] for more
details.

## Quality enhancements

* Fixed memory leaks in Avalonia views after browser disposal while the host
  window remained open. This affected off-screen rendering on Windows, Linux,
  and macOS, and hardware-accelerated rendering on macOS.
* On macOS, loading DotNetBrowser’s native libraries no longer makes Chromium's
  allocator the default malloc zone for the .NET application process. This
  prevents unrelated native allocations in the same process from going through
  Chromium's allocator.
* Removed trust for the emSign ECC Root CA - G3 root certificate. DotNetBrowser now
  rejects the affected eMudhra certificate hierarchy in line with Chrome's
  distrust decision.

[cve-2026-118306]: https://nvd.nist.gov/vuln/detail/CVE-2026-118306
[cve-2026-118331]: https://nvd.nist.gov/vuln/detail/CVE-2026-118331
[cve-2026-118348]: https://nvd.nist.gov/vuln/detail/CVE-2026-118348
[cve-2026-118344]: https://nvd.nist.gov/vuln/detail/CVE-2026-118344
[cve-2026-118357]: https://nvd.nist.gov/vuln/detail/CVE-2026-118357
[chromium-oct-27-2026]: https://chromereleases.googleblog.com/2026/10/stable-channel-update-for-desktop_0562499947.html
