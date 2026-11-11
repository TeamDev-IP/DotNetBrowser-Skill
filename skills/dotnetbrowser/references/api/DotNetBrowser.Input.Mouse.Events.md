# <a id="DotNetBrowser_Input_Mouse_Events"></a> Namespace DotNetBrowser.Input.Mouse.Events

### Classes

 [MouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs)

Event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> events associated with a mouse button.

 [MouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseDraggedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Dragged" data-throw-if-not-resolved="false"></xref> event.

 [MouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEnteredEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Entered" data-throw-if-not-resolved="false"></xref> event.

 [MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs)

 [MouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Exited" data-throw-if-not-resolved="false"></xref> event.

 [MouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseModifiers)

 [MouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseMovedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Moved" data-throw-if-not-resolved="false"></xref> event.

 [MousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MousePressedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Pressed" data-throw-if-not-resolved="false"></xref> event.

 [MouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseReleasedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Released" data-throw-if-not-resolved="false"></xref> event.

 [MouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.WheelMoved" data-throw-if-not-resolved="false"></xref> event.

### Interfaces

 [IMouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs)

Event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> events associated with a mouse button.

 [IMouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseDraggedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Dragged" data-throw-if-not-resolved="false"></xref> event.

 [IMouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Entered" data-throw-if-not-resolved="false"></xref> event.

 [IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

The base interface for all <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> event arguments.

 [IMouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Exited" data-throw-if-not-resolved="false"></xref> event.

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

The mouse modifiers indicating which mouse buttons are currently pressed.

 [IMouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Moved" data-throw-if-not-resolved="false"></xref> event.

 [IMousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMousePressedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Pressed" data-throw-if-not-resolved="false"></xref> event.

 [IMouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseReleasedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Released" data-throw-if-not-resolved="false"></xref> event.

 [IMouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs)

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.WheelMoved" data-throw-if-not-resolved="false"></xref> event.

### Enums

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

The mouse buttons.

 [MouseScrollType](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseScrollType)

Scroll type.

## <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs"></a> Class MouseButtonEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> events associated with a mouse button.

```csharp
public class MouseButtonEventArgs : MouseEventArgs, IMouseButtonEventArgs, IMouseEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs) ← 
[MouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs)

##### Derived

[MousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MousePressedEventArgs), 
[MouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseReleasedEventArgs)

##### Implements

[IMouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

##### Inherited Members

[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode), 
[MouseEventArgs.Equals\(MouseEventArgs\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_DotNetBrowser_Input_Mouse_Events_MouseEventArgs_), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_Button"></a> Button

Gets or sets the mouse button this event is related to.

```csharp
public MouseButton Button { get; set; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_ClickCount"></a> ClickCount

Gets or sets the count of consecutive clicks that happened in a short amount of time.

```csharp
public uint ClickCount { get; set; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_KeyModifiers"></a> KeyModifiers

Gets or sets the keyboard modifiers.

```csharp
public IKeyModifiers KeyModifiers { get; set; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_MouseModifiers"></a> MouseModifiers

Gets or sets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
public IMouseModifiers MouseModifiers { get; set; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_MouseDraggedEventArgs"></a> Class MouseDraggedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Dragged" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MouseDraggedEventArgs : MouseEventArgs, IMouseDraggedEventArgs, IMouseEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs) ← 
[MouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseDraggedEventArgs)

##### Implements

[IMouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseDraggedEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

##### Inherited Members

[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseDraggedEventArgs_Button"></a> Button

Gets or sets the button that is pressed during the move.

```csharp
public MouseButton Button { get; set; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseDraggedEventArgs_Modifiers"></a> Modifiers

Gets or sets the keyboard modifiers.

```csharp
public IKeyModifiers Modifiers { get; set; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseDraggedEventArgs_MouseModifiers"></a> MouseModifiers

Gets or sets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
public IMouseModifiers MouseModifiers { get; set; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_MouseEnteredEventArgs"></a> Class MouseEnteredEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Entered" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MouseEnteredEventArgs : MouseEventArgs, IMouseEnteredEventArgs, IMouseEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs) ← 
[MouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEnteredEventArgs)

##### Implements

[IMouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

##### Inherited Members

[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseEnteredEventArgs_Button"></a> Button

Gets or sets the mouse button that is pressed when entering the browser.

```csharp
public MouseButton Button { get; set; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseEnteredEventArgs_KeyModifiers"></a> KeyModifiers

Gets or sets the keyboard modifiers.

```csharp
public IKeyModifiers KeyModifiers { get; set; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseEnteredEventArgs_MouseModifiers"></a> MouseModifiers

Gets or sets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
public IMouseModifiers MouseModifiers { get; set; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs"></a> Class MouseEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public abstract class MouseEventArgs : IMouseEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs)

##### Derived

[MouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs), 
[MouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseDraggedEventArgs), 
[MouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEnteredEventArgs), 
[MouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs), 
[MouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseMovedEventArgs), 
[MouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs)

##### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location"></a> Location

Gets or sets the mouse position relative to the bounds of the browser instance.

```csharp
public Point Location { get; set; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen"></a> LocationOnScreen

Gets or sets the mouse position relative to the bounds of the screen.

```csharp
public Point LocationOnScreen { get; set; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

### Methods

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_DotNetBrowser_Input_Mouse_Events_MouseEventArgs_"></a> Equals\(MouseEventArgs\)

Determines whether the specified object is equal to the current object.

```csharp
protected bool Equals(MouseEventArgs other)
```

##### Parameters

`other` [MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs)

The object to compare with the current object.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if the specified object  is equal to the current object; otherwise,
<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs"></a> Class MouseExitedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Exited" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MouseExitedEventArgs : MouseEventArgs, IMouseExitedEventArgs, IMouseEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs) ← 
[MouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs)

##### Implements

[IMouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

##### Inherited Members

[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs_Button"></a> Button

Gets or sets the mouse button that is pressed when exiting the browser.

```csharp
public MouseButton Button { get; set; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs_KeyModifiers"></a> KeyModifiers

Gets or sets the keyboard modifiers.

```csharp
public IKeyModifiers KeyModifiers { get; set; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs_MouseModifiers"></a> MouseModifiers

Gets or sets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
public IMouseModifiers MouseModifiers { get; set; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_MouseModifiers"></a> Class MouseModifiers

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class MouseModifiers : IMouseModifiers
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseModifiers)

##### Implements

[IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseModifiers_BackButtonDown"></a> BackButtonDown

Indicates whether the first extended ("Back") mouse button is pressed.

```csharp
public bool BackButtonDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseModifiers_ForwardButtonDown"></a> ForwardButtonDown

Indicates whether the second extended ("Forward") mouse button is pressed.

```csharp
public bool ForwardButtonDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseModifiers_MiddleButtonDown"></a> MiddleButtonDown

Indicates whether the middle mouse button is pressed.

```csharp
public bool MiddleButtonDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseModifiers_PrimaryButtonDown"></a> PrimaryButtonDown

Indicates whether the primary mouse button is pressed.

```csharp
public bool PrimaryButtonDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseModifiers_SecondaryButtonDown"></a> SecondaryButtonDown

Indicates whether the secondary mouse button is pressed.

```csharp
public bool SecondaryButtonDown { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### Methods

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseModifiers_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseModifiers_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Input_Mouse_Events_MouseMovedEventArgs"></a> Class MouseMovedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Moved" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MouseMovedEventArgs : MouseEventArgs, IMouseMovedEventArgs, IMouseEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs) ← 
[MouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseMovedEventArgs)

##### Implements

[IMouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

##### Inherited Members

[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseMovedEventArgs_Button"></a> Button

Gets or sets the mouse button that is pressed during the move.

```csharp
public MouseButton Button { get; set; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseMovedEventArgs_KeyModifiers"></a> KeyModifiers

Gets or sets the keyboard modifiers.

```csharp
public IKeyModifiers KeyModifiers { get; set; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseMovedEventArgs_MouseModifiers"></a> MouseModifiers

Gets or sets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
public IMouseModifiers MouseModifiers { get; set; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_MousePressedEventArgs"></a> Class MousePressedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Pressed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MousePressedEventArgs : MouseButtonEventArgs, IMousePressedEventArgs, IMouseButtonEventArgs, IMouseEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs) ← 
[MouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs) ← 
[MousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MousePressedEventArgs)

##### Implements

[IMousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMousePressedEventArgs), 
[IMouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

##### Inherited Members

[MouseButtonEventArgs.Button](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_Button), 
[MouseButtonEventArgs.ClickCount](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_ClickCount), 
[MouseButtonEventArgs.KeyModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_KeyModifiers), 
[MouseButtonEventArgs.MouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_MouseModifiers), 
[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Input_Mouse_Events_MouseReleasedEventArgs"></a> Class MouseReleasedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Released" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MouseReleasedEventArgs : MouseButtonEventArgs, IMouseReleasedEventArgs, IMouseButtonEventArgs, IMouseEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs) ← 
[MouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs) ← 
[MouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseReleasedEventArgs)

##### Implements

[IMouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseReleasedEventArgs), 
[IMouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

##### Inherited Members

[MouseButtonEventArgs.Button](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_Button), 
[MouseButtonEventArgs.ClickCount](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_ClickCount), 
[MouseButtonEventArgs.KeyModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_KeyModifiers), 
[MouseButtonEventArgs.MouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButtonEventArgs_MouseModifiers), 
[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs"></a> Class MouseWheelMovedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.WheelMoved" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MouseWheelMovedEventArgs : MouseEventArgs, IMouseWheelMovedEventArgs, IMouseEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs) ← 
[MouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs)

##### Implements

[IMouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

##### Inherited Members

[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_DeltaX"></a> DeltaX

The amount of units to scroll horizontally.

```csharp
public float DeltaX { get; set; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_DeltaY"></a> DeltaY

The amount of units to scroll vertically.

```csharp
public float DeltaY { get; set; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_Modifiers"></a> Modifiers

The keyboard modifiers applied.

```csharp
public IKeyModifiers Modifiers { get; set; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_ScrollType"></a> ScrollType

The scroll type of the event.

```csharp
public MouseScrollType ScrollType { get; set; }
```

##### Property Value

 [MouseScrollType](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseScrollType)

### Methods

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs"></a> Interface IMouseButtonEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> events associated with a mouse button.

```csharp
public interface IMouseButtonEventArgs : IMouseEventArgs
```

##### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs_Button"></a> Button

Gets the mouse button this event is related to.

```csharp
MouseButton Button { get; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs_ClickCount"></a> ClickCount

Gets the count of consecutive clicks that happened in a short amount of time.

```csharp
uint ClickCount { get; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs_MouseModifiers"></a> MouseModifiers

Gets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
IMouseModifiers MouseModifiers { get; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_IMouseDraggedEventArgs"></a> Interface IMouseDraggedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Dragged" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseDraggedEventArgs : IMouseEventArgs
```

##### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseDraggedEventArgs_Button"></a> Button

Gets the button that is pressed during the move.

```csharp
MouseButton Button { get; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseDraggedEventArgs_Modifiers"></a> Modifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers Modifiers { get; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseDraggedEventArgs_MouseModifiers"></a> MouseModifiers

Gets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
IMouseModifiers MouseModifiers { get; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs"></a> Interface IMouseEnteredEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Entered" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseEnteredEventArgs : IMouseEventArgs
```

##### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs_Button"></a> Button

Gets the mouse button that is pressed when entering the browser.

```csharp
MouseButton Button { get; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs_MouseModifiers"></a> MouseModifiers

Gets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
IMouseModifiers MouseModifiers { get; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_IMouseEventArgs"></a> Interface IMouseEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The base interface for all <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> event arguments.

```csharp
public interface IMouseEventArgs
```

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEventArgs_Location"></a> Location

Gets the mouse position relative to the bounds of the browser instance.

```csharp
Point Location { get; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseEventArgs_LocationOnScreen"></a> LocationOnScreen

Gets the mouse position relative to the bounds of the screen.

```csharp
Point LocationOnScreen { get; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

## <a id="DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs"></a> Interface IMouseExitedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Exited" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseExitedEventArgs : IMouseEventArgs
```

##### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs_Button"></a> Button

Gets the mouse button that is pressed when exiting the browser.

```csharp
MouseButton Button { get; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs_MouseModifiers"></a> MouseModifiers

Gets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
IMouseModifiers MouseModifiers { get; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_IMouseModifiers"></a> Interface IMouseModifiers

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
public interface IMouseModifiers
```

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseModifiers_BackButtonDown"></a> BackButtonDown

Indicates whether the first extended ("Back") mouse button is pressed.

```csharp
bool BackButtonDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseModifiers_ForwardButtonDown"></a> ForwardButtonDown

Indicates whether the second extended ("Forward") mouse button is pressed.

```csharp
bool ForwardButtonDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseModifiers_MiddleButtonDown"></a> MiddleButtonDown

Indicates whether the middle mouse button is pressed.

```csharp
bool MiddleButtonDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseModifiers_PrimaryButtonDown"></a> PrimaryButtonDown

Indicates whether the primary mouse button is pressed.

```csharp
bool PrimaryButtonDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseModifiers_SecondaryButtonDown"></a> SecondaryButtonDown

Indicates whether the secondary mouse button is pressed.

```csharp
bool SecondaryButtonDown { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## <a id="DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs"></a> Interface IMouseMovedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Moved" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseMovedEventArgs : IMouseEventArgs
```

##### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs_Button"></a> Button

Gets the mouse button that is pressed during the move.

```csharp
MouseButton Button { get; }
```

##### Property Value

 [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs_MouseModifiers"></a> MouseModifiers

Gets the mouse modifiers indicating which mouse buttons are currently pressed.

```csharp
IMouseModifiers MouseModifiers { get; }
```

##### Property Value

 [IMouseModifiers](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseModifiers)

## <a id="DotNetBrowser_Input_Mouse_Events_IMousePressedEventArgs"></a> Interface IMousePressedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Pressed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMousePressedEventArgs : IMouseButtonEventArgs, IMouseEventArgs
```

##### Implements

[IMouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

## <a id="DotNetBrowser_Input_Mouse_Events_IMouseReleasedEventArgs"></a> Interface IMouseReleasedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.Released" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseReleasedEventArgs : IMouseButtonEventArgs, IMouseEventArgs
```

##### Implements

[IMouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseButtonEventArgs), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

## <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs"></a> Interface IMouseWheelMovedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.WheelMoved" data-throw-if-not-resolved="false"></xref> event.

```csharp
public interface IMouseWheelMovedEventArgs : IMouseEventArgs
```

##### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEventArgs)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs_DeltaX"></a> DeltaX

The amount of units to scroll horizontally.

```csharp
float DeltaX { get; set; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs_DeltaY"></a> DeltaY

The amount of units to scroll vertically.

```csharp
float DeltaY { get; set; }
```

##### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs_Modifiers"></a> Modifiers

The keyboard modifiers applied.

```csharp
IKeyModifiers Modifiers { get; }
```

##### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.md#DotNetBrowser_Input_Keyboard_Events_IKeyModifiers)

#### <a id="DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs_ScrollType"></a> ScrollType

The scroll type of the event.

```csharp
MouseScrollType ScrollType { get; }
```

##### Property Value

 [MouseScrollType](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseScrollType)

## <a id="DotNetBrowser_Input_Mouse_Events_MouseButton"></a> Enum MouseButton

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The mouse buttons.

```csharp
public enum MouseButton
```

### Fields

`Back = 5` 

Back (XButton1) button.



`Eraser = 7` 

Button eraser.



`Forward = 6` 

Forward (XButton2) button.



`Left = 2` 

Left (primary) button.



`Middle = 3` 

Middle button.



`None = 1` 

No button.



`Right = 4` 

Right (secondary) button.

## <a id="DotNetBrowser_Input_Mouse_Events_MouseScrollType"></a> Enum MouseScrollType

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

Scroll type.

```csharp
public enum MouseScrollType
```

### Fields

`BlockScroll = 2` 

Defines the scroll by page (block).



`UnitScroll = 1` 

Defines the scroll by units.
