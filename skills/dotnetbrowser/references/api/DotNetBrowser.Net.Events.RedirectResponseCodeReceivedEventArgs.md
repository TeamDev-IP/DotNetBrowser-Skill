# <a id="DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs"></a> Class RedirectResponseCodeReceivedEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Net.INetwork.RedirectResponseCodeReceived" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class RedirectResponseCodeReceivedEventArgs : NetworkEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.NetworkEventArgs.md) ← 
[RedirectResponseCodeReceivedEventArgs](DotNetBrowser.Net.Events.RedirectResponseCodeReceivedEventArgs.md)

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

### <a id="DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs_NewUrl"></a> NewUrl

Gets the new URL.

```csharp
public string NewUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_Events_RedirectResponseCodeReceivedEventArgs_ResponseCode"></a> ResponseCode

Gets the HTTP response code (e.g., 200, 404, and so on).

```csharp
public int ResponseCode { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

