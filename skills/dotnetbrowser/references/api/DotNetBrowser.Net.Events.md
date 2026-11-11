# <a id="DotNetBrowser_Net_Events"></a> Namespace DotNetBrowser.Net.Events

### Classes

 [ConnectionTypeChangedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ConnectionTypeChangedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.ConnectionTypeChanged" data-throw-if-not-resolved="false"></xref> event.

 [NetworkEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs)

The base class for <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> event arguments.

 [PacScriptErrorEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_PacScriptErrorEventArgs)

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.PacScriptErrorOccurred" data-throw-if-not-resolved="false"></xref> event.

 [RedirectResponseCodeReceivedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.RedirectResponseCodeReceived" data-throw-if-not-resolved="false"></xref> event.

 [RequestCompletedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RequestCompletedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.RequestCompleted" data-throw-if-not-resolved="false"></xref> event.

 [RequestDestroyedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RequestDestroyedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.RequestDestroyed" data-throw-if-not-resolved="false"></xref> event.

 [ResponseBytesReceivedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.ResponseBytesReceived" data-throw-if-not-resolved="false"></xref> event.

 [ResponseStartedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ResponseStartedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.ResponseStarted" data-throw-if-not-resolved="false"></xref> event.

### Enums

 [ConnectionType](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ConnectionType)

The network connection type.

## <a id="DotNetBrowser_Net_Events_ConnectionTypeChangedEventArgs"></a> Class ConnectionTypeChangedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.ConnectionTypeChanged" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ConnectionTypeChangedEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ConnectionTypeChangedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ConnectionTypeChangedEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Events_ConnectionTypeChangedEventArgs_ConnectionType"></a> ConnectionType

Gets the connection type of the network at the time of the event.

```csharp
public ConnectionType ConnectionType { get; }
```

##### Property Value

 [ConnectionType](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ConnectionType)

## <a id="DotNetBrowser_Net_Events_NetworkEventArgs"></a> Class NetworkEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> event arguments.

```csharp
public class NetworkEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs)

##### Derived

[RedirectResponseCodeReceivedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs), 
[RequestCompletedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RequestCompletedEventArgs), 
[RequestDestroyedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RequestDestroyedEventArgs), 
[ResponseBytesReceivedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs), 
[ResponseStartedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ResponseStartedEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Events_NetworkEventArgs_UrlRequest"></a> UrlRequest

The URL request received from the Chromium engine.

```csharp
public UrlRequest UrlRequest { get; }
```

##### Property Value

 [UrlRequest](DotNetBrowser.Net.md#DotNetBrowser_Net_UrlRequest)

## <a id="DotNetBrowser_Net_Events_PacScriptErrorEventArgs"></a> Class PacScriptErrorEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.PacScriptErrorOccurred" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class PacScriptErrorEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PacScriptErrorEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_PacScriptErrorEventArgs)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Events_PacScriptErrorEventArgs_ErrorText"></a> ErrorText

Gets the ErrorText.

```csharp
public string ErrorText { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Events_PacScriptErrorEventArgs_LineNumber"></a> LineNumber

Gets the LineNumber which contains the error.

```csharp
public uint LineNumber { get; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

## <a id="DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs"></a> Class RedirectResponseCodeReceivedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.RedirectResponseCodeReceived" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class RedirectResponseCodeReceivedEventArgs : NetworkEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs) ← 
[RedirectResponseCodeReceivedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs)

##### Inherited Members

[NetworkEventArgs.UrlRequest](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs_UrlRequest), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs_NewUrl"></a> NewUrl

Gets the new URL.

```csharp
public string NewUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs_ResponseCode"></a> ResponseCode

Gets the HTTP response code (e.g., 200, 404, and so on).

```csharp
public int ResponseCode { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs"></a> Class RequestCompletedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.RequestCompleted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class RequestCompletedEventArgs : NetworkEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs) ← 
[RequestCompletedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RequestCompletedEventArgs)

##### Inherited Members

[NetworkEventArgs.UrlRequest](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs_UrlRequest), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs_ErrorCode"></a> ErrorCode

Gets the URL request error code. In case the request has failed, contains the error code
of the network. Otherwise, has the default <xref href="DotNetBrowser.Net.NetError.Unknown" data-throw-if-not-resolved="false"></xref> value.

```csharp
public NetError ErrorCode { get; }
```

##### Property Value

 [NetError](DotNetBrowser.Net.md#DotNetBrowser_Net_NetError)

#### <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs_IsCached"></a> IsCached

Indicates if the response has been taken from cache.

```csharp
public bool IsCached { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs_ResponseCode"></a> ResponseCode

Gets the response code of the current URL request (e.g., 200, 404, and so on).

```csharp
public int ResponseCode { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Net_Events_RequestCompletedEventArgs_Status"></a> Status

Gets the status of the current URL request.

```csharp
public RequestStatus Status { get; }
```

##### Property Value

 [RequestStatus](DotNetBrowser.Net.md#DotNetBrowser_Net_RequestStatus)

## <a id="DotNetBrowser_Net_Events_RequestDestroyedEventArgs"></a> Class RequestDestroyedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.RequestDestroyed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class RequestDestroyedEventArgs : NetworkEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs) ← 
[RequestDestroyedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_RequestDestroyedEventArgs)

##### Inherited Members

[NetworkEventArgs.UrlRequest](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs_UrlRequest), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs"></a> Class ResponseBytesReceivedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.ResponseBytesReceived" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ResponseBytesReceivedEventArgs : NetworkEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs) ← 
[ResponseBytesReceivedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs)

##### Inherited Members

[NetworkEventArgs.UrlRequest](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs_UrlRequest), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs_Data"></a> Data

Gets the received part of HTTP response body.

```csharp
public byte[] Data { get; }
```

##### Property Value

 [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

#### <a id="DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs_MimeType"></a> MimeType

Gets the MIME type from the headers.

```csharp
public MimeType MimeType { get; }
```

##### Property Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

## <a id="DotNetBrowser_Net_Events_ResponseStartedEventArgs"></a> Class ResponseStartedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.ResponseStarted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class ResponseStartedEventArgs : NetworkEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs) ← 
[ResponseStartedEventArgs](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_ResponseStartedEventArgs)

##### Inherited Members

[NetworkEventArgs.UrlRequest](DotNetBrowser.Net.Events.md#DotNetBrowser_Net_Events_NetworkEventArgs_UrlRequest), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Net_Events_ResponseStartedEventArgs_ResponseCode"></a> ResponseCode

Gets the response code of the current URL request (e.g., 200, 404, and so on).
Returns 0 if the request has been failed or canceled.

```csharp
public int ResponseCode { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Net_Events_ConnectionType"></a> Enum ConnectionType

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

The network connection type.

```csharp
public enum ConnectionType
```

### Fields

`Bluetooth = 5` 

A Bluetooth connection.



`Ethernet = 6` 

An Ethernet connection.



`None = 7` 

No connection.



`Type2G = 1` 

A 2G connection.



`Type3G = 2` 

A 3G connection.



`Type4G = 3` 

A 4G connection.



`Type5G = 4` 

A 5G connection.



`Unknown = 8` 

A connection exists, but its type is unknown.



`Wifi = 9` 

A Wi-Fi connection.
