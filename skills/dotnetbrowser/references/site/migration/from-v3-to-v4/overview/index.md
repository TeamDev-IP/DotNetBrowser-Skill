
# Migrating from 3.x.x to 4.0.0

**Lead**
DotNetBrowser version 4.0.0 brings some improvements to both internal features and public API of the library. This guide shows how to make your application code written with DotNetBrowser version 3.x.x compatible with version 4.0.0.


### Why migrate?

We recommend updating your code to the latest version because all the new features, Chromium upgrades, support of new operating systems and .NET versions, bug fixes, security patches, performance, and memory usage enhancements are applied on top of the latest version.

### How long does it take?

From our experience, upgrade to a new version may take from a couple of hours to a few days depending on the number of the features you use in your application. As usual, we strongly recommend to test your software after the upgrade in all the environments it supports.

### Getting help

In case you did not find the answer in this guide and you need assistance with the migration, please [contact us](https://dotnetbrowser.support.teamdev.com/support/tickets/new). We will be happy to help.

## Key changes

### Obsolete and Removed API Changes

The following API changes were introduced in this version:

 * `ProprietaryFeatures.Widevine` flag has been removed.
It is replaced with the `IEngine.Widevine` property.
 * `ShowContextMenuParameters.CustomMenuItems` has been removed without a replacement.
 
### PermissionType enum update

**Renumbered existing values:**

| Member | Old value | New value |
|---|---|---|
| `WakeLockScreen` | 15 | 16 |
| `WakeLockSystem` | 16 | 17 |
| `ClipboardReadWrite` | 12 | 18 |
| `ClipboardSanitizedWrite` | 13 | 19 |
| `LocalFonts` | 14 | 24 |
| `LocalNetworkAccess` | 17 | 33 |

**New values added (12–36 range):**
`PaymentHandler`, `BackgroundFetch`, `IdleDetection`, `PeriodicBackgroundSync`, `Vr`, `StorageAccessGrant`, `CameraPanTiltZoom`, `WindowManagement`, `DisplayCapture`, `TopLevelStorageAccess`, `CapturedSurfaceControl`, `SpeakerSelection`, `KeyboardLock`, `PointerLock`, `AutomaticFullscreen`, `HandTracking`, `LocalNetwork`, `LoopbackNetwork`, `GeolocationApproximate`
