# <a id="DotNetBrowser_Dom_Events_ITouchEvent"></a> Interface ITouchEvent

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

Represents a touch event and provides an access to specific touch event data.

<p>
    This event occurs when a user performs an action with a touch device (such as a touchscreen).
</p>

```csharp
public interface ITouchEvent : IUiKeyEventModifier, IEvent, IAutoDisposable
```

#### Implements

[IUiKeyEventModifier](DotNetBrowser.Dom.Events.IUiKeyEventModifier.md), 
[IEvent](DotNetBrowser.Dom.Events.IEvent.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_Events_ITouchEvent_ChangedTouchPoints"></a> ChangedTouchPoints

Gets the list of touch points that have changed since the last touch event.

```csharp
IReadOnlyList<ITouchPoint> ChangedTouchPoints { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ITouchPoint](DotNetBrowser.Input.Touch.Events.ITouchPoint.md)\>

### <a id="DotNetBrowser_Dom_Events_ITouchEvent_TargetTouchPoints"></a> TargetTouchPoints

Gets the list of touch points that are specific to the target element.

```csharp
IReadOnlyList<ITouchPoint> TargetTouchPoints { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ITouchPoint](DotNetBrowser.Input.Touch.Events.ITouchPoint.md)\>

### <a id="DotNetBrowser_Dom_Events_ITouchEvent_TouchPoints"></a> TouchPoints

Gets the list of touch points that are currently on the screen.

```csharp
IReadOnlyList<ITouchPoint> TouchPoints { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ITouchPoint](DotNetBrowser.Input.Touch.Events.ITouchPoint.md)\>

