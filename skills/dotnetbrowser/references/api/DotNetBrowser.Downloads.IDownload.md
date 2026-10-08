# <a id="DotNetBrowser_Downloads_IDownload"></a> Interface IDownload

Namespace: [DotNetBrowser.Downloads](DotNetBrowser.Downloads.md)  
Assembly: DotNetBrowser.dll  

Represents a download.

```csharp
public interface IDownload : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Downloads_IDownload_Browser"></a> Browser

Gets the browser that initiated this download.

```csharp
IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Downloads_IDownload_Extension"></a> Extension

Gets the extension that initiated this download.

```csharp
IExtension Extension { get; }
```

#### Property Value

 [IExtension](DotNetBrowser.Extensions.IExtension.md)

### <a id="DotNetBrowser_Downloads_IDownload_Info"></a> Info

Gets the additional information about this download.

```csharp
DownloadInfo Info { get; }
```

#### Property Value

 [DownloadInfo](DotNetBrowser.Downloads.DownloadInfo.md)

### <a id="DotNetBrowser_Downloads_IDownload_IsPaused"></a> IsPaused

Indicates whether this download is paused.

```csharp
bool IsPaused { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Downloads_IDownload_State"></a> State

Gets the current download state.

```csharp
DownloadState State { get; }
```

#### Property Value

 [DownloadState](DotNetBrowser.Downloads.DownloadState.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

## Methods

### <a id="DotNetBrowser_Downloads_IDownload_Cancel"></a> Cancel\(\)

Cancels this download. Will have no effect when the download is already cancelled.

```csharp
void Cancel()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Downloads_IDownload_Pause"></a> Pause\(\)

Pauses this download. Will have no effect when the download is already paused.

```csharp
void Pause()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Downloads_IDownload_Resume"></a> Resume\(\)

Resumes this download. Will have no effect when the download is not paused.

```csharp
void Resume()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Downloads_IDownload_Canceled"></a> Canceled

Occurs when the download was canceled.

```csharp
event EventHandler<CanceledEventArgs> Canceled
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CanceledEventArgs](DotNetBrowser.Downloads.Events.CanceledEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Downloads_IDownload_Finished"></a> Finished

Occurs when the download was finished.

```csharp
event EventHandler<FinishedEventArgs> Finished
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FinishedEventArgs](DotNetBrowser.Downloads.Events.FinishedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Downloads_IDownload_Interrupted"></a> Interrupted

Occurs when the download was interrupted.

```csharp
event EventHandler<InterruptedEventArgs> Interrupted
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[InterruptedEventArgs](DotNetBrowser.Downloads.Events.InterruptedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Downloads_IDownload_Paused"></a> Paused

Occurs when the download was paused.

```csharp
event EventHandler<PausedEventArgs> Paused
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PausedEventArgs](DotNetBrowser.Downloads.Events.PausedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Downloads_IDownload_Updated"></a> Updated

Occurs when the download state was updated.

```csharp
event EventHandler<UpdatedEventArgs> Updated
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[UpdatedEventArgs](DotNetBrowser.Downloads.Events.UpdatedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownload" data-throw-if-not-resolved="false"></xref> has already been disposed.

