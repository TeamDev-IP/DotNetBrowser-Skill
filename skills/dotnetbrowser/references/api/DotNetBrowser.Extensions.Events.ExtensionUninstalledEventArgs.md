# <a id="DotNetBrowser_Extensions_Events_ExtensionUninstalledEventArgs"></a> Class ExtensionUninstalledEventArgs

Namespace: [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensions.ExtensionUninstalled" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ExtensionUninstalledEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ExtensionUninstalledEventArgs](DotNetBrowser.Extensions.Events.ExtensionUninstalledEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Extensions_Events_ExtensionUninstalledEventArgs_ExtensionId"></a> ExtensionId

Gets the identifier of the uninstalled extension.

```csharp
public string ExtensionId { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

