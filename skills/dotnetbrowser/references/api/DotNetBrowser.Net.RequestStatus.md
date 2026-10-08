# <a id="DotNetBrowser_Net_RequestStatus"></a> Enum RequestStatus

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The status of a URL request.

```csharp
public enum RequestStatus
```

## Fields

`Canceled = 4` 

A request was cancelled programmatically.



`Failed = 5` 

A request failed for some reason.



`IoPending = 3` 

An IO request is pending. It is expected that the request issuer will be informed when it
is completed.



`Success = 2` 

A request succeeded.



`Unknown = 1` 

The request status is unknown.



