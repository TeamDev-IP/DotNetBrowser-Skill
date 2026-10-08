# <a id="DotNetBrowser_Browser_IOffScreenRenderProvider"></a> Interface IOffScreenRenderProvider

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

Provides access to an image rendered by the browser
that works in the off-screen rendering mode.

```csharp
public interface IOffScreenRenderProvider
```

## Properties

### <a id="DotNetBrowser_Browser_IOffScreenRenderProvider_PaintHandler"></a> PaintHandler

Gets or sets a handler that is used when the browser contents should be rendered.

```csharp
IHandler<PaintParameters> PaintHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-1.md)<PaintParameters\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_Browser_IOffScreenRenderProvider_Hide"></a> Hide\(\)

Tells the browser to stop rendering its content as if it was hidden.

```csharp
void Hide()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IOffScreenRenderProvider_Show"></a> Show\(\)

Tells the browser to start rendering its content as if it was shown on the screen.

```csharp
void Show()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IOffScreenRenderProvider_CursorChanged"></a> CursorChanged

Occurs when the cursor should be changed.

```csharp
event EventHandler<CursorChangedEventArgs> CursorChanged
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[CursorChangedEventArgs](DotNetBrowser.Browser.Events.CursorChangedEventArgs.md)\>

