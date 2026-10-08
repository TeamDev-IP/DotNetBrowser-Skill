# <a id="DotNetBrowser_Cache_IHttpCache"></a> Interface IHttpCache

Namespace: [DotNetBrowser.Cache](DotNetBrowser.Cache.md)  
Assembly: DotNetBrowser.dll  

An HTTP cache service.

```csharp
public interface IHttpCache : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Remarks

<p>
    By default, HTTP cache stores the resources fetched from the web on a disk or in the
    memory. Chromium itself decides how to cache the resources for optimal performance.
</p>
<p>
    The memory cache stores and loads the resources to and from the process memory (RAM). It is a
    fast, but non-persistent way.
</p>
<p>
    The disk cache is persistent. The cached resources are stored and loaded to and from the
    disk. The disk cache is stored in the HttpCache folder in the User Data directory.
</p>

## Properties

### <a id="DotNetBrowser_Cache_IHttpCache_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Cache_IHttpCache_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

## Methods

### <a id="DotNetBrowser_Cache_IHttpCache_Clear"></a> Clear\(\)

Marks all the cache entries for deletion. The deletion of the entries is performed asynchronously by the
Chromium engine itself. If the engine is closed during this task executing - the operation will be canceled.

```csharp
Task Clear()
```

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

a <xref href="System.Threading.Tasks.Task" data-throw-if-not-resolved="false"></xref> which is completed when the disk cache is cleared.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cache.IHttpCache" data-throw-if-not-resolved="false"></xref> has already been disposed.

