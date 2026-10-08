# <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs"></a> Class UpdatedEventArgs

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Updated" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class UpdatedEventArgs : DownloadEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[DownloadEventArgs](DotNetBrowser.Downloads.Events.DownloadEventArgs.md) ← 
[UpdatedEventArgs](DotNetBrowser.Downloads.Events.UpdatedEventArgs.md)

#### Inherited Members

[DownloadEventArgs.Download](DotNetBrowser.Downloads.Events.DownloadEventArgs.md\#DotNetBrowser\_Downloads\_Events\_DownloadEventArgs\_Download), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs_CurrentSpeed"></a> CurrentSpeed

Gets the estimated download speed.

```csharp
public long CurrentSpeed { get; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

### <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs_Progress"></a> Progress

Gets the rough percent complete.

```csharp
public float Progress { get; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs_ReceivedBytes"></a> ReceivedBytes

Gets the number or received (downloaded) bytes.

```csharp
public long ReceivedBytes { get; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

### <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs_TotalBytes"></a> TotalBytes

Gets the total size of the file.

```csharp
public long TotalBytes { get; }
```

#### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

