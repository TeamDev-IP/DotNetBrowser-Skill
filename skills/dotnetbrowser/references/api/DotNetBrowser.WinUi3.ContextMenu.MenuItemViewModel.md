# <a id="DotNetBrowser_WinUi3_ContextMenu_MenuItemViewModel"></a> Class MenuItemViewModel

Namespace: [DotNetBrowser.WinUi3.ContextMenu](DotNetBrowser.WinUi3.ContextMenu.md)  
Assembly: DotNetBrowser.WinUi3.dll  

Represent the view model of a single menu item.

```csharp
public class MenuItemViewModel
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MenuItemViewModel](DotNetBrowser.WinUi3.ContextMenu.MenuItemViewModel.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_WinUi3_ContextMenu_MenuItemViewModel_Command"></a> Command

Gets or sets the command to execute when the menu item is selected.

```csharp
public ICommand Command { get; set; }
```

#### Property Value

 [ICommand](https://learn.microsoft.com/dotnet/api/system.windows.input.icommand)

### <a id="DotNetBrowser_WinUi3_ContextMenu_MenuItemViewModel_Header"></a> Header

Gets the menu item header.

```csharp
public string Header { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_WinUi3_ContextMenu_MenuItemViewModel_IsCheckable"></a> IsCheckable

Gets the checkable status that says whether the menu item has the check button behavior.

```csharp
public bool IsCheckable { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_WinUi3_ContextMenu_MenuItemViewModel_IsChecked"></a> IsChecked

Gets the checked status  of menu item. Actual if <xref href="DotNetBrowser.WinUi3.ContextMenu.MenuItemViewModel.IsCheckable" data-throw-if-not-resolved="false"></xref> is true.

```csharp
public bool IsChecked { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_WinUi3_ContextMenu_MenuItemViewModel_IsEnabled"></a> IsEnabled

Gets the enabled status that says whether the menu item is enabled.

```csharp
public bool IsEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_WinUi3_ContextMenu_MenuItemViewModel_MenuItems"></a> MenuItems

Gets the collection of submenu items.

```csharp
public ObservableCollection<MenuItemViewModel> MenuItems { get; }
```

#### Property Value

 [ObservableCollection](https://learn.microsoft.com/dotnet/api/system.collections.objectmodel.observablecollection\-1)<[MenuItemViewModel](DotNetBrowser.WinUi3.ContextMenu.MenuItemViewModel.md)\>

## Methods

### <a id="DotNetBrowser_WinUi3_ContextMenu_MenuItemViewModel_Execute"></a> Execute\(\)

Execute command logic.

```csharp
protected virtual void Execute()
```

