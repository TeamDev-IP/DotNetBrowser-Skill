# <a id="DotNetBrowser_ContextMenu_ContextMenuItem"></a> Class ContextMenuItem

Namespace: [DotNetBrowser.ContextMenu](DotNetBrowser.ContextMenu.md)  
Assembly: DotNetBrowser.dll  

A custom context menu item.

```csharp
public sealed class ContextMenuItem
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ContextMenuItem](DotNetBrowser.ContextMenu.ContextMenuItem.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_ContextMenu_ContextMenuItem_IsChecked"></a> IsChecked

Indicates whether context menu item is checked or not.

```csharp
public bool IsChecked { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_ContextMenu_ContextMenuItem_IsEnabled"></a> IsEnabled

Indicates whether context menu item is enabled or not.

```csharp
public bool IsEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_ContextMenu_ContextMenuItem_SubItems"></a> SubItems

Gets a collection of sub-items.

```csharp
public IEnumerable<ContextMenuItem> SubItems { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[ContextMenuItem](DotNetBrowser.ContextMenu.ContextMenuItem.md)\>

### <a id="DotNetBrowser_ContextMenu_ContextMenuItem_Text"></a> Text

Gets the text of the context menu item.

```csharp
public string Text { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_ContextMenu_ContextMenuItem_Type"></a> Type

Gets the type of the context menu item.

```csharp
public ContextMenuItemType Type { get; }
```

#### Property Value

 [ContextMenuItemType](DotNetBrowser.ContextMenu.ContextMenuItemType.md)

