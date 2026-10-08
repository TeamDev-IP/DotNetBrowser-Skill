# <a id="DotNetBrowser_Cache_IHttpAuthCache"></a> Interface IHttpAuthCache

Namespace: [DotNetBrowser.Cache](DotNetBrowser.Cache.md)  
Assembly: DotNetBrowser.dll  

An HTTP Authentication cache service.

```csharp
public interface IHttpAuthCache : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Remarks

This service stores HTTP authentication identities and challenge info.

## Properties

### <a id="DotNetBrowser_Cache_IHttpAuthCache_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Cache_IHttpAuthCache_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this object.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

## Methods

### <a id="DotNetBrowser_Cache_IHttpAuthCache_Clear"></a> Clear\(\)

Clears all added HTTP authentication entries.

```csharp
void Clear()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Cache.IHttpCache" data-throw-if-not-resolved="false"></xref> has already been disposed.

