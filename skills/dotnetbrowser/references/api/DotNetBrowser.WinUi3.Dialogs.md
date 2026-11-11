# <a id="DotNetBrowser_WinUi3_Dialogs"></a> Namespace DotNetBrowser.WinUi3.Dialogs

### Classes

 [DefaultAuthenticationHandler](DotNetBrowser.WinUi3.Dialogs.md#DotNetBrowser_WinUi3_Dialogs_DefaultAuthenticationHandler)

Default WinUI 3 authentication handler, which displays an authentication dialog.

 [DialogHandlerBase](DotNetBrowser.WinUi3.Dialogs.md#DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase)

The base class for all dialog handlers.

## <a id="DotNetBrowser_WinUi3_Dialogs_DefaultAuthenticationHandler"></a> Class DefaultAuthenticationHandler

Namespace: [DotNetBrowser.WinUi3.Dialogs](DotNetBrowser.WinUi3.Dialogs.md)  
Assembly: DotNetBrowser.WinUi3.dll  

Default WinUI 3 authentication handler, which displays an authentication dialog.

```csharp
public class DefaultAuthenticationHandler : DialogHandlerBase, IHandler<AuthenticateParameters, AuthenticateResponse>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.WinUi3.Dialogs.md#DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase) ← 
[DefaultAuthenticationHandler](DotNetBrowser.WinUi3.Dialogs.md#DotNetBrowser_WinUi3_Dialogs_DefaultAuthenticationHandler)

##### Implements

IHandler<AuthenticateParameters, AuthenticateResponse\>

##### Inherited Members

[DialogHandlerBase.Parent](DotNetBrowser.WinUi3.Dialogs.md#DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase_Parent), 
[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_WinUi3_Dialogs_DefaultAuthenticationHandler__ctor_Microsoft_UI_Xaml_Window_Microsoft_UI_Xaml_UIElement_"></a> DefaultAuthenticationHandler\(Window, UIElement\)

```csharp
public DefaultAuthenticationHandler(Window owner, UIElement parent)
```

##### Parameters

`owner` [Window](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.window)

`parent` [UIElement](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement)

### Methods

#### <a id="DotNetBrowser_WinUi3_Dialogs_DefaultAuthenticationHandler_Handle_DotNetBrowser_Net_Handlers_AuthenticateParameters_"></a> Handle\(AuthenticateParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
public AuthenticateResponse Handle(AuthenticateParameters parameters)
```

##### Parameters

`parameters` AuthenticateParameters

The handler parameters.

##### Returns

 AuthenticateResponse

An object that represents the response that should be
determined based on the provided parameters.

## <a id="DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase"></a> Class DialogHandlerBase

Namespace: [DotNetBrowser.WinUi3.Dialogs](DotNetBrowser.WinUi3.Dialogs.md)  
Assembly: DotNetBrowser.WinUi3.dll  

The base class for all dialog handlers.

```csharp
public class DialogHandlerBase
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.WinUi3.Dialogs.md#DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase)

##### Derived

[DefaultAuthenticationHandler](DotNetBrowser.WinUi3.Dialogs.md#DotNetBrowser_WinUi3_Dialogs_DefaultAuthenticationHandler)

##### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase__ctor_Microsoft_UI_Xaml_UIElement_"></a> DialogHandlerBase\(UIElement\)

Creates and initializes the dialog handler.

```csharp
public DialogHandlerBase(UIElement parent)
```

##### Parameters

`parent` [UIElement](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement)

The parent object for the dialog displayed by this handler.

### Properties

#### <a id="DotNetBrowser_WinUi3_Dialogs_DialogHandlerBase_Parent"></a> Parent

The parent object for the dialog displayed by this handler. This object is used to locate the owner
window for the modal dialogs.

```csharp
protected UIElement Parent { get; }
```

##### Property Value

 [UIElement](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement)
