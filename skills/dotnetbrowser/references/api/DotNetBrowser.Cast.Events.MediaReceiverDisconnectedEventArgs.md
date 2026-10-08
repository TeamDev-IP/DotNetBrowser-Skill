# <a id="DotNetBrowser_Cast_Events_MediaReceiverDisconnectedEventArgs"></a> Class MediaReceiverDisconnectedEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.IMediaReceiver.Disconnected" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MediaReceiverDisconnectedEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[MediaReceiverDisconnectedEventArgs](DotNetBrowser.Cast.Events.MediaReceiverDisconnectedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Cast_Events_MediaReceiverDisconnectedEventArgs_MediaReceiver"></a> MediaReceiver

Gets the media receiver that has been disconnected.

```csharp
public IMediaReceiver MediaReceiver { get; }
```

#### Property Value

 [IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)

