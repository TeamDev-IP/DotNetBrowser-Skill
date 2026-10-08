# <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs"></a> Class RequestCompletedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.RequestCompleted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class RequestCompletedEventArgs : NetworkEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.NetworkEventArgs.md) ← 
[RequestCompletedEventArgs](DotNetBrowser.Net.Events.RequestCompletedEventArgs.md)

#### Inherited Members

[NetworkEventArgs.UrlRequest](DotNetBrowser.Net.Events.NetworkEventArgs.md\#DotNetBrowser\_Net\_Events\_NetworkEventArgs\_UrlRequest), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs_ErrorCode"></a> ErrorCode

Gets the URL request error code. In case the request has failed, contains the error code
of the network. Otherwise, has the default <xref href="DotNetBrowser.Net.NetError.Unknown" data-throw-if-not-resolved="false"></xref> value.

```csharp
public NetError ErrorCode { get; }
```

#### Property Value

 [NetError](DotNetBrowser.Net.NetError.md)

### <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs_IsCached"></a> IsCached

Indicates if the response has been taken from cache.

```csharp
public bool IsCached { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs_ResponseCode"></a> ResponseCode

Gets the response code of the current URL request (e.g., 200, 404, and so on).

```csharp
public int ResponseCode { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs_Status"></a> Status

Gets the status of the current URL request.

```csharp
public RequestStatus Status { get; }
```

#### Property Value

 [RequestStatus](DotNetBrowser.Net.RequestStatus.md)

