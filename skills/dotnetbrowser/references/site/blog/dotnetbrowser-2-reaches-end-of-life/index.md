# DotNetBrowser 2 reaches end-of-life

With the release of DotNetBrowser 3 in December 2024,
we [announced][announcement] one more year of support for DotNetBrowser 2. 
That year is now almost over.

On December 3, 2025, DotNetBrowser 2 will officially reach end of life. 
This post explains what that means in practice.

## What changes

Starting with December 3, we will no longer release new versions of
DotNetBrowser 2 including minor and patch versions.

We will add new features, fix bugs, and upgrade Chromium in DotNetBrowser 3
only. We always recommend using the latest version to keep your software secure
and up to date.

You can find the latest version on the [product home page][product-page] or
in [Release Notes][release-notes].

## What doesn't change

After the end-of-life date, DotNetBrowser 2 will continue working as before
without disruption. In line with its perpetual license, we designed
DotNetBrowser to work perpetually.

We will keep DotNetBrowser 2 available in NuGet, but it will be hidden from
search. The existing download links will remain active. The API references for
DotNetBrowser 2 will remain on the same [web page][api-reference].

## How do I switch to DotNetBrowser 3?

In most cases, you can simply replace your project's dependencies from
DotNetBrowser 2 to DotNetBrowser 3. The versions are mostly compatible 
with minor API differences, which we document in detail in
the [migration guide][migration-guide].

If you have any questions or need assistance with the upgrade, please feel free
to contact us at 
[https://teamdev.com/contacts](https://teamdev.com/contacts/).

[announcement]: https://teamdev.com/dotnetbrowser/releases/2024/v3-0-0/#dotnetbrowser-2-updates
[product-page]: https://teamdev.com/dotnetbrowser/
[release-notes]: https://teamdev.com/dotnetbrowser/releases/
[api-reference]: https://teamdev.com/dotnetbrowser/docs/reference/
[migration-guide]: https://teamdev.com/dotnetbrowser/migration/from-v2-to-v3/overview/
