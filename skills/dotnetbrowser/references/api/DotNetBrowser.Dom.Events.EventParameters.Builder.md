# <a id="DotNetBrowser_Dom_Events_EventParameters_Builder"></a> Class EventParameters.Builder

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

The <xref href="DotNetBrowser.Dom.Events.EventParameters" data-throw-if-not-resolved="false"></xref> builder.

```csharp
public class EventParameters.Builder
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventParameters.Builder](DotNetBrowser.Dom.Events.EventParameters.Builder.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Dom_Events_EventParameters_Builder_Bubbles"></a> Bubbles

Gets or sets whether the dispatched event is a bubbling event.

```csharp
public bool Bubbles { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Dom_Events_EventParameters_Builder_Cancelable"></a> Cancelable

Gets or sets whether the dispatched event can have its default action
prevented.

```csharp
public bool Cancelable { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## Methods

### <a id="DotNetBrowser_Dom_Events_EventParameters_Builder_Build"></a> Build\(\)

Builds and returns a read-only <xref href="DotNetBrowser.Dom.Events.EventParameters" data-throw-if-not-resolved="false"></xref> object.

```csharp
public EventParameters Build()
```

#### Returns

 [EventParameters](DotNetBrowser.Dom.Events.EventParameters.md)

a read-only <xref href="DotNetBrowser.Dom.Events.EventParameters" data-throw-if-not-resolved="false"></xref> object.

