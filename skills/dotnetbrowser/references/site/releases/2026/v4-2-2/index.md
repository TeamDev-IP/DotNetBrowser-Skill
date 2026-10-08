# DotNetBrowser 4.2.2

Version 4.2.2 · Posted on 2026-08-03

## Opening links in external apps

`OpenExternalAppParameters` now exposes `Url` property — the URL
that is about to be handed to the external application. Previously
the callback only provided the localized dialog texts, so there
was no way to tell which link triggered it or to apply your own
allow/deny rules before calling `OpenExternalAppResponse.Open()`.

```csharp
browser.Dialogs.OpenExternalAppHandler =
    new Handler<OpenExternalAppParameters, OpenExternalAppResponse>(p =>
    {
        if (IsTrusted(p.Url))
        {
            return OpenExternalAppResponse.Open();
        }

        return OpenExternalAppResponse.Cancel();
    });
```

We also removed Chromium's built-in limitation on how often
external applications may be launched. Chromium blocks every
external-protocol request after the first one until the user
performs a new gesture, which meant script-initiated requests
were silently dropped and your callback was never invoked for
them. DotNetBrowser now routes every request to
`OpenExternalAppHandler`, so a web page can open an external
application as many times as needed, and the decision to allow
or block it is entirely yours.

As part of the same change, `mailto:` links are no longer
special-cased. Chromium used to launch the default mail client
directly, bypassing the callback; `mailto:` now reaches
`OpenExternalAppHandler` like any other external scheme.

## macOS 12 is no longer supported

Starting with this release, macOS 13 (Ventura) is the minimum
supported macOS version. This change follows the Chromium 151
upgrade, which dropped support for macOS 12 (Monterey).

## Chromium 151.0.7922.72

We upgraded Chromium to a newer version, which introduces 393
security fixes. Among them:

* [CVE-2026-15899: Use after free in CameraCapture][cve-2026-15899]
* [CVE-2026-15900: Use after free in GPU][cve-2026-15900]
* [CVE-2026-15901: Use after free in Network][cve-2026-15901]
* [CVE-2026-17650: Use after free in Compositing][cve-2026-17650]
* [CVE-2026-17651: Insufficient validation of untrusted input in Dawn][cve-2026-17651]

See the Chromium release announcements for more details.

* [July 16][chromium-july-16-2026]
* [July 21][chromium-july-21-2026]
* [July 23][chromium-july-23-2026]
* [July 29][chromium-july-29-2026]

## Quality enhancements

* Keyboard shortcuts now work correctly in DevTools on macOS.
* Closing DevTools no longer causes the Chromium window to
  detach and become visible on macOS.

[cve-2026-15899]: https://nvd.nist.gov/vuln/detail/CVE-2026-15899
[cve-2026-15900]: https://nvd.nist.gov/vuln/detail/CVE-2026-15900
[cve-2026-15901]: https://nvd.nist.gov/vuln/detail/CVE-2026-15901
[cve-2026-17650]: https://nvd.nist.gov/vuln/detail/CVE-2026-17650
[cve-2026-17651]: https://nvd.nist.gov/vuln/detail/CVE-2026-17651
[chromium-july-16-2026]: https://chromereleases.googleblog.com/2026/07/stable-channel-update-for-desktop_049796704.html
[chromium-july-21-2026]: https://chromereleases.googleblog.com/2026/07/stable-channel-update-for-desktop_0256605430.html
[chromium-july-23-2026]: https://chromereleases.googleblog.com/2026/07/stable-channel-update-for-desktop_01320465736.html
[chromium-july-29-2026]: https://chromereleases.googleblog.com/2026/07/stable-channel-update-for-desktop_0887107924.html
