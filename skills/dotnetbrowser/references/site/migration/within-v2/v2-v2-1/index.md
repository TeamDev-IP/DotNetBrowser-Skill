
# Migrating from 2.0 to 2.1

**Lead**
DotNetBrowser version 2.1 brings some improvements to both internal features and public API of the library. The engine version got updated to Chromium 79. This guide shows how to make your application code written with DotNetBrowser version 2.0 compatible with version 2.1.


### Why migrate?

We recommend you to update your code to the latest version because all the new features, Chromium upgrades, support of new operating systems and .NET Framework versions, bug fixes, security patches, performance, and memory usage enhancements are applied on top of the latest version.

### How long does it take?

From our experience, upgrade to a new version may take from a couple of hours to a few days depending on the number of the features you use in your application. As usual, we strongly recommend to test your software after the upgrade in all the environments it supports.

### Getting help

In case you did not find the answer in this guide and you need assistance with the migration, please [contact us](https://dotnetbrowser.support.teamdev.com/support/tickets/new). We will be happy to help.

## Key changes

### Download Handler

The `StartDownloadHandler` property is moved from `IDownloads` to `IBrowser` interface.

**v2.0**


**C#**
```csharp
engine.Downloads.StartDownloadHandler = 
    new Handler<StartDownloadParameters, StartDownloadResponse>((p) =>
    {
        return StartDownloadResponse.DownloadTo(Path.Combine(Path.GetTempPath(),
            p.Download.Info.SuggestedFileName));
    });
```

**VB**
```vb
engine.Downloads.StartDownloadHandler = 
    New Handler(Of StartDownloadParameters, StartDownloadResponse)(Function(p)
        Return StartDownloadResponse.DownloadTo(Path.Combine(Path.GetTempPath(),
            p.Download.Info.SuggestedFileName))
    End Function)
```



**v2.1**


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



### Dropped functionality

In the new version, the following functionality is no longer supported:

* The `INetwork.TransactionStarted` event. You can use the `INetwork.StartTransactionHandler` instead.
* The `INetwork.BytesReceived` event. You can use the `INetwork.ResponseBytesReceived` event instead.
* The `INetwork.BytesSent` event.
* The `Url` propertty is no longer available in the`CanAccessFileParameters`used by `INetwork.CanAccessFileHandler`.
