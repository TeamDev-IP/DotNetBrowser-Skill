# <a id="DotNetBrowser_Dom_Events_Event"></a> Class Event

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

Represents a DOM event that can be handled on the .NET side.

```csharp
public sealed class Event
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Event](DotNetBrowser.Dom.Events.Event.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Dom_Events_Event_EventType"></a> EventType

Gets the DOM event type.

```csharp
public EventType EventType { get; }
```

#### Property Value

 [EventType](DotNetBrowser.Dom.Events.EventType.md)

### <a id="DotNetBrowser_Dom_Events_Event_UseCapture"></a> UseCapture

Indicates if capturing is used for the DOM event.

```csharp
public bool UseCapture { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

<p>
    If capturing is used, all events of the specified type will be dispatched to the
    registered listeners before being dispatched to any event target beneath them
    in the tree.
</p>
<p>Events which are bubbling upward through the tree will not trigger the listeners in this case.</p>

### <a id="DotNetBrowser_Dom_Events_Event_EventReceived"></a> EventReceived

Occurs when the corresponding DOM event is received.

```csharp
public event EventHandler<DomEventArgs> EventReceived
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Operators

### <a id="DotNetBrowser_Dom_Events_Event_op_Addition_DotNetBrowser_Dom_Events_Event_System_EventHandler_DotNetBrowser_Dom_Events_DomEventArgs__"></a> operator \+\(Event, EventHandler<DomEventArgs\>\)

The overloaded operator that can be used for simplifying registering event handlers for the DOM event.

```csharp
public static Event operator +(Event evt, EventHandler<DomEventArgs> handler)
```

#### Parameters

`evt` [Event](DotNetBrowser.Dom.Events.Event.md)

The custom DOM event.

`handler` [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

the event handler to register for this DOM event.

#### Returns

 [Event](DotNetBrowser.Dom.Events.Event.md)

The updated <xref href="DotNetBrowser.Dom.Events.Event" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_Event_op_Subtraction_DotNetBrowser_Dom_Events_Event_System_EventHandler_DotNetBrowser_Dom_Events_DomEventArgs__"></a> operator \-\(Event, EventHandler<DomEventArgs\>\)

The overloaded operator that can be used for simplifying registering event handlers for the DOM event.

```csharp
public static Event operator -(Event node, EventHandler<DomEventArgs> handler)
```

#### Parameters

`node` [Event](DotNetBrowser.Dom.Events.Event.md)

The custom DOM event.

`handler` [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

The event handler to unregister from this DOM event.

#### Returns

 [Event](DotNetBrowser.Dom.Events.Event.md)

The updated <xref href="DotNetBrowser.Dom.Events.Event" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

