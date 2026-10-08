# <a id="DotNetBrowser_Dom_Events_EventParameters"></a> Class EventParameters

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

The parameters of creating the DOM event.

```csharp
public class EventParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventParameters](DotNetBrowser.Dom.Events.EventParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Dom_Events_EventParameters_Bubbles"></a> Bubbles

Indicates whether the dispatched event is a bubbling event.

```csharp
public bool Bubbles { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Dom_Events_EventParameters_Cancelable"></a> Cancelable

Indicates whether the dispatched event can have its default action
prevented.

```csharp
public bool Cancelable { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

