
# Cache

**Lead**
This guide describes the cache types supported by Chromium and shows how to work with them.


Chromium supports the following cache types:

- HTTP cache
- Blink cache
- HTML5 AppCache

When any resource request is made from a page, it first goes through the Blink loader and the Blink cache. A request to the browser process may or may not be issued from there. As it goes through the browser's network stack, it reaches the HTTP, either disk or memory cache. There is no explicit communication from a page with the cache.

HTML5 AppCache is used explicitly by a web page. It stores data independently from other caches.

## HTTP cache

By default, the HTTP cache stores the resources fetched from the web on a disk or in the memory. Chromium itself decides how to cache the resources for optimal performance.

The memory cache stores and loads the resources to and from the process memory which is RAM. It is a fast but a non-persistent way. The content is available only until you dispose the `IBrowser` instance.

The disk cache is a persistent way as the cached resources are stored and loaded to and from the disk.

On Windows, the disk cache is stored in the `Cache` folder in the [User Data](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#user-data-directory) directory and may look like this:

```
C:\Users\<username>\AppData\Local\Temp\dotnetbrowser-chromium\<version>\<arch>\data\Cache\
```

### Incognito mode

In the [Incognito](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#incognito) mode, Chromium stores the resources only in the memory and does not use the disk for storing resources. The cached resources are only available until you delete the `Profile` or dispose the `IEngine` instance.

### HTTP cache size

The default cache size is calculated at startup. It depends on the available disk space in the volume where the cache is located.

You can configure the HTTP cache size using an appropriate option when constructing the `IEngine` instance. For example, to set a 32MB limit, use the code sample below:


**C#**
```csharp
engine = EngineFactory.Create(new EngineOptions.Builder
{
    DiskCacheSize = 33554432
}
.Build());
```

**VB**
```vb
engine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .DiskCacheSize = 33554432
}.Build())
```



If the disk cache size is set to zero, a default value is calculated and used automatically.

### Clearing HTTP cache

To clear the HTTP cache associated with a specific `Profile` and perform an action after completion, use the code sample below:


**C#**
```csharp
profile.HttpCache.Clear().ContinueWith(t => 
{
    // Cache has been cleared.
});
```

**VB**
```vb
profile.HttpCache.Clear().ContinueWith(Sub(t)
    ' Cache has been cleared.
End Sub)
```



Using the `IEngine.HttpCache()` method you will get the `HttpCache` service for the default profile.

**Note**
Before calling `profile.HttpCache.Clear()` method it is advised to have at least one `IBrowser` instance running. Otherwise, it may lead to the call hang.


### Clearing HTTP authentication cache

To clear HTTP authentication cache associated with a certain profile, use the following code:


**C#**
```csharp
profile.HttpAuthCache.Clear();
```

**VB**
```vb
profile.HttpAuthCache.Clear()
```


