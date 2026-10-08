# <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuResponse"></a> Class ShowContextMenuResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowContextMenuResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuResponse_Close"></a> Close\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser the context menu should be closed.

```csharp
public static ShowContextMenuResponse Close()
```

#### Returns

 [ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuResponse_Select_DotNetBrowser_ContextMenu_ContextMenuItem_"></a> Select\(ContextMenuItem\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the <code>item</code> should be
selected. The browser will execute the
corresponding functionality of the selected context menu item. The context menu state
will be changed to closed.

```csharp
public static ShowContextMenuResponse Select(ContextMenuItem item)
```

#### Parameters

`item` [ContextMenuItem](DotNetBrowser.ContextMenu.ContextMenuItem.md)

The menu item that should be selected.

#### Returns

 [ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">item</code> is null.

