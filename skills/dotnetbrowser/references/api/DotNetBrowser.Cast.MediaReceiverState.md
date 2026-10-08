# <a id="DotNetBrowser_Cast_MediaReceiverState"></a> Enum MediaReceiverState

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The state of the media receiver.

```csharp
public enum MediaReceiverState
```

## Fields

`Available = 1` 

The receiver is available to be cast to.



`Connected = 3` 

Content is currently cast to the receiver.



`Connecting = 2` 

The receiver is starting a new cast session. A receiver temporarily enters this
state when transitioning from Available to Connected.



`Disconnecting = 4` 

The receiver is still connected but is in the process of disconnecting. A receiver
temporarily enters this state when transitioning from Connected to Available.



`Unavailable = 5` 

The receiver is disconnected/cached (not available right now).



