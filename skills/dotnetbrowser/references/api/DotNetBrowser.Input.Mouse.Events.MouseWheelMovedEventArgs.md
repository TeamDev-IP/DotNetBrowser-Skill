# <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs"></a> Class MouseWheelMovedEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

The event arguments for the <xref href="DotNetBrowser.Input.Mouse.IMouse.WheelMoved" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MouseWheelMovedEventArgs : MouseEventArgs, IMouseWheelMovedEventArgs, IMouseEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md) ← 
[MouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseWheelMovedEventArgs.md)

#### Implements

[IMouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseWheelMovedEventArgs.md), 
[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md)

#### Inherited Members

[MouseEventArgs.Location](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_Location), 
[MouseEventArgs.LocationOnScreen](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_LocationOnScreen), 
[MouseEventArgs.Equals\(object\)](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_Equals\_System\_Object\_), 
[MouseEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md\#DotNetBrowser\_Input\_Mouse\_Events\_MouseEventArgs\_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_DeltaX"></a> DeltaX

The amount of units to scroll horizontally.

```csharp
public float DeltaX { get; set; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_DeltaY"></a> DeltaY

The amount of units to scroll vertically.

```csharp
public float DeltaY { get; set; }
```

#### Property Value

 [float](https://learn.microsoft.com/dotnet/api/system.single)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_Modifiers"></a> Modifiers

The keyboard modifiers applied.

```csharp
public IKeyModifiers Modifiers { get; set; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_ScrollType"></a> ScrollType

The scroll type of the event.

```csharp
public MouseScrollType ScrollType { get; set; }
```

#### Property Value

 [MouseScrollType](DotNetBrowser.Input.Mouse.Events.MouseScrollType.md)

## Methods

### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

