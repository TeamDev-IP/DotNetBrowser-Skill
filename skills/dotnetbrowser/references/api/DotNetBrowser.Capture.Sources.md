# <a id="DotNetBrowser_Capture_Sources"></a> Class Sources

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

Provides the access to the sources available for content capture.

```csharp
public sealed class Sources
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Sources](DotNetBrowser.Capture.Sources.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Capture_Sources_ApplicationWindows"></a> ApplicationWindows

Gets all of the available application windows for capture.

```csharp
public IReadOnlyList<Source> ApplicationWindows { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Source](DotNetBrowser.Capture.Source.md)\>

### <a id="DotNetBrowser_Capture_Sources_Browsers"></a> Browsers

Gets all of the available browsers for capture.

```csharp
public IReadOnlyList<Source> Browsers { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Source](DotNetBrowser.Capture.Source.md)\>

### <a id="DotNetBrowser_Capture_Sources_Screens"></a> Screens

Gets all of the available screens for capture.

```csharp
public IReadOnlyList<Source> Screens { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Source](DotNetBrowser.Capture.Source.md)\>

