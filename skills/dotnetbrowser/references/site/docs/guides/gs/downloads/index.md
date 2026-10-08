
# Downloads

**Lead**
This guide describes how to manage file downloads, track download progress, get the notification on download completion, and so on.


## Overview

To manage file downloads associated with a specific `Profile`, use the following approach:


**C#**
```csharp
IDownloads downloads = engine.Profiles.Default.Downloads;
```

**VB**
```vb
Dim downloads As IDownloads = engine.Profiles.Default.Downloads
```



Using `IEngine.Downloads` you will get the download service for the default profile.

Every time the DotNetBrowser needs to download a file, the `StartDownloadHandler` is used. In this handler, you can decide whether the file should be downloaded or the download request must be canceled.

The code sample below demonstrates how to cancel all download requests:


**C#**
```csharp
browser.StartDownloadHandler = 
    new Handler<StartDownloadParameters, StartDownloadResponse>(p =>
    {
        return StartDownloadResponse.Cancel();
    });
```

**VB**
```vb
browser.StartDownloadHandler = 
    New Handler(Of StartDownloadParameters, StartDownloadResponse)(Function(p)
        Return StartDownloadResponse.Cancel()
    End Function)
```



**Note**
By default, all download requests are canceled.


## Accepting a download

To change the default behavior and allow to download a file, use the following approach:


**C#**
```csharp
browser.StartDownloadHandler = 
    new Handler<StartDownloadParameters, StartDownloadResponse>((p) =>
    {
        return StartDownloadResponse.DownloadTo(Path.Combine(Path.GetTempPath(),
            p.Download.Info.SuggestedFileName));
    });
```

**VB**
```vb
browser.StartDownloadHandler =
    New Handler(Of StartDownloadParameters, StartDownloadResponse)(Function(p)
        Return StartDownloadResponse.DownloadTo(Path.Combine(Path.GetTempPath(),
            p.Download.Info.SuggestedFileName))
    End Function)
```



In the code sample above, we tell the library that the file can be downloaded and saved to a given destination file.

**Note**
Make sure that Chromium [main process](https://teamdev.com/dotnetbrowser/docs/guides/architecture/#chromium-main-process) has rights to create files in the provided destination directory. If the given directory already has a file with the identical name, then the file will be overridden automatically. We recommend checking the rights and the file existence before accepting the file download.


## Controlling a download process

To control the download process, use the `IDownload` instance which you can obtain from using the `StartDownloadHandler`.

### Pausing a download

To pause the download, use the `IDownload.Pause()` method:


**C#**
```csharp
download.Pause();
```

**VB**
```vb
download.Pause()
```



### Resuming a download

To resume the paused download, use the `IDownload.Resume()` method:


**C#**
```csharp
if (download.IsPaused) {
    download.Resume();
}
```

**VB**
```vb
If download.IsPaused Then
    download.Resume()
End If
```



### Canceling a download

You can cancel the download anytime unless the download is in a terminal state. This includes the successfully completed downloads, canceled downloads, and interrupted downloads that cannot be resumed. To find out whether download is in the terminal state, use the `IDownload.State` property. To cancel the download, use the `IDownload.Cancel()` method as shown in the code sample below:


**C#**
```csharp
if (download.State != DownloadState.Complete) {
    download.Cancel();
}
```

**VB**
```vb
If download.State <> DownloadState.Complete Then
    download.Cancel()
End If
```



## Download events

You can track the download progress, get notifications when the download is canceled, paused, interrupted, or complete.

### Download Canceled event

To get notifications when the `IDownload` is canceled, use the `Canceled` event:


**C#**
```csharp
download.Canceled += (s, e) => { };
```

**VB**
```vb
AddHandler download.Canceled, Sub(s, e)
End Sub
```



### Download Finished event

To get notifications when the `IDownload` is finished, use the `Finished` event:


**C#**
```csharp
download.Finished += (s, e) => { };
```

**VB**
```vb
AddHandler download.Finished, Sub(s, e)
End Sub
```



### Download Paused event

To get notifications when the `IDownload` is paused, use the `Paused` event:


**C#**
```csharp
download.Paused += (s, e) => { };
```

**VB**
```vb
AddHandler download.Paused, Sub(s, e)
End Sub
```



### Download Updated event

To track the download progress, use the `Updated` event:


**C#**
```csharp 
download.Updated += (s, e) =>
{
    // Get download progress in percents.
    float progress = e.Progress;
    // The current download speed estimate in bytes/second.
    long currentSpeed = e.CurrentSpeed;
    // The total size of a file in bytes.
    long totalBytes = e.TotalBytes;
    // The number or received (downloaded) bytes.
    long receivedBytes = e.ReceivedBytes;
};
```

**VB**
```vb
AddHandler download.Updated, Sub(s, e)
    ' Get download progress in percents.
    Dim progress As Single = e.Progress
    ' The current download speed estimate in bytes/second.
    Dim currentSpeed As Long = e.CurrentSpeed
    ' The total size of a file in bytes.
    Dim totalBytes As Long = e.TotalBytes
    ' The number or received (downloaded) bytes.
    Dim receivedBytes As Long = e.ReceivedBytes
End Sub
```



### Download Interrupted event

To get notifications when the `Download` is interrupted for some reason, use the `Interrupted` event:


**C#**
```csharp
download.Interrupted += (s, e) =>
{
    // The interrupt reason such as file access denied, network failed, etc.
    DownloadInterruptionReason reason = e.InterruptionReason;
};
```

**VB**
```vb
AddHandler download.Interrupted, Sub(s, e)
    ' The interrupt reason such as file access denied, network failed, etc.
    Dim reason As DownloadInterruptionReason = e.InterruptionReason
End Sub
```


