# <a id="DotNetBrowser_Plugins_Plugin"></a> Class Plugin

Namespace: [DotNetBrowser.Plugins](DotNetBrowser.Plugins.md)  
Assembly: DotNetBrowser.dll  

The detailed information about the installed Chromium plugin.

```csharp
public class Plugin
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Plugin](DotNetBrowser.Plugins.Plugin.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Plugins_Plugin_Description"></a> Description

Gets the plugin description.

```csharp
public string Description { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Plugins_Plugin_MimeTypes"></a> MimeTypes

Gets the MIME types supported by this plugin.

```csharp
public IEnumerable<MimeType> MimeTypes { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[MimeType](DotNetBrowser.Net.MimeType.md)\>

### <a id="DotNetBrowser_Plugins_Plugin_Name"></a> Name

Gets the name of the plugin.

```csharp
public string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Plugins_Plugin_Path"></a> Path

Gets the plugin path representation.

```csharp
public string Path { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Plugins_Plugin_PluginType"></a> PluginType

Gets the plugin type.

```csharp
public PluginType PluginType { get; }
```

#### Property Value

 [PluginType](DotNetBrowser.Plugins.PluginType.md)

### <a id="DotNetBrowser_Plugins_Plugin_Version"></a> Version

Gets the version number of the plugin file.

```csharp
public string Version { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

