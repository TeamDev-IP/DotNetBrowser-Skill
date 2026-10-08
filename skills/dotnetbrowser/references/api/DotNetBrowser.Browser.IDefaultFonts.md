# <a id="DotNetBrowser_Browser_IDefaultFonts"></a> Interface IDefaultFonts

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The default fonts used by a browser.

```csharp
public interface IDefaultFonts
```

## Remarks

An instance of this interface belongs to a browser and can be used while the browser is alive.

## Properties

### <a id="DotNetBrowser_Browser_IDefaultFonts_Available"></a> Available

Gets the system fonts available to the browser.

```csharp
IReadOnlyList<Font> Available { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Font](DotNetBrowser.Ui.Font.md)\>

#### Remarks

The available fonts depend on the operating system and the fonts installed on it.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IDefaultFonts_FixedWidth"></a> FixedWidth

Gets or sets the fixed-width font used by the browser.

```csharp
Font FixedWidth { get; set; }
```

#### Property Value

 [Font](DotNetBrowser.Ui.Font.md)

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IDefaultFonts_Mathematical"></a> Mathematical

Gets or sets the mathematical font used by the browser.

```csharp
Font Mathematical { get; set; }
```

#### Property Value

 [Font](DotNetBrowser.Ui.Font.md)

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IDefaultFonts_SansSerif"></a> SansSerif

Gets or sets the sans-serif font used by the browser.

```csharp
Font SansSerif { get; set; }
```

#### Property Value

 [Font](DotNetBrowser.Ui.Font.md)

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IDefaultFonts_Serif"></a> Serif

Gets or sets the serif font used by the browser.

```csharp
Font Serif { get; set; }
```

#### Property Value

 [Font](DotNetBrowser.Ui.Font.md)

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IDefaultFonts_Standard"></a> Standard

Gets or sets the standard font used by the browser.

```csharp
Font Standard { get; set; }
```

#### Property Value

 [Font](DotNetBrowser.Ui.Font.md)

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The value is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The associated browser has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

