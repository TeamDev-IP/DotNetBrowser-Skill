# <a id="DotNetBrowser_Extensions_IExtensionAction"></a> Interface IExtensionAction

Namespace: [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)  
Assembly: DotNetBrowser.dll  

The extension action is a clickable extension icon.

<p></p>

In Chrome, extension actions are located in the top-right corner of the toolbar.
Clicking the icon usually results in showing an extension action popup. If the extension
requests to show a popup, the <xref href="DotNetBrowser.Browser.IBrowser.OpenExtensionActionPopupHandler" data-throw-if-not-resolved="false"></xref> is invoked.
The extension can also handle the click action without showing any popups, in which case
the handler is not invoked.

```csharp
public interface IExtensionAction : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Extensions_IExtensionAction_Badge"></a> Badge

Gets the extension action badge text for the given browser.

```csharp
string Badge { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtensionAction_Browser"></a> Browser

Gets the browser instance associated with this extension action.

```csharp
IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Extensions_IExtensionAction_Extension"></a> Extension

Gets the extension associated with this extension action.

```csharp
IExtension Extension { get; }
```

#### Property Value

 [IExtension](DotNetBrowser.Extensions.IExtension.md)

### <a id="DotNetBrowser_Extensions_IExtensionAction_Icon"></a> Icon

Gets the extension action icon for the given browser.

```csharp
Bitmap Icon { get; }
```

#### Property Value

 [Bitmap](DotNetBrowser.Ui.Bitmap.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtensionAction_IsEnabled"></a> IsEnabled

Indicates whether the extension action is currently enabled.

```csharp
bool IsEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtensionAction_Tooltip"></a> Tooltip

Gets the extension action tooltip.

```csharp
string Tooltip { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtensionAction_Type"></a> Type

Gets the extension action type.

```csharp
ExtensionActionType Type { get; }
```

#### Property Value

 [ExtensionActionType](DotNetBrowser.Extensions.ExtensionActionType.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

## Methods

### <a id="DotNetBrowser_Extensions_IExtensionAction_Click"></a> Click\(\)

Simulates a click on the extension action icon for the given browser.

```csharp
void Click()
```

#### Remarks

Clicking a disabled action is no-op.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Extensions.IExtensionAction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Extensions_IExtensionAction_Updated"></a> Updated

Occurs when the extension action has been updated.

```csharp
event EventHandler<ExtensionActionUpdatedEventArgs> Updated
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ExtensionActionUpdatedEventArgs](DotNetBrowser.Extensions.Events.ExtensionActionUpdatedEventArgs.md)\>

#### Remarks

You can use this event to monitor changes in the extension action badge, tooltip, or icon.

