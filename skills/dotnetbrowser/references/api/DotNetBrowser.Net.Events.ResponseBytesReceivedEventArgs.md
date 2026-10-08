# <a id="DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs"></a> Class ResponseBytesReceivedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.ResponseBytesReceived" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ResponseBytesReceivedEventArgs : NetworkEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.NetworkEventArgs.md) ← 
[ResponseBytesReceivedEventArgs](DotNetBrowser.Net.Events.ResponseBytesReceivedEventArgs.md)

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

### <a id="DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs_Data"></a> Data

Gets the received part of HTTP response body.

```csharp
public byte[] Data { get; }
```

#### Property Value

 [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

### <a id="DotNetBrowser_Net_Events_ResponseBytesReceivedEventArgs_MimeType"></a> MimeType

Gets the MIME type from the headers.

```csharp
public MimeType MimeType { get; }
```

#### Property Value

 [MimeType](DotNetBrowser.Net.MimeType.md)

