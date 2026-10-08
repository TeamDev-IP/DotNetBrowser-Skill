# <a id="DotNetBrowser_Dom_Events_IWheelEvent"></a> Interface IWheelEvent

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

A wheel event that provides access to the wheel event data.

<p>This event occurs when a user rotates a wheel on a pointing device (such as a mouse).</p>

```csharp
public interface IWheelEvent : IMouseEvent, IUiKeyEventModifier, IEvent, IAutoDisposable
```

#### Implements

[IMouseEvent](DotNetBrowser.Dom.Events.IMouseEvent.md), 
[IUiKeyEventModifier](DotNetBrowser.Dom.Events.IUiKeyEventModifier.md), 
[IEvent](DotNetBrowser.Dom.Events.IEvent.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_Events_IWheelEvent_DeltaMode"></a> DeltaMode

Gets the delta units type.

```csharp
DeltaMode DeltaMode { get; }
```

#### Property Value

 [DeltaMode](DotNetBrowser.Dom.Events.DeltaMode.md)

### <a id="DotNetBrowser_Dom_Events_IWheelEvent_DeltaX"></a> DeltaX

Gets the amount of units to scroll horizontally.

```csharp
double DeltaX { get; }
```

#### Property Value

 [double](https://learn.microsoft.com/dotnet/api/system.double)

### <a id="DotNetBrowser_Dom_Events_IWheelEvent_DeltaY"></a> DeltaY

Gets the amount of units to scroll vertically.

```csharp
double DeltaY { get; }
```

#### Property Value

 [double](https://learn.microsoft.com/dotnet/api/system.double)

