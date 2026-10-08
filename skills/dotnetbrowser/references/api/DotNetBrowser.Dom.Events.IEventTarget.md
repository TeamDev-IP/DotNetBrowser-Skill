# <a id="DotNetBrowser_Dom_Events_IEventTarget"></a> Interface IEventTarget

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

```csharp
public interface IEventTarget : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_Events_IEventTarget_Events"></a> Events

Gets the DOM events that can be listened.

```csharp
IEvents Events { get; }
```

#### Property Value

 [IEvents](DotNetBrowser.Dom.Events.IEvents.md)

## Methods

### <a id="DotNetBrowser_Dom_Events_IEventTarget_DispatchEvent_DotNetBrowser_Dom_Events_IEvent_"></a> DispatchEvent\(IEvent\)

Dispatches (sends) a particular DOM event to the current target.

```csharp
bool DispatchEvent(IEvent evt)
```

#### Parameters

`evt` [IEvent](DotNetBrowser.Dom.Events.IEvent.md)

The DOM event to dispatch

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>false</code> if event is cancelable and at least one of the event handlers
which handled this event called cancelable action; <code>true</code> otherwise.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

