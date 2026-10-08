# DotNetBrowser 4.1.1

Version 4.1.1 · Posted on 2026-06-17

## Improved UrlRequestJob API

Added asynchronous and stream-friendly response writing for intercepted requests.

In this release, we extended `UrlRequestJob` with asynchronous write methods
and added stream extension methods to simplify handling large responses.

New APIs:

* `UrlRequestJob.WriteAsync(byte[] data)`
* `UrlRequestJob.WriteAsync(byte[] data, int offset, int count)`
* `UrlRequestJobExtensions.Write(UrlRequestJob job, Stream stream, int bufferSize = 81920)`
* `UrlRequestJobExtensions.WriteAsync(UrlRequestJob job, Stream stream, CancellationToken cancellationToken = default, int bufferSize = 81920)`

These APIs provide non-blocking response writes in asynchronous interception
flows, convenient streaming from `Stream` without loading the entire payload
into memory, and chunked writing with a configurable buffer size.

After writing all chunks, call `Complete()` to finish the response.
Call `Fail()` if writing cannot be completed.

## Touch handles

DotNetBrowser now allows disabling Chromium touch selection handles in touch
environments. This is useful when an application needs to manage text
selection UI itself and should not show Chromium's built-in touch handles.

The feature is controlled by the `--disable-touch-selection-handles` Chromium
command line switch.

See the [Chromium switches](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#chromium-switches) section
to learn how to configure command line switches.

## Password store API changes

In this release, we updated the password store API to make record removal
more explicit and to improve consistency for URL-based password matching.

### `IPasswordStore`: `Remove(PasswordRecord)` added

A new `Remove(PasswordRecord record)` method is now part of
`IPasswordStore`. It removes exactly one record by value and replaces
`RemoveByUrl` as the primary removal API.

```csharp
PasswordRecord record = profile.PasswordStore.AllSaved
    .First(r => r.Url.StartsWith("https://example.com"));

profile.PasswordStore.Remove(record);
```

### Breaking change: `RemoveByUrl` moved to an extension method

`IPasswordStore.RemoveByUrl(string url)` has been removed from the
interface and moved to `PasswordStoreExtensions`. The call syntax is
unchanged, so existing code that calls `store.RemoveByUrl(url)` continues
to compile as long as the `DotNetBrowser.Passwords` namespace is imported.

### Breaking change: `PasswordRecord.Url` for saved records

The value of `PasswordRecord.Url` has changed for saved (regular) records.
It now contains the full form URL (for example,
`https://example.com/login`) instead of only the origin URL.
For blacklisted (`NeverSave`) records, the value is unchanged and still
contains the origin URL.

Code that compares or filters saved records by exact origin URL may no
longer match as expected. Update such checks to use full URLs or
prefix-based matching.

```csharp
// Before: can miss saved records if full form URLs are stored
var records = store.All.Where(r => r.Url == "https://example.com/");

// After: origin-based matching for saved and blacklisted records
var records = store.All.Where(r => r.Url.StartsWith("https://example.com/"));
```

## Chromium 149.0.7827.103

We upgraded Chromium to a newer version, which introduces 74 security
fixes, including:

* [CVE-2026-11628: Use after free in Ozone][cve-2026-11628]
* [CVE-2026-11629: Use after free in Ozone][cve-2026-11629]
* [CVE-2026-11630: Use after free in File Input][cve-2026-11630]
* [CVE-2026-11631: Use after free in Aura][cve-2026-11631]
* [CVE-2026-11645: Out of bounds memory access in V8][cve-2026-11645]

Google is aware that an exploit for `CVE-2026-11645` exists in the wild.

See the Chromium [release announcement][chromium-jun-08-2026] for more
details.

## Quality enhancements

* Fixed an issue where the color picker was displayed in the wrong location on macOS in hardware-accelerated rendering mode in Avalonia applications.

[chromium-jun-08-2026]: https://chromereleases.googleblog.com/2026/06/stable-channel-update-for-desktop_0153744567.html
[cve-2026-11628]: https://nvd.nist.gov/vuln/detail/CVE-2026-11628
[cve-2026-11629]: https://nvd.nist.gov/vuln/detail/CVE-2026-11629
[cve-2026-11630]: https://nvd.nist.gov/vuln/detail/CVE-2026-11630
[cve-2026-11631]: https://nvd.nist.gov/vuln/detail/CVE-2026-11631
[cve-2026-11645]: https://nvd.nist.gov/vuln/detail/CVE-2026-11645
