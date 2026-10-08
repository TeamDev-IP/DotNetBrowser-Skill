# <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters"></a> Class ShowContextMenuParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowContextMenuParameters : BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md) ← 
[ShowContextMenuParameters](DotNetBrowser.Browser.Handlers.ShowContextMenuParameters.md)

#### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.BrowserParameters.md\#DotNetBrowser\_Browser\_Handlers\_BrowserParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_ExtensionMenuItems"></a> ExtensionMenuItems

Gets the collection of the extension context menu items.

```csharp
public IEnumerable<ContextMenuItem> ExtensionMenuItems { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[ContextMenuItem](DotNetBrowser.ContextMenu.ContextMenuItem.md)\>

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_FrameCharset"></a> FrameCharset

Gets the character encoding of the frame on which the menu is invoked.

```csharp
public string FrameCharset { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_FrameUrl"></a> FrameUrl

Gets the URL of the sub-frame that the context menu was invoked on.

```csharp
public string FrameUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_IsMainFrame"></a> IsMainFrame

Indicates whether the context menu is invoked on the main frame.

```csharp
public bool IsMainFrame { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_LinkText"></a> LinkText

Gets the text associated with the link.

```csharp
public string LinkText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_LinkUrl"></a> LinkUrl

Gets the URL of the link that encloses the node the context menu
was invoked on.

```csharp
public string LinkUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_Location"></a> Location

Gets the context menu location. This location is related to the frame the context menu
is invoked on.

```csharp
public Point Location { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_MediaType"></a> MediaType

Gets the media type of the node the context menu is being invoked on.

```csharp
public MediaType MediaType { get; }
```

#### Property Value

 [MediaType](DotNetBrowser.Media.MediaType.md)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_PageUrl"></a> PageUrl

Gets the URL of the top level page that the context menu was invoked on.

```csharp
public string PageUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_SelectedText"></a> SelectedText

Gets the text of the selection that the context menu was invoked on.

```csharp
public string SelectedText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_SourceUrl"></a> SourceUrl

Gets the source URL for the element that the context menu was
invoked on.

```csharp
public string SourceUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_SpellCheckMenu"></a> SpellCheckMenu

Gets the spell check submenu.

```csharp
public SpellCheckMenu SpellCheckMenu { get; }
```

#### Property Value

 [SpellCheckMenu](DotNetBrowser.SpellCheck.SpellCheckMenu.md)

## Methods

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_ToString"></a> ToString\(\)

Represent object as string

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

a string that represents the object

