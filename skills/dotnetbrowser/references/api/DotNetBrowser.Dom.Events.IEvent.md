# <a id="DotNetBrowser_Dom_Events_IEvent"></a> Interface IEvent

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

Represents DOM <code>Event</code> object and provides access to the event object data.

```csharp
public interface IEvent : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_Events_IEvent_Bubbles"></a> Bubbles

Indicates whether an event is a bubbling event.

```csharp
bool Bubbles { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Dom_Events_IEvent_Cancelable"></a> Cancelable

Indicates whether an event can have its default action
prevented.

```csharp
bool Cancelable { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Dom_Events_IEvent_CurrentTarget"></a> CurrentTarget

Gets the <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> whose event listeners are currently
being processed.

```csharp
IEventTarget CurrentTarget { get; }
```

#### Property Value

 [IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md)

### <a id="DotNetBrowser_Dom_Events_IEvent_EventPhase"></a> EventPhase

Gets the phase of event flow.

```csharp
EventPhase EventPhase { get; }
```

#### Property Value

 [EventPhase](DotNetBrowser.Dom.Events.EventPhase.md)

### <a id="DotNetBrowser_Dom_Events_IEvent_Target"></a> Target

Gets the <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> to which the event was originally dispatched.

```csharp
IEventTarget Target { get; }
```

#### Property Value

 [IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md)

### <a id="DotNetBrowser_Dom_Events_IEvent_Type"></a> Type

Gets the type of this DOM event.

```csharp
EventType Type { get; }
```

#### Property Value

 [EventType](DotNetBrowser.Dom.Events.EventType.md)

## Methods

### <a id="DotNetBrowser_Dom_Events_IEvent_PreventDefault"></a> PreventDefault\(\)

Cancels the event if it is cancelable, without stopping further propagation of the event.

```csharp
void PreventDefault()
```

### <a id="DotNetBrowser_Dom_Events_IEvent_StopPropagation"></a> StopPropagation\(\)

Prevents further propagation of the current event.

```csharp
void StopPropagation()
```

