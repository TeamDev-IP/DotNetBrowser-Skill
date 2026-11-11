# <a id="DotNetBrowser_Input_DragAndDrop"></a> Namespace DotNetBrowser.Input.DragAndDrop

### Namespaces

 [DotNetBrowser.Input.DragAndDrop.Handlers](DotNetBrowser.Input.DragAndDrop.Handlers.md)

### Interfaces

 [IDragAndDrop](DotNetBrowser.Input.DragAndDrop.md#DotNetBrowser_Input_DragAndDrop_IDragAndDrop)

The drag and drop functionality of the browser.

## <a id="DotNetBrowser_Input_DragAndDrop_IDragAndDrop"></a> Interface IDragAndDrop

Namespace: [DotNetBrowser.Input.DragAndDrop](DotNetBrowser.Input.DragAndDrop.md)  
Assembly: DotNetBrowser.dll  

The drag and drop functionality of the browser.

```csharp
public interface IDragAndDrop : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Input_DragAndDrop_IDragAndDrop_DropHandler"></a> DropHandler

Gets or sets a handler that is used when the input system reports an underlying drop event with the browser as the
drag target.

```csharp
IHandler<DropParameters> DropHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)<[DropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DropParameters)\>

##### Remarks

<p>
    <b>Important:</b> the engine will be blocked until the <code>Handle()</code> method returns.
    It is not allowed to invoke any engine methods in the scope of this handler implementation.
</p>
<p>
    The parameters are valid only in the scope of the <code>Handle()</code> method and become invalid when this
    method returns.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Input_DragAndDrop_IDragAndDrop_Enabled"></a> Enabled

Enables or disables the drag and drop functionality in the browser.

```csharp
bool Enabled { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Input_DragAndDrop_IDragAndDrop_EnterDragHandler"></a> EnterDragHandler

Gets or sets a handler that is used when the input system reports an underlying drag enter event with the browser
as the drag target.

```csharp
IHandler<EnterDragParameters> EnterDragHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)<[EnterDragParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_EnterDragParameters)\>

##### Remarks

<p>
    <b>Important:</b> the engine will be blocked until the <code>Handle()</code> method returns.
    It is not allowed to invoke any engine methods in the scope of this handler implementation.
</p>
<p>
    The parameters are valid only in the scope of the <code>Handle()</code> method and become invalid when this
    method returns.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.
