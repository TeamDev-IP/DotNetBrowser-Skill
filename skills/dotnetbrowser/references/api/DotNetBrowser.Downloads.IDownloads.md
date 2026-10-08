# <a id="DotNetBrowser_Downloads_IDownloads"></a> Interface IDownloads

Namespace: [DotNetBrowser.Downloads](DotNetBrowser.Downloads.md)  
Assembly: DotNetBrowser.dll  

A service that can be used to work with the downloads.

```csharp
public interface IDownloads
```

## Properties

### <a id="DotNetBrowser_Downloads_IDownloads_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Downloads_IDownloads_Items"></a> Items

Gets an immutable collection of all download items including already completed downloads during this session and
the active
downloads.

```csharp
IEnumerable<IDownload> Items { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IDownload](DotNetBrowser.Downloads.IDownload.md)\>

### <a id="DotNetBrowser_Downloads_IDownloads_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

