# <a id="DotNetBrowser_Net_Events_ResponseStartedEventArgs"></a> Class ResponseStartedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.ResponseStarted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class ResponseStartedEventArgs : NetworkEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.NetworkEventArgs.md) ← 
[ResponseStartedEventArgs](DotNetBrowser.Net.Events.ResponseStartedEventArgs.md)

#### Inherited Members

[NetworkEventArgs.UrlRequest](DotNetBrowser.Net.Events.NetworkEventArgs.md\#DotNetBrowser\_Net\_Events\_NetworkEventArgs\_UrlRequest), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Events_ResponseStartedEventArgs_ResponseCode"></a> ResponseCode

Gets the response code of the current URL request (e.g., 200, 404, and so on).
Returns 0 if the request has been failed or canceled.

```csharp
public int ResponseCode { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

