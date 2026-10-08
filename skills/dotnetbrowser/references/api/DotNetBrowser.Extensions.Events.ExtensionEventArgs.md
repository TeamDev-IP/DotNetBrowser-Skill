# <a id="DotNetBrowser_Extensions_Events_ExtensionEventArgs"></a> Class ExtensionEventArgs

Namespace: [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for the extension-related event arguments.

```csharp
public class ExtensionEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ExtensionEventArgs](DotNetBrowser.Extensions.Events.ExtensionEventArgs.md)

#### Derived

[ExtensionInstalledEventArgs](DotNetBrowser.Extensions.Events.ExtensionInstalledEventArgs.md), 
[ExtensionUpdatedEventArgs](DotNetBrowser.Extensions.Events.ExtensionUpdatedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Extensions_Events_ExtensionEventArgs_Extension"></a> Extension

Gets the extension for which the event occurred.

```csharp
public IExtension Extension { get; }
```

#### Property Value

 [IExtension](DotNetBrowser.Extensions.IExtension.md)

