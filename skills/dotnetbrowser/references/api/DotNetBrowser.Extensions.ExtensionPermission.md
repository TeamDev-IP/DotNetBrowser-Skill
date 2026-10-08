# <a id="DotNetBrowser_Extensions_ExtensionPermission"></a> Enum ExtensionPermission

Namespace: [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)  
Assembly: DotNetBrowser.dll  

The extension permission types.

```csharp
public enum ExtensionPermission
```

## Fields

`ActiveTab = 2` 

Gives temporary access to the active tab through a user gesture.



`Alarms = 3` 

Gives access to the chrome.alarms API.



`Background = 4` 

Makes Chrome start up early (as soon as the user logs into their computer—before the user
launches Chrome), and shut down late (even after its last window is closed until the user
explicitly quits Chrome).
In DotNetBrowser this permission has no effect.



`Bookmarks = 5` 

Gives access to the `chrome.bookmarks` API.



`BrowsingData = 6` 

Gives access to the `chrome.browsingData` API.



`CertificateProvider = 7` 

ChromeOS only. Gives access to the `chrome.certificateProvider` API.



`ClipboardRead = 8` 

Required if the extension uses `document.execCommand('paste')`.



`ClipboardWrite = 9` 

Required if the extension uses `document.execCommand('copy')` or `document.execCommand('cut')`.



`ContentSettings = 10` 

Gives access to the `chrome.contentSettings` API.



`ContextMenus = 11` 

Gives access to the `chrome.contextMenus` API.



`Cookies = 12` 

Gives access to the `chrome.cookies` API.



`Debugger = 13` 

Gives access to the `chrome.debugger` API.



`DeclarativeContent = 14` 

Gives access to the `chrome.declarativeContent` API.



`DeclarativeNetRequest = 15` 

Gives access to the `chrome.declarativeNetRequest` API.



`DeclarativeNetRequestFeedback = 17` 

Gives access to the `chrome.declarativeNetRequestFeedback` API which returns information on declarative rules
matched.



`DeclarativeNetRequestWithHostAccess = 16` 

Gives access to the `chrome.declarativeNetRequest` API, but requires host permissions to the request URL and
initiator to act on a request.



`DeclarativeWebRequest = 18` 

Gives access to the `chrome.declarativeWebRequest` API.
This API is deprecated. Check out the `chrome.declarativeNetRequest` API instead.



`DesktopCapture = 19` 

Gives access to the `chrome.desktopCapture` API.



`DocumentScan = 20` 

Gives access to the `chrome.documentScan` API.



`Downloads = 21` 

Gives access to the `chrome.downloads` API.

In DotNetBrowser the downloads API is not supported. Extensions are not allowed
to initiate downloads.

`DownloadsOpen = 69` 

The permission required to use the `chrome.downloads.open()` method.



`DownloadsUI = 70` 

The permission required to use the `chrome.downloads.setUiOptions()` method.In DotNetBrowser this method has no
effect.



`EnterpriseDeviceAttributes = 22` 

Gives access to the `chrome.enterprise.deviceAttributes` API.



`EnterpriseHardwarePlatform = 23` 

Gives access to the `chrome.enterprise.hardwarePlatform` API.



`EnterpriseNetworkingAttributes = 24` 

Gives access to the `chrome.enterprise.networkingAttributes` API.



`EnterprisePlatformKeys = 25` 

Gives access to the `chrome.enterprise.platformKeys` API.



`Experimental = 26` 

Gives access to the `chrome.experimental.*` APIs.



`FileBrowserHandler = 27` 

ChromeOS only. Gives access to the `chrome.fileBrowserHandler` API.



`FileSystemProvider = 28` 

ChromeOS only. Gives access to the `chrome.fileSystemProvider` API.



`FontSettings = 29` 

Gives access to the `chrome.fontSettings` API.



`Gcm = 30` 

Gives access to the `chrome.gcm` API.



`Geolocation = 31` 

Allows the extension to use the geolocation API without prompting the user for permission.



`History = 32` 

Gives access to the `chrome.history` API.



`Identity = 33` 

Gives access to the `chrome.identity` API.



`Idle = 34` 

Gives access to the `chrome.idle` API.



`LoginState = 35` 

ChromeOS only. Gives access to the `chrome.loginState` API.



`Management = 36` 

Gives access to the `chrome.management` API.



`NativeMessaging = 37` 

Gives access to the native messaging API.



`Notifications = 38` 

Gives access to the `chrome.notifications` API.



`Offscreen = 39` 

Gives access to the `chrome.offscreen` API.



`PageCapture = 40` 

Gives access to the `chrome.pageCapture` API.



`PlatformKeys = 41` 

ChromeOS only. Gives access to the `chrome.platformKeys` API.



`Power = 42` 

Gives access to the `chrome.power` API.



`PrinterProvider = 43` 

Gives access to the `chrome.printerProvider` API.



`Printing = 44` 

ChromeOS only. Gives access to the `chrome.printing` API.



`PrintingMetrics = 45` 

ChromeOS only. Gives access to the `chrome.printingMetrics` API.



`Privacy = 46` 

Gives access to the `chrome.privacy` API.



`Process = 47` 

Gives access to the `chrome.processes` API.



`Proxy = 48` 

Gives access to the `chrome.proxy` API.



`Scripting = 49` 

Gives access to the `chrome.scripting` API.



`Search = 50` 

Gives access to the `chrome.search` API.



`Sessions = 51` 

Gives access to the `chrome.sessions` API.



`Storage = 52` 

Gives access to the `chrome.storage` API.



`SystemCpu = 53` 

Gives access to the `chrome.system.cpu` API.



`SystemDisplay = 54` 

Gives access to the `chrome.system.display` API.



`SystemMemory = 55` 

Gives access to the `chrome.system.memory` API.



`SystemStorage = 56` 

Gives access to the `chrome.system.storage` API.



`TabCapture = 57` 

Gives access to the `chrome.tabCapture` API.



`TabGroups = 58` 

Gives access to the `chrome.tabGroups` API.



`Tabs = 59` 

Gives access to privileged fields of the Tab objects used by several APIs including `chrome.tabs` and
`chrome.windows`. In many circumstances your extension will not need
to declare the "tabs" permission to make use of these APIs.



`TopSites = 60` 

Gives access to the `chrome.topSites` API.



`Tts = 61` 

Gives access to the `chrome.tts` API.



`TtsEngine = 62` 

Gives access to the `chrome.ttsEngine` API.



`Unknown = 1` 

An unknown permission type.



`UnlimitedStorage = 63` 

Provides an unlimited quota for storing client-side data, such as databases and local storage files. Without this
permission, the extension is limited to 10 MB of local storage.

Note: This permission applies only to Web SQL Database and application cache (see issue 58985).
Also, it doesn't currently work with wildcard subdomains such as http://*.example.com.

`VpnProvider = 64` 

ChromeOS only. Gives access to the `chrome.vpnProvider` API.



`Wallpaper = 65` 

ChromeOS only. Gives access to the `chrome.wallpaper` API.



`WebAuthenticationProxy = 71` 

Gives access to the `chrome.webAuthenticationProxy` API.



`WebNavigation = 66` 

Gives access to the `chrome.webNavigation` API.



`WebRequest = 67` 

Gives access to the `chrome.webRequest` API.



`WebRequestBlocking = 68` 

Required if the extension uses the `chrome.webRequest` API in a blocking fashion.



