# <a id="DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase"></a> Class DialogHandlerBase

Namespace: [DotNetBrowser.WinUi3.Dialogs](DotNetBrowser.WinUi3.Dialogs.md)  
Assembly: DotNetBrowser.WinUi3.dll  

The base class for all dialog handlers.

```csharp
public class DialogHandlerBase
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.WinUi3.Dialogs.DialogHandlerBase.md)

#### Derived

[DefaultAuthenticationHandler](DotNetBrowser.WinUi3.Dialogs.DefaultAuthenticationHandler.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase__ctor_Microsoft_UI_Xaml_UIElement_"></a> DialogHandlerBase\(UIElement\)

Creates and initializes the dialog handler.

```csharp
public DialogHandlerBase(UIElement parent)
```

#### Parameters

`parent` [UIElement](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement)

The parent object for the dialog displayed by this handler.

## Properties

### <a id="DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase_Parent"></a> Parent

The parent object for the dialog displayed by this handler. This object is used to locate the owner
window for the modal dialogs.

```csharp
protected UIElement Parent { get; }
```

#### Property Value

 [UIElement](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement)

