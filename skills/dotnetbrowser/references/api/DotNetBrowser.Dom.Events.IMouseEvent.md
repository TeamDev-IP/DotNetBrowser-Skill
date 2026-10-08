# <a id="DotNetBrowser_Dom_Events_IMouseEvent"></a> Interface IMouseEvent

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

Represents a mouse event and provides an access to specific mouse event data.

<p>
    This event occurs when a user performs an action with a pointing device (such as a mouse), for
    example moves the mouse or clicks a mouse button.
</p>

```csharp
public interface IMouseEvent : IUiKeyEventModifier, IEvent, IAutoDisposable
```

#### Implements

[IUiKeyEventModifier](DotNetBrowser.Dom.Events.IUiKeyEventModifier.md), 
[IEvent](DotNetBrowser.Dom.Events.IEvent.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_Events_IMouseEvent_Button"></a> Button

Gets the button which was pressed on the mouse to trigger the event.

```csharp
DomMouseButton Button { get; }
```

#### Property Value

 [DomMouseButton](DotNetBrowser.Dom.Events.DomMouseButton.md)

### <a id="DotNetBrowser_Dom_Events_IMouseEvent_ClickCount"></a> ClickCount

Gets the click count.

```csharp
uint ClickCount { get; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

### <a id="DotNetBrowser_Dom_Events_IMouseEvent_ClientLocation"></a> ClientLocation

Gets the location of the mouse cursor in the local (DOM content) coordinate system at the time the
event occurred.

```csharp
Point ClientLocation { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Dom_Events_IMouseEvent_OffsetLocation"></a> OffsetLocation

Gets the location of the mouse cursor in the component's coordinate system at the time the
event occurred.

```csharp
Point OffsetLocation { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

#### Remarks

<p>
    For example, clicking in the top-left corner of the client area will always result in that
    the <code>X</code> field of the result equals 0, regardless of whether the page is scrolled
    horizontally.
</p>
<p> This API is available since DotNetBrowser 2.1.</p>

### <a id="DotNetBrowser_Dom_Events_IMouseEvent_ScreenLocation"></a> ScreenLocation

Gets the location of the mouse cursor in the screen's coordinate system at the time the
event occurred.

```csharp
Point ScreenLocation { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

