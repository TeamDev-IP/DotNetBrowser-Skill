# <a id="DotNetBrowser_Permissions_PermissionType"></a> Enum PermissionType

Namespace: [DotNetBrowser.Permissions](DotNetBrowser.Permissions.md)  
Assembly: DotNetBrowser.dll  

Represents the permission types.

```csharp
public enum PermissionType
```

## Fields

`AudioCapture = 8` 

The permission associated with the access to the audio capture devices.



`AutomaticFullscreen = 31` 

The permission to enter fullscreen mode without a prior user gesture.



`BackgroundFetch = 13` 

The permission for a service worker to download large resources in the background after
the user leaves the page.



`BackgroundSync = 10` 

The permission associated with the usage of Background Sync web API.



`CameraPanTiltZoom = 22` 

The permission to control camera pan, tilt, and zoom (PTZ) when capturing video.



`CapturedSurfaceControl = 27` 

The permission to scroll or zoom a surface captured via <code>getDisplayMedia()</code>.



`ClipboardReadWrite = 18` 

The permission associated with the usage of the asynchronous methods in the Clipboard API.



`ClipboardSanitizedWrite = 19` 

The permission associated with the <code>Clipboard.writeText()</code> method in the Clipboard API.



`DisplayCapture = 25` 

The permission to capture display, window, or tab contents via <code>getDisplayMedia()</code>.



`Geolocation = 4` 

The permission associated with the access to precise geographic location.



`GeolocationApproximate = 36` 

The permission associated with the access to approximate (city-level) geographic location.



`HandTracking = 32` 

The permission to access hand/finger-tracking data during a WebXR session.



`IdleDetection = 14` 

The permission to detect when the user is idle (inactive or screen locked).



`KeyboardLock = 29` 

The permission to capture system-level keyboard shortcuts (e.g. Escape, Alt+Tab) via
the Keyboard Lock API.



`LocalFonts = 24` 

The permission associated with the usage of the Local Font Access API. This permission
allows accessing the locally installed fonts and obtaining low-level details about them.



`LocalNetwork = 34` 

The permission for a page to access local network addresses (e.g. 192.168.x.x). Part of
Private Network Access.



`LocalNetworkAccess = 33` 

The permission associated with the usage of the Local Network Access API. This permission
prevents undesired requests to insecure devices on the local network.



`LoopbackNetwork = 35` 

The permission for a page to access localhost / 127.0.0.1. Part of Private Network Access.



`Midi = 6` 

The permission associated with the usage of Web MIDI API (without SysEx).



`MidiSysex = 2` 

The permission associated with the usage of Web MIDI API (with SysEx messages support).



`Notifications = 3` 

The permission associated with the usage of the Notifications API.



`PaymentHandler = 12` 

The permission for a service worker to handle payment requests via the Payment Handler API.



`PeriodicBackgroundSync = 15` 

The permission for a service worker to periodically wake up and sync data in the background.



`PersistentStorage = 7` 

The Persistent Storage permission (Durable Storage).



`PointerLock = 30` 

The permission to lock the mouse pointer to the page via the Pointer Lock API.



`ProtectedMediaIdentifier = 5` 

The protected media identifier permission.



`Sensors = 11` 

The permission to use motion and light sensors.



`SpeakerSelection = 28` 

The permission to select a specific audio output device (speaker/headphones).



`StorageAccessGrant = 21` 

The permission for a cross-origin iframe to access its first-party cookies via the
Storage Access API.



`TopLevelStorageAccess = 26` 

The permission for a top-level document to access unpartitioned cookies via the
Storage Access API.



`Unknown = 1` 

The unknown permission type.



`VideoCapture = 9` 

The permission associated with the access to the video capture devices.



`Vr = 20` 

The permission to create immersive VR sessions via the WebXR Device API.



`WakeLockScreen = 16` 

The permission associated with the usage of the Screen Wake Lock API. This permission
prevents the screen from turning off or dimming. Only visible documents can acquire the
screen wake lock.



`WakeLockSystem = 17` 

The permission associated with the usage of the System Wake Lock API. This permission
prevents the system from suspending.



`WindowManagement = 23` 

The permission to enumerate connected screens and place windows on them via the
Multi-Screen Window Placement API.



