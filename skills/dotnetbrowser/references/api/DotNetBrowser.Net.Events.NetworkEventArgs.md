# <a id="DotNetBrowser_Net_Events_NetworkEventArgs"></a> Class NetworkEventArgs

Namespace: [DotNetBrowser.Net.Events](DotNetBrowser.Net.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Net.INetwork" data-throw-if-not-resolved="false"></xref> event arguments.

```csharp
public class NetworkEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[NetworkEventArgs](DotNetBrowser.Net.Events.NetworkEventArgs.md)

#### Derived

[RedirectResponseCodeReceivedEventArgs](DotNetBrowser.Net.Events.RedirectResponseCodeReceivedEventArgs.md), 
[RequestCompletedEventArgs](DotNetBrowser.Net.Events.RequestCompletedEventArgs.md), 
[RequestDestroyedEventArgs](DotNetBrowser.Net.Events.RequestDestroyedEventArgs.md), 
[ResponseBytesReceivedEventArgs](DotNetBrowser.Net.Events.ResponseBytesReceivedEventArgs.md), 
[ResponseStartedEventArgs](DotNetBrowser.Net.Events.ResponseStartedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Events_NetworkEventArgs_UrlRequest"></a> UrlRequest

The URL request received from the Chromium engine.

```csharp
public UrlRequest UrlRequest { get; }
```

#### Property Value

 [UrlRequest](DotNetBrowser.Net.UrlRequest.md)

