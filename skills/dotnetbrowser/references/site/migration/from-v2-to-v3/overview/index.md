
# Migrating from 2.x.x to 3.0.0

**Lead**
DotNetBrowser version 3.0.0 brings some improvements to both internal features and public API of the library. This guide shows how to make your application code written with DotNetBrowser version 2.x.x compatible with version 3.0.0.


### Why migrate?

We recommend you to update your code to the latest version because all the new features, Chromium upgrades, support of new operating systems and .NET versions, bug fixes, security patches, performance, and memory usage enhancements are applied on top of the latest version.

### How long does it take?

From our experience, upgrade to a new version may take from a couple of hours to a few days depending on the number of the features you use in your application. As usual, we strongly recommend to test your software after the upgrade in all the environments it supports.

### Getting help

In case you did not find the answer in this guide and you need assistance with the migration, please [contact us](https://dotnetbrowser.support.teamdev.com/support/tickets/new). We will be happy to help.

## Key changes

### Obsolete API was removed

The API that was previously marked as obsolete in DotNetBrowser 2, is no longer available in 3.0.0.

Here is the list of the API removed and its replacements:

 * `LoadUrlParameters.PostData`, which is replaced with `LoadUrlParameters.UploadData`;
 * `VerifyCertificateParameters.VerifyStatuses`, which is replaced with `VerifyCertificateParameters.VerifyErrors`;
 * `BinariesExtractionOptions.CheckLastModificationDate`, which is replaced with `BinariesExtractionOptions.VerificationLevel`;
 * `ISpellChecker.DictionaryNames`, which is replaced by `ISpellChecker.Languages`.

 The following properties were previously available in the `IEngine` interface, however, they were related to the default profile and marked as obsolete:

 * `IEngine.CookieStore`
 * `IEngine.Downloads`
 * `IEngine.HttpCache`
 * `IEngine.Network`
 * `IEngine.Permissions`
 * `IEngine.Plugins`
 * `IEngine.Proxy`
 * `IEngine.SpellChecker`
 * `IEngine.ZoomLevels`

These properties were removed from the `IEngine` interface, and now available in the default profile only. For example, if you were using `engine.Network`, you need to use `engine.Profiles.Default.Network` instead.

### `GoogleTrafficDisabled` option was removed

Some of our clients reported that Chromium sends unexpected requests to external web services sometimes. We figured out that Chromium features such as Google Cloud Messaging, Translate Ranker, Extensions Updater, Safe Browsing, Spell Checker, Widevine etc. make requests to the external Google web services such as https://ssl.gstatic.com, https://clients4.google.com, to work properly.

We understand that any unexpected request to an external web service might be treated as a security threat and should be blocked. We analyzed all the Chromium features that send requests to external web services and ensured you have full control over them via the DotNetBrowser API. The features you cannot control using the API are disabled by default to prevent unexpected requests to external web services.

In terms of this enhancement, we removed the `GoogleTrafficDisabled` Engine option because it’s not needed anymore.
