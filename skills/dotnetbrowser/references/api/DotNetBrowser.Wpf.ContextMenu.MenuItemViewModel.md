# <a id="DotNetBrowser_Wpf_ContextMenu_MenuItemViewModel"></a> Class MenuItemViewModel

Namespace: [DotNetBrowser.Wpf.ContextMenu](DotNetBrowser.Wpf.ContextMenu.md)  
Assembly: DotNetBrowser.Wpf.dll  

```csharp
public abstract class MenuItemViewModel
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MenuItemViewModel](DotNetBrowser.Wpf.ContextMenu.MenuItemViewModel.md)

#### Inherited Members

[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

## Properties

### <a id="DotNetBrowser_Wpf_ContextMenu_MenuItemViewModel_Command"></a> Command

```csharp
public ICommand Command { get; }
```

#### Property Value

 [ICommand](https://learn.microsoft.com/dotnet/api/system.windows.input.icommand)

### <a id="DotNetBrowser_Wpf_ContextMenu_MenuItemViewModel_Header"></a> Header

```csharp
public string Header { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Wpf_ContextMenu_MenuItemViewModel_IsCheckable"></a> IsCheckable

```csharp
public bool IsCheckable { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Wpf_ContextMenu_MenuItemViewModel_IsChecked"></a> IsChecked

```csharp
public bool IsChecked { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Wpf_ContextMenu_MenuItemViewModel_IsEnabled"></a> IsEnabled

```csharp
public bool IsEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Wpf_ContextMenu_MenuItemViewModel_MenuItems"></a> MenuItems

```csharp
public ObservableCollection<MenuItemViewModel> MenuItems { get; }
```

#### Property Value

 [ObservableCollection](https://learn.microsoft.com/dotnet/api/system.collections.objectmodel.observablecollection\-1)<[MenuItemViewModel](DotNetBrowser.Wpf.ContextMenu.MenuItemViewModel.md)\>

