# <a id="DotNetBrowser_Downloads_Events_DownloadEventArgs"></a> Class DownloadEventArgs

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> events.

```csharp
public class DownloadEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[DownloadEventArgs](DotNetBrowser.Downloads.Events.DownloadEventArgs.md)

#### Derived

[CanceledEventArgs](DotNetBrowser.Downloads.Events.CanceledEventArgs.md), 
[FinishedEventArgs](DotNetBrowser.Downloads.Events.FinishedEventArgs.md), 
[InterruptedEventArgs](DotNetBrowser.Downloads.Events.InterruptedEventArgs.md), 
[PausedEventArgs](DotNetBrowser.Downloads.Events.PausedEventArgs.md), 
[UpdatedEventArgs](DotNetBrowser.Downloads.Events.UpdatedEventArgs.md)

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

### <a id="DotNetBrowser_Downloads_Events_DownloadEventArgs_Download"></a> Download

Gets the download instance which is the source of this event.

```csharp
public IDownload Download { get; }
```

#### Property Value

 [IDownload](DotNetBrowser.Downloads.IDownload.md)

