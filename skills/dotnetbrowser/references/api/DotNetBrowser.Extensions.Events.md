# <a id="DotNetBrowser_Extensions_Events"></a> Namespace DotNetBrowser.Extensions.Events

### Classes

 [ExtensionActionUpdatedEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionActionUpdatedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensionAction.Updated" data-throw-if-not-resolved="false"></xref> event.

 [ExtensionEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionEventArgs)

The base class for the extension-related event arguments.

 [ExtensionInstalledEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionInstalledEventArgs)

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensions.ExtensionInstalled" data-throw-if-not-resolved="false"></xref> event.

 [ExtensionUninstalledEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionUninstalledEventArgs)

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensions.ExtensionUninstalled" data-throw-if-not-resolved="false"></xref> event.

 [ExtensionUpdatedEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionUpdatedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensions.ExtensionUpdated" data-throw-if-not-resolved="false"></xref> event.

## <a id="DotNetBrowser_Extensions_Events_ExtensionActionUpdatedEventArgs"></a> Class ExtensionActionUpdatedEventArgs

Namespace: [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensionAction.Updated" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ExtensionActionUpdatedEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ExtensionActionUpdatedEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionActionUpdatedEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Extensions_Events_ExtensionActionUpdatedEventArgs_Browser"></a> Browser

Gets the browser for which the extension action has been updated.

```csharp
public IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Extensions_Events_ExtensionActionUpdatedEventArgs_ExtensionAction"></a> ExtensionAction

Gets the extension action which is the source of this event.

```csharp
public IExtensionAction ExtensionAction { get; }
```

##### Property Value

 [IExtensionAction](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtensionAction)

## <a id="DotNetBrowser_Extensions_Events_ExtensionEventArgs"></a> Class ExtensionEventArgs

Namespace: [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)  
Assembly: DotNetBrowser.dll  

The base class for the extension-related event arguments.

```csharp
public class ExtensionEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ExtensionEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionEventArgs)

##### Derived

[ExtensionInstalledEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionInstalledEventArgs), 
[ExtensionUpdatedEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionUpdatedEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Extensions_Events_ExtensionEventArgs_Extension"></a> Extension

Gets the extension for which the event occurred.

```csharp
public IExtension Extension { get; }
```

##### Property Value

 [IExtension](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtension)

## <a id="DotNetBrowser_Extensions_Events_ExtensionInstalledEventArgs"></a> Class ExtensionInstalledEventArgs

Namespace: [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensions.ExtensionInstalled" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ExtensionInstalledEventArgs : ExtensionEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ExtensionEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionEventArgs) ← 
[ExtensionInstalledEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionInstalledEventArgs)

##### Inherited Members

[ExtensionEventArgs.Extension](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionEventArgs_Extension), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Extensions_Events_ExtensionUninstalledEventArgs"></a> Class ExtensionUninstalledEventArgs

Namespace: [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensions.ExtensionUninstalled" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ExtensionUninstalledEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ExtensionUninstalledEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionUninstalledEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Extensions_Events_ExtensionUninstalledEventArgs_ExtensionId"></a> ExtensionId

Gets the identifier of the uninstalled extension.

```csharp
public string ExtensionId { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Extensions_Events_ExtensionUpdatedEventArgs"></a> Class ExtensionUpdatedEventArgs

Namespace: [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensions.ExtensionUpdated" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ExtensionUpdatedEventArgs : ExtensionEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ExtensionEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionEventArgs) ← 
[ExtensionUpdatedEventArgs](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionUpdatedEventArgs)

##### Inherited Members

[ExtensionEventArgs.Extension](DotNetBrowser.Extensions.Events.md#DotNetBrowser_Extensions_Events_ExtensionEventArgs_Extension), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)
