# <a id="DotNetBrowser_Cast_Events_MediaReceiverDiscoveredEventArgs"></a> Class MediaReceiverDiscoveredEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.IMediaReceivers.Discovered" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MediaReceiverDiscoveredEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[MediaReceiverDiscoveredEventArgs](DotNetBrowser.Cast.Events.MediaReceiverDiscoveredEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Cast_Events_MediaReceiverDiscoveredEventArgs_MediaReceiver"></a> MediaReceiver

Gets the discovered receiver.

```csharp
public IMediaReceiver MediaReceiver { get; }
```

#### Property Value

 [IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)

### <a id="DotNetBrowser_Cast_Events_MediaReceiverDiscoveredEventArgs_MediaReceivers"></a> MediaReceivers

Gets the <xref href="DotNetBrowser.Cast.IMediaReceivers" data-throw-if-not-resolved="false"></xref> instance initiated this event.

```csharp
public IMediaReceivers MediaReceivers { get; }
```

#### Property Value

 [IMediaReceivers](DotNetBrowser.Cast.IMediaReceivers.md)

