# DotNetBrowser 4.0.0

Version 4.0.0 · Posted on 2026-04-28

**Lead**
We are excited to announce the release of DotNetBrowser 4.0.0!


This new major version introduces a number of new features and improvements, including support for trimming and AOT.

We did not change the API significantly, so you can easily migrate your existing code to the new version. However, we recommend that you review the [migration guide](https://teamdev.com/dotnetbrowser/migration/from-v3-to-v4/overview/) to learn about the changes and improvements in DotNetBrowser 4.0.0.

More information about the new features and improvements in DotNetBrowser 4.0.0 can be found below.

## Trimming and Native AOT Support (.NET 8+)

Added trimming and Native AOT compatibility for key packages targeting .NET 8+.
This feature works with console and Avalonia UI applications.

You can find more information in [this article](https://teamdev.com/dotnetbrowser/docs/guides/gs/aot-support).

## Rendering mode per browser

Previously, the rendering mode was fixed for the entire `IEngine`. All
browsers created from that engine shared the same mode, which made it
impossible to share a profile between an off-screen and a
hardware-accelerated browser.

In DotNetBrowser 4.0.0, you can specify the rendering mode for each
`IBrowser` instance individually:

```csharp
IBrowser browser = engine.Profiles.Default.CreateBrowser(RenderingMode.OffScreen);
```

Browsers created with `IEngine.CreateBrowser()` or `IProfile.CreateBrowser()`
without arguments still use the engine's default rendering mode. Popup
browsers inherit the rendering mode of their parent browser.

Learn more in the [Rendering](https://teamdev.com/dotnetbrowser/docs/guides/gs/browser-view/#rendering) guide.

## New JavaScript types

In this version, we add two new data types that are automatically converted between .NET and JavaScript:

* `BigInt` ↔ `System.Numerics.BigInteger`
* `Symbol` ↔ `DotNetBrowser.Js.IJsSymbol`

For example:

```csharp
BigInteger number = IFrame.ExecuteJavaScript<BigInteger>("9007199254740991n").Result;
IJsSymbol symbol = IFrame.ExecuteJavaScript<IJsSymbol>("Symbol('bacf2f')").Result;
```

Check out the [JavaScript guide](https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/#type-conversion) for more details.

## Delegated screen capturing

DotNetBrowser now supports delegated screen capturing. That is the mode where the OS
presents a system dialog for the user to choose the capture source, instead
of exposing all windows and screens directly to the application.

Delegated capturing is the default mode on Linux/Wayland.

## Chromium 147.0.7727.117

We upgraded Chromium to a newer version, which introduces 50 security
fixes. Among them:

* [CVE-2026-6296: Heap buffer overflow in ANGLE][cve-2026-6296]
* [CVE-2026-6297: Use after free in Proxy][cve-2026-6297]
* [CVE-2026-6298: Heap buffer overflow in Skia][cve-2026-6298]
* [CVE-2026-6299: Use after free in Prerender][cve-2026-6299]
* [CVE-2026-6358: Use after free in XR][cve-2026-6358]

You can read more about it in the Chromium blog posts:

* [April 15, 2026][chromium-apr-15-2026]
* [April 22, 2026][chromium-apr-22-2026]

## Quality enhancements

* Fixed an issue where the `IsVisible` property of `BrowserView` could not be bound via AXAML in Avalonia UI.
* Fixed an issue where default keyboard shortcuts did not work on macOS.
* Fixed an issue with drop-downs by using the `--enable-custom-dropdowns` switch in environments where the parent window is not available.
* Added full support for Wayland systems via XWayland in DotNetBrowser.

## How to upgrade

If you have a valid DotNetBrowser license with active support and updates subscription, you can upgrade to DotNetBrowser 4.0.0 for free.

You can upgrade DotNetBrowser in your project by changing the version of the DotNetBrowser dependency in your project configuration.

If you have any questions or need assistance with the upgrade, please feel free to contact us.

[cve-2026-6296]: https://nvd.nist.gov/vuln/detail/CVE-2026-6296
[cve-2026-6297]: https://nvd.nist.gov/vuln/detail/CVE-2026-6297
[cve-2026-6298]: https://nvd.nist.gov/vuln/detail/CVE-2026-6298
[cve-2026-6299]: https://nvd.nist.gov/vuln/detail/CVE-2026-6299
[cve-2026-6358]: https://nvd.nist.gov/vuln/detail/CVE-2026-6358
[chromium-apr-15-2026]: https://chromereleases.googleblog.com/2026/04/stable-channel-update-for-desktop_15.html
[chromium-apr-22-2026]: https://chromereleases.googleblog.com/2026/04/stable-channel-update-for-desktop_22.html