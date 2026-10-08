# <a id="DotNetBrowser_Downloads_Events_InterruptedEventArgs"></a> Class InterruptedEventArgs

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Interrupted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class InterruptedEventArgs : DownloadEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[DownloadEventArgs](DotNetBrowser.Downloads.Events.DownloadEventArgs.md) ← 
[InterruptedEventArgs](DotNetBrowser.Downloads.Events.InterruptedEventArgs.md)

#### Inherited Members

[DownloadEventArgs.Download](DotNetBrowser.Downloads.Events.DownloadEventArgs.md\#DotNetBrowser\_Downloads\_Events\_DownloadEventArgs\_Download), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Downloads_Events_InterruptedEventArgs_InterruptionReason"></a> InterruptionReason

Gets the possible download interruption reason.

```csharp
public DownloadInterruptionReason InterruptionReason { get; }
```

#### Property Value

 [DownloadInterruptionReason](DotNetBrowser.Downloads.Events.DownloadInterruptionReason.md)

