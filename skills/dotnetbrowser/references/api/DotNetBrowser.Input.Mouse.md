# <a id="DotNetBrowser_Input_Mouse"></a> Namespace DotNetBrowser.Input.Mouse

### Namespaces

 [DotNetBrowser.Input.Mouse.Events](DotNetBrowser.Input.Mouse.Events.md)

### Classes

 [MouseExtensions](DotNetBrowser.Input.Mouse.md#DotNetBrowser_Input_Mouse_MouseExtensions)

The mouse input simulation service extension methods.

### Interfaces

 [IMouse](DotNetBrowser.Input.Mouse.md#DotNetBrowser_Input_Mouse_IMouse)

A service that can be used for mouse input simulation and handling.

## <a id="DotNetBrowser_Input_Mouse_MouseExtensions"></a> Class MouseExtensions

Namespace: [DotNetBrowser.Input.Mouse](DotNetBrowser.Input.Mouse.md)  
Assembly: DotNetBrowser.Core.dll  

The mouse input simulation service extension methods.

```csharp
public static class MouseExtensions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseExtensions](DotNetBrowser.Input.Mouse.md#DotNetBrowser_Input_Mouse_MouseExtensions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Input_Mouse_MouseExtensions_SimulateClick_DotNetBrowser_Input_Mouse_IMouse_DotNetBrowser_Input_Mouse_Events_MouseButton_DotNetBrowser_Geometry_Point_"></a> SimulateClick\(IMouse, MouseButton, Point\)

Simulate mouse button click at the specified location.

```csharp
public static void SimulateClick(this IMouse mouse, MouseButton mouseButton, Point location)
```

##### Parameters

`mouse` [IMouse](DotNetBrowser.Input.Mouse.md#DotNetBrowser_Input_Mouse_IMouse)

The mouse input simulation service.

`mouseButton` [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

The mouse button that should be used for clicking.

`location` [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

The mouse pointer location relative to the top left corner of the browser.

##### Remarks

The mouse click is simulated by raising <xref href="DotNetBrowser.Input.Mouse.IMouse.Moved" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Input.Mouse.IMouse.Pressed" data-throw-if-not-resolved="false"></xref>, and
<xref href="DotNetBrowser.Input.Mouse.IMouse.Released" data-throw-if-not-resolved="false"></xref> events in a sequence.

#### <a id="DotNetBrowser_Input_Mouse_MouseExtensions_SimulateClick_DotNetBrowser_Input_Mouse_IMouse_DotNetBrowser_Input_Mouse_Events_MouseButton_DotNetBrowser_Dom_IElement_"></a> SimulateClick\(IMouse, MouseButton, IElement\)

Simulate mouse button click at the specified element.

```csharp
public static void SimulateClick(this IMouse mouse, MouseButton mouseButton, IElement element)
```

##### Parameters

`mouse` [IMouse](DotNetBrowser.Input.Mouse.md#DotNetBrowser_Input_Mouse_IMouse)

The mouse input simulation service.

`mouseButton` [MouseButton](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseButton)

The mouse button that should be used for clicking.

`element` [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

The element to click at.

##### Remarks

<p>
    The mouse click is simulated by raising <xref href="DotNetBrowser.Input.Mouse.IMouse.Moved" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Input.Mouse.IMouse.Pressed" data-throw-if-not-resolved="false"></xref>, and
    <xref href="DotNetBrowser.Input.Mouse.IMouse.Released" data-throw-if-not-resolved="false"></xref> events in a sequence.
</p>
<p> The point to click at is determined as the center of the bounding client rectangle of the specified element.</p>

## <a id="DotNetBrowser_Input_Mouse_IMouse"></a> Interface IMouse

Namespace: [DotNetBrowser.Input.Mouse](DotNetBrowser.Input.Mouse.md)  
Assembly: DotNetBrowser.dll  

A service that can be used for mouse input simulation and handling.

```csharp
public interface IMouse : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Extension Methods

[MouseExtensions.SimulateClick\(IMouse, MouseButton, Point\)](DotNetBrowser.Input.Mouse.md#DotNetBrowser_Input_Mouse_MouseExtensions_SimulateClick_DotNetBrowser_Input_Mouse_IMouse_DotNetBrowser_Input_Mouse_Events_MouseButton_DotNetBrowser_Geometry_Point_), 
[MouseExtensions.SimulateClick\(IMouse, MouseButton, IElement\)](DotNetBrowser.Input.Mouse.md#DotNetBrowser_Input_Mouse_MouseExtensions_SimulateClick_DotNetBrowser_Input_Mouse_IMouse_DotNetBrowser_Input_Mouse_Events_MouseButton_DotNetBrowser_Dom_IElement_)

### Properties

#### <a id="DotNetBrowser_Input_Mouse_IMouse_Dragged"></a> Dragged

Gets the mouse dragged event for the browser.

```csharp
IInputEvent<IMouseDraggedEventArgs, MouseDraggedEventArgs> Dragged { get; }
```

##### Property Value

 [IInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInputEvent_2)<[IMouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseDraggedEventArgs), [MouseDraggedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseDraggedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Input_Mouse_IMouse_Entered"></a> Entered

Occurs when the mouse has entered the web page.

```csharp
IInterceptableInputEvent<IMouseEnteredEventArgs, MouseEnteredEventArgs> Entered { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[IMouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseEnteredEventArgs), [MouseEnteredEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseEnteredEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Input_Mouse_IMouse_Exited"></a> Exited

Occurs when the mouse has exited the web page.

```csharp
IInterceptableInputEvent<IMouseExitedEventArgs, MouseExitedEventArgs> Exited { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[IMouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseExitedEventArgs), [MouseExitedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseExitedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Input_Mouse_IMouse_Moved"></a> Moved

Occurs when the mouse has moved over the web page.

```csharp
IInterceptableInputEvent<IMouseMovedEventArgs, MouseMovedEventArgs> Moved { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[IMouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseMovedEventArgs), [MouseMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseMovedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Input_Mouse_IMouse_Pressed"></a> Pressed

Occurs when the mouse button has been pressed on the web page.

```csharp
IInterceptableInputEvent<IMousePressedEventArgs, MousePressedEventArgs> Pressed { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[IMousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMousePressedEventArgs), [MousePressedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MousePressedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Input_Mouse_IMouse_Released"></a> Released

Occurs when the mouse button has been released on the web page.

```csharp
IInterceptableInputEvent<IMouseReleasedEventArgs, MouseReleasedEventArgs> Released { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[IMouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseReleasedEventArgs), [MouseReleasedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseReleasedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Input_Mouse_IMouse_WheelMoved"></a> WheelMoved

Occurs when the mouse wheel has scrolled on the web page.

```csharp
IInterceptableInputEvent<IMouseWheelMovedEventArgs, MouseWheelMovedEventArgs> WheelMoved { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[IMouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_IMouseWheelMovedEventArgs), [MouseWheelMovedEventArgs](DotNetBrowser.Input.Mouse.Events.md#DotNetBrowser_Input_Mouse_Events_MouseWheelMovedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.
