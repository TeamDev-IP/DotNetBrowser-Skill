# <a id="DotNetBrowser_Downloads"></a> Namespace DotNetBrowser.Downloads

### Namespaces

 [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)

 [DotNetBrowser.Downloads.Handlers](DotNetBrowser.Downloads.Handlers.md)

### Classes

 [DownloadInfo](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_DownloadInfo)

The general information about the download.

### Interfaces

 [IDownload](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_IDownload)

Represents a download.

 [IDownloads](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_IDownloads)

A service that can be used to work with the downloads.

### Enums

 [DownloadState](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_DownloadState)

The download state.

## <a id="DotNetBrowser_Downloads_DownloadInfo"></a> Class DownloadInfo

Namespace: [DotNetBrowser.Downloads](DotNetBrowser.Downloads.md)  
Assembly: DotNetBrowser.dll  

The general information about the download.

```csharp
public sealed class DownloadInfo
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DownloadInfo](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_DownloadInfo)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Downloads_DownloadInfo_MimeType"></a> MimeType

Gets the MIME type of this download.

```csharp
public MimeType MimeType { get; }
```

##### Property Value

 [MimeType](DotNetBrowser.Net.md#DotNetBrowser_Net_MimeType)

#### <a id="DotNetBrowser_Downloads_DownloadInfo_SuggestedFileName"></a> SuggestedFileName

Gets the suggested file name.

```csharp
public string SuggestedFileName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Downloads_DownloadInfo_Url"></a> Url

Gets the URL of this download.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Downloads_IDownload"></a> Interface IDownload

Namespace: [DotNetBrowser.Downloads](DotNetBrowser.Downloads.md)  
Assembly: DotNetBrowser.dll  

Represents a download.

```csharp
public interface IDownload : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Downloads_IDownload_Browser"></a> Browser

Gets the browser that initiated this download.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Downloads_IDownload_Extension"></a> Extension

Gets the extension that initiated this download.

```csharp
IExtension Extension { get; }
```

##### Property Value

 [IExtension](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtension)

#### <a id="DotNetBrowser_Downloads_IDownload_Info"></a> Info

Gets the additional information about this download.

```csharp
DownloadInfo Info { get; }
```

##### Property Value

 [DownloadInfo](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_DownloadInfo)

#### <a id="DotNetBrowser_Downloads_IDownload_IsPaused"></a> IsPaused

Indicates whether this download is paused.

```csharp
bool IsPaused { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Downloads_IDownload_State"></a> State

Gets the current download state.

```csharp
DownloadState State { get; }
```

##### Property Value

 [DownloadState](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_DownloadState)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

### Methods

#### <a id="DotNetBrowser_Downloads_IDownload_Cancel"></a> Cancel\(\)

Cancels this download. Will have no effect when the download is already cancelled.

```csharp
void Cancel()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Downloads_IDownload_Pause"></a> Pause\(\)

Pauses this download. Will have no effect when the download is already paused.

```csharp
void Pause()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Downloads_IDownload_Resume"></a> Resume\(\)

Resumes this download. Will have no effect when the download is not paused.

```csharp
void Resume()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Downloads_IDownload_Canceled"></a> Canceled

Occurs when the download was canceled.

```csharp
event EventHandler<CanceledEventArgs> Canceled
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CanceledEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_CanceledEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Downloads_IDownload_Finished"></a> Finished

Occurs when the download was finished.

```csharp
event EventHandler<FinishedEventArgs> Finished
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FinishedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_FinishedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Downloads_IDownload_Interrupted"></a> Interrupted

Occurs when the download was interrupted.

```csharp
event EventHandler<InterruptedEventArgs> Interrupted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[InterruptedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_InterruptedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Downloads_IDownload_Paused"></a> Paused

Occurs when the download was paused.

```csharp
event EventHandler<PausedEventArgs> Paused
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PausedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_PausedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Downloads_IDownload_Updated"></a> Updated

Occurs when the download state was updated.

```csharp
event EventHandler<UpdatedEventArgs> Updated
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[UpdatedEventArgs](DotNetBrowser.Downloads.Events.md#DotNetBrowser_Downloads_Events_UpdatedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Downloads_IDownloads"></a> Interface IDownloads

Namespace: [DotNetBrowser.Downloads](DotNetBrowser.Downloads.md)  
Assembly: DotNetBrowser.dll  

A service that can be used to work with the downloads.

```csharp
public interface IDownloads
```

### Properties

#### <a id="DotNetBrowser_Downloads_IDownloads_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

##### Property Value

 [IEngine](DotNetBrowser.Engine.md#DotNetBrowser_Engine_IEngine)

#### <a id="DotNetBrowser_Downloads_IDownloads_Items"></a> Items

Gets an immutable collection of all download items including already completed downloads during this session and
the active
downloads.

```csharp
IEnumerable<IDownload> Items { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IDownload](DotNetBrowser.Downloads.md#DotNetBrowser_Downloads_IDownload)\>

#### <a id="DotNetBrowser_Downloads_IDownloads_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

##### Property Value

 [IProfile](DotNetBrowser.Profile.md#DotNetBrowser_Profile_IProfile)

## <a id="DotNetBrowser_Downloads_DownloadState"></a> Enum DownloadState

Namespace: [DotNetBrowser.Downloads](DotNetBrowser.Downloads.md)  
Assembly: DotNetBrowser.dll  

The download state.

```csharp
public enum DownloadState
```

### Fields

`Cancelled = 3` 

The download has been cancelled.



`Complete = 2` 

The download is completely finished.



`InProgress = 1` 

The download is in progress.



`Interrupted = 4` 

The download has been interrupted.
