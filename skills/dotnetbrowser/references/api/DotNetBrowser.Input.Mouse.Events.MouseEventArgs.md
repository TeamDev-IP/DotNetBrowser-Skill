# <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs"></a> Class MouseEventArgs

Namespace: [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public abstract class MouseEventArgs : IMouseEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventArgs](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md)

#### Derived

[MouseButtonEventArgs](DotNetBrowser.Input.Mouse.Events.MouseButtonEventArgs.md), 
[MouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseDraggedEventArgs.md), 
[MouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.MouseEnteredEventArgs.md), 
[MouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseExitedEventArgs.md), 
[MouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseMovedEventArgs.md), 
[MouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.MouseWheelMovedEventArgs.md)

#### Implements

[IMouseEventArgs](DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Location"></a> Location

Gets or sets the mouse position relative to the bounds of the browser instance.

```csharp
public Point Location { get; set; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_LocationOnScreen"></a> LocationOnScreen

Gets or sets the mouse position relative to the bounds of the screen.

```csharp
public Point LocationOnScreen { get; set; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

## Methods

### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_Equals_DotNetBrowser_Input_Mouse_Events_MouseEventArgs_"></a> Equals\(MouseEventArgs\)

Determines whether the specified object is equal to the current object.

```csharp
protected bool Equals(MouseEventArgs other)
```

#### Parameters

`other` [MouseEventArgs](DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md)

The object to compare with the current object.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if the specified object  is equal to the current object; otherwise,
<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

### <a id="DotNetBrowser_Input_Mouse_Events_MouseEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

