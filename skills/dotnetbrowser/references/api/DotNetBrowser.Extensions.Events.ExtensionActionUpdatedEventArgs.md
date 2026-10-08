# <a id="DotNetBrowser_Extensions_Events_ExtensionActionUpdatedEventArgs"></a> Class ExtensionActionUpdatedEventArgs

Namespace: [DotNetBrowser.Extensions.Events](DotNetBrowser.Extensions.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Extensions.IExtensionAction.Updated" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class ExtensionActionUpdatedEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[ExtensionActionUpdatedEventArgs](DotNetBrowser.Extensions.Events.ExtensionActionUpdatedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Extensions_Events_ExtensionActionUpdatedEventArgs_Browser"></a> Browser

Gets the browser for which the extension action has been updated.

```csharp
public IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Extensions_Events_ExtensionActionUpdatedEventArgs_ExtensionAction"></a> ExtensionAction

Gets the extension action which is the source of this event.

```csharp
public IExtensionAction ExtensionAction { get; }
```

#### Property Value

 [IExtensionAction](DotNetBrowser.Extensions.IExtensionAction.md)

