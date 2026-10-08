# <a id="DotNetBrowser_Cast_ResultCode"></a> Enum ResultCode

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

Contains the codes indicating the result of creating a cast session.

```csharp
public enum ResultCode
```

## Fields

`Cancelled = 8` 

The cast session has been canceled, i.e. via the "Cancel" button in the screen picker.



`CastSessionAlreadyExists = 9` 

The cast session can not be created since it already exists.



`CastSessionAlreadyTerminated = 11` 

The cast session has already been terminated.



`CastSessionNotFound = 4` 

The cast session was not found.



`DesktopPickerFailed = 10` 

An attempt to show the screen picker has failed.



`InvalidOrigin = 6` 

The origin of the web content is not allowed to start a cast session.



`NoSupportedProvider = 7` 

The media source provider is not supported.



`NotificationDisabled = 14` 

Failed to launch session as the notifications are disabled on the receiver device.



`Ok = 2` 

The cast session successfully started.



`ReceiverNotFound = 5` 

The receiver was not found when starting the cast session.



`RedundantRequest = 12` 

The cast request is redundant since the desired cast session is already active.



`TimedOut = 3` 

The cast session has not been created within the specified time.



`UnknownError = 1` 

The error is unknown.



`UserNotAllowed = 13` 

The user has declined the cast request.



