# <a id="DotNetBrowser_Engine_WidevineActivationStatus"></a> Enum WidevineActivationStatus

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Represents the result of attempting to activate the Widevine component.

```csharp
public enum WidevineActivationStatus
```

## Fields

`Activated = 1` 

The Widevine component is successfully activated and updated to the latest version.



`ActivationFailed = 3` 

Activation of the Widevine component has failed.

Activation can fail due to various reasons, such as network issues or some internal
errors on the remote service.

`NotSupported = 4` 

The Widevine component is not supported on the current platform and CPU architecture.



`RestartRequired = 2` 

The Widevine component is successfully activated, but the engine restart is required to
start using it.

This status is used on Linux only, because the engine cannot start using it right after
activation or updating to the latest version.

