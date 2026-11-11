# <a id="DotNetBrowser_Downloads_Events"></a> Namespace DotNetBrowser.Downloads.Events

### Classes

 [CanceledEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_CanceledEventArgs)

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Canceled" data-throw-if-not-resolved="false"></xref> event.

 [DownloadEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs)

The base class for <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> events.

 [FinishedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_FinishedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Finished" data-throw-if-not-resolved="false"></xref> event.

 [InterruptedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_InterruptedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Interrupted" data-throw-if-not-resolved="false"></xref> event.

 [PausedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_PausedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Paused" data-throw-if-not-resolved="false"></xref> event.

 [UpdatedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_UpdatedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Updated" data-throw-if-not-resolved="false"></xref> event.

### Enums

 [DownloadInterruptionReason](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadInterruptionReason)

Possible download interruption reason.

## <a id="DotNetBrowser_Downloads_Events_CanceledEventArgs"></a> Class CanceledEventArgs

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Canceled" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class CanceledEventArgs : DownloadEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[DownloadEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs) ← 
[CanceledEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_CanceledEventArgs)

##### Inherited Members

[DownloadEventArgs.Download](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs_Download), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Downloads_Events_DownloadEventArgs"></a> Class DownloadEventArgs

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> events.

```csharp
public class DownloadEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[DownloadEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs)

##### Derived

[CanceledEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_CanceledEventArgs), 
[FinishedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_FinishedEventArgs), 
[InterruptedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_InterruptedEventArgs), 
[PausedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_PausedEventArgs), 
[UpdatedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_UpdatedEventArgs)

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

#### <a id="DotNetBrowser_Downloads_Events_DownloadEventArgs_Download"></a> Download

Gets the download instance which is the source of this event.

```csharp
public IDownload Download { get; }
```

##### Property Value

 [IDownload](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_IDownload)

## <a id="DotNetBrowser_Downloads_Events_FinishedEventArgs"></a> Class FinishedEventArgs

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Finished" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class FinishedEventArgs : DownloadEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[DownloadEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs) ← 
[FinishedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_FinishedEventArgs)

##### Inherited Members

[DownloadEventArgs.Download](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs_Download), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Downloads_Events_InterruptedEventArgs"></a> Class InterruptedEventArgs

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Interrupted" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class InterruptedEventArgs : DownloadEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[DownloadEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs) ← 
[InterruptedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_InterruptedEventArgs)

##### Inherited Members

[DownloadEventArgs.Download](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs_Download), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Downloads_Events_InterruptedEventArgs_InterruptionReason"></a> InterruptionReason

Gets the possible download interruption reason.

```csharp
public DownloadInterruptionReason InterruptionReason { get; }
```

##### Property Value

 [DownloadInterruptionReason](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadInterruptionReason)

## <a id="DotNetBrowser_Downloads_Events_PausedEventArgs"></a> Class PausedEventArgs

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Paused" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class PausedEventArgs : DownloadEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[DownloadEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs) ← 
[PausedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_PausedEventArgs)

##### Inherited Members

[DownloadEventArgs.Download](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs_Download), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs"></a> Class UpdatedEventArgs

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Downloads.IDownload.Updated" data-throw-if-not-resolved="false"></xref> event.

```csharp
public class UpdatedEventArgs : DownloadEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[DownloadEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs) ← 
[UpdatedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_UpdatedEventArgs)

##### Inherited Members

[DownloadEventArgs.Download](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_DownloadEventArgs_Download), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs_CurrentSpeed"></a> CurrentSpeed

Gets the estimated download speed.

```csharp
public long CurrentSpeed { get; }
```

##### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

#### <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs_Progress"></a> Progress

Gets the rough percent complete.

```csharp
public float Progress { get; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs_ReceivedBytes"></a> ReceivedBytes

Gets the number or received (downloaded) bytes.

```csharp
public long ReceivedBytes { get; }
```

##### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

#### <a id="DotNetBrowser_Downloads_Events_UpdatedEventArgs_TotalBytes"></a> TotalBytes

Gets the total size of the file.

```csharp
public long TotalBytes { get; }
```

##### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

## <a id="DotNetBrowser_Downloads_Events_DownloadInterruptionReason"></a> Enum DownloadInterruptionReason

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

Possible download interruption reason.

```csharp
public enum DownloadInterruptionReason
```

### Fields

`Crash = 50` 

The browser crashed.
Internal use only:  resume pending downloads if possible.



`FileAccessDenied = 3` 

The file cannot be accessed due to security restrictions.
"Access Denied".



`FileBlocked = 11` 

The file was blocked due to local policy.
"Blocked"



`FileFailed = 2` 

Generic file operation failure.
"File Error".



`FileHashMismatch = 14` 

The partial file didn't match the expected hash.



`FileNameTooLong = 5` 

The directory or file name is too long.
"Path Too Long".



`FileNoSpace = 4` 

There is not enough room on the drive.
"Disk Full".



`FileSameAsSource = 15` 

The source and the target of the download were the same



`FileSecurityCheckFailed = 12` 

An attempt to check the safety of the download failed due to unexpected
reasons. See http:///crbug.com/153212.



`FileTooLarge = 6` 

The file is too large for the file system to handle.
"File Too Large".



`FileTooShort = 13` 

An attempt was made to seek past the end of a file in opening
a file (as part of resuming a previously interrupted download).



`FileTransientError = 10` 

The file was in use.
Too many files are opened at once.
We have run out of memory.
"Temporary Problem".



`FileVirusInfected = 7` 

The file contains a virus.
"Virus".



`NetworkDisconnected = 22` 

The network connection has been lost.
"Connection Lost".



`NetworkFailed = 20` 

Generic network failure.
"Network Error".



`NetworkInvalidRequest = 24` 

The network request was invalid. This may be due to the original URL or a
redirected URL:
- Having an unsupported scheme.
- Being an invalid URL.
- Being disallowed by policy.



`NetworkServerDown = 23` 

The server has gone down.
"Server Down".



`NetworkTimeout = 21` 

The network operation timed out.
"Operation Timed Out".



`ServerBadContent = 33` 

The server does not have the requested data.
"Unable to get file".



`ServerCertProblem = 35` 

Server certificate problem.



`ServerContentLengthMismatch = 38` 

The server sent fewer bytes than the content-length header. It may indicate
that the connection was closed prematurely, or the Content-Length header was
invalid. The download is only interrupted if strong validators are present.
Otherwise, it is treated as finished.



`ServerFailed = 30` 

The server indicates that the operation has failed (generic).
"Server Error".



`ServerForbidden = 36` 

Server access forbidden.



`ServerNoRange = 31` 

The server does not support range requests.
Internal use only:  must restart from the beginning.



`ServerUnauthorized = 34` 

Server didn't authorize access to resource.



`ServerUnreachable = 37` 

Unexpected server response. This might indicate that the responding server
may not be the intended server.



`Unknown = 1` 

There is no interruption reason.



`UserCanceled = 40` 

The user canceled the download.
"Canceled".



`UserShutdown = 41` 

The user shut down the browser.
Internal use only:  resume pending downloads if possible.
