# <a id="DotNetBrowser_Dom_Events_IEvents"></a> Interface IEvents

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

A collection of custom DOM events that can be listened and/or handled.

```csharp
public interface IEvents
```

## Properties

### <a id="DotNetBrowser_Dom_Events_IEvents_Item_DotNetBrowser_Dom_Events_EventType_System_Boolean_"></a> this\[EventType, bool\]

Gets or sets the custom DOM event to listen.

```csharp
Event this[EventType eventType, bool useCapture = false] { get; set; }
```

#### Property Value

 [Event](DotNetBrowser.Dom.Events.Event.md)

### <a id="DotNetBrowser_Dom_Events_IEvents_Abort"></a> Abort

Occurs when the loading of a resource has been aborted.

```csharp
event EventHandler<DomEventArgs> Abort
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Blur"></a> Blur

Occurs when an element loses focus.

```csharp
event EventHandler<DomEventArgs> Blur
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Change"></a> Change

Occurs when the content of a form element, the selection,
or the checked state have changed (for &lt;input&gt;, &lt;select&gt;, and &lt;textarea&gt;).

```csharp
event EventHandler<DomEventArgs> Change
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Click"></a> Click

Occurs when the user clicks on an element.

```csharp
event EventHandler<DomEventArgs> Click
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_DoubleClick"></a> DoubleClick

Occurs when the user double-clicks on an element.

```csharp
event EventHandler<DomEventArgs> DoubleClick
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Error"></a> Error

Occurs when an error occurs while loading an external file.

```csharp
event EventHandler<DomEventArgs> Error
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Focus"></a> Focus

Occurs when an element gets focus.

```csharp
event EventHandler<DomEventArgs> Focus
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_KeyDown"></a> KeyDown

Occurs when the user presses a key.

```csharp
event EventHandler<DomEventArgs> KeyDown
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_KeyPress"></a> KeyPress

Occurs when the user presses a key that produces a character value.

```csharp
event EventHandler<DomEventArgs> KeyPress
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_KeyUp"></a> KeyUp

Occurs when the user releases a key.

```csharp
event EventHandler<DomEventArgs> KeyUp
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Load"></a> Load

Occurs when an object has loaded.

```csharp
event EventHandler<DomEventArgs> Load
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_MouseDown"></a> MouseDown

Occurs when the user presses a mouse button over an element.

```csharp
event EventHandler<DomEventArgs> MouseDown
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_MouseMove"></a> MouseMove

Occurs when the pointer is moving while it is over an element.

```csharp
event EventHandler<DomEventArgs> MouseMove
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_MouseOut"></a> MouseOut

Occurs when a user moves the mouse pointer out of an element, or out of one of its children

```csharp
event EventHandler<DomEventArgs> MouseOut
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_MouseOver"></a> MouseOver

Occurs when the pointer is moved onto an element, or onto one of its children.

```csharp
event EventHandler<DomEventArgs> MouseOver
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_MouseUp"></a> MouseUp

Occurs when a user releases a mouse button over an element.

```csharp
event EventHandler<DomEventArgs> MouseUp
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Reset"></a> Reset

Occurs when a form is reset.

```csharp
event EventHandler<DomEventArgs> Reset
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Resize"></a> Resize

Occurs when the document view is resized.

```csharp
event EventHandler<DomEventArgs> Resize
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Scroll"></a> Scroll

Occurs when an element's scrollbar is being scrolled.

```csharp
event EventHandler<DomEventArgs> Scroll
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Select"></a> Select

Occurs after the user selects some text (for &lt;input&gt; and &lt;textarea&gt;).

```csharp
event EventHandler<DomEventArgs> Select
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Submit"></a> Submit

Occurs when a form is submitted.

```csharp
event EventHandler<DomEventArgs> Submit
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_TouchCancel"></a> TouchCancel

Occurs when one or more touch points have been disrupted in an implementation-specific manner.

```csharp
event EventHandler<DomEventArgs> TouchCancel
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_TouchEnd"></a> TouchEnd

Occurs when one or more touch points are removed from the touch surface.

```csharp
event EventHandler<DomEventArgs> TouchEnd
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_TouchMove"></a> TouchMove

Occurs when one or more touch points are moved along the touch surface.

```csharp
event EventHandler<DomEventArgs> TouchMove
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_TouchStart"></a> TouchStart

Occurs when one or more touch points are placed on the touch surface.

```csharp
event EventHandler<DomEventArgs> TouchStart
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Unload"></a> Unload

Occurs once a page has unloaded (for &lt;body&gt;).

```csharp
event EventHandler<DomEventArgs> Unload
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_Events_IEvents_Wheel"></a> Wheel

Occurs when user scrolls a mouse wheel over an element.

```csharp
event EventHandler<DomEventArgs> Wheel
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[DomEventArgs](DotNetBrowser.Dom.Events.DomEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.Events.IEventTarget" data-throw-if-not-resolved="false"></xref> has already been disposed.

