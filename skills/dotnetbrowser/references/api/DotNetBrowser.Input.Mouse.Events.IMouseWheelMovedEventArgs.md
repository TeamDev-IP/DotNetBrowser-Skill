# <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs"></a> Interface IMouseWheelMovedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.WheelMoved" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseWheelMovedEventArgs : IMouseEventArgs
```

#### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md)

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs_DeltaX"></a> DeltaX

The amount of units to scroll horizontally.

```csharp
float DeltaX { get; set; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs_DeltaY"></a> DeltaY

The amount of units to scroll vertically.

```csharp
float DeltaY { get; set; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs_Modifiers"></a> Modifiers

The keyboard modifiers applied.

```csharp
IKeyModifiers Modifiers { get; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs_ScrollType"></a> ScrollType

The scroll type of the event.

```csharp
MouseScrollType ScrollType { get; }
```

#### Property Value

 [MouseScrollType](DotNetBrowser.Input.Mouse.Events.MouseScrollType.md)

