# <a id="DotNetBrowser_AvaloniaUi_Dialogs_DefaultAuthenticationHandler"></a> Class DefaultAuthenticationHandler

Namespace: [DotNetBrowser.AvaloniaUi.Dialogs](DotNetBrowser.AvaloniaUi.Dialogs.md)  
Assembly: DotNetBrowser.AvaloniaUi.dll  

Default Avalonia UI authentication handler, which displays an authentication dialog.

```csharp
public class DefaultAuthenticationHandler : DialogHandlerBase, IHandler<AuthenticateParameters, AuthenticateResponse>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.AvaloniaUi.Dialogs.DialogHandlerBase.md) ← 
[DefaultAuthenticationHandler](DotNetBrowser.AvaloniaUi.Dialogs.DefaultAuthenticationHandler.md)

#### Implements

[IHandler<AuthenticateParameters, AuthenticateResponse\>](DotNetBrowser.Handlers.IHandler\-2.md)

#### Inherited Members

[DialogHandlerBase.Parent](DotNetBrowser.AvaloniaUi.Dialogs.DialogHandlerBase.md\#DotNetBrowser\_AvaloniaUi\_Dialogs\_DialogHandlerBase\_Parent), 
[DialogHandlerBase.FocusParent\(\)](DotNetBrowser.AvaloniaUi.Dialogs.DialogHandlerBase.md\#DotNetBrowser\_AvaloniaUi\_Dialogs\_DialogHandlerBase\_FocusParent), 
[DialogHandlerBase.GetStorageProvider\(\)](DotNetBrowser.AvaloniaUi.Dialogs.DialogHandlerBase.md\#DotNetBrowser\_AvaloniaUi\_Dialogs\_DialogHandlerBase\_GetStorageProvider), 
[DialogHandlerBase.UnfocusFocusBrowser\(IBrowser\)](DotNetBrowser.AvaloniaUi.Dialogs.DialogHandlerBase.md\#DotNetBrowser\_AvaloniaUi\_Dialogs\_DialogHandlerBase\_UnfocusFocusBrowser\_DotNetBrowser\_Browser\_IBrowser\_), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_AvaloniaUi_Dialogs_DefaultAuthenticationHandler__ctor_Avalonia_Visual_"></a> DefaultAuthenticationHandler\(Visual\)

Creates and initializes the dialog handler.

```csharp
public DefaultAuthenticationHandler(Visual parent)
```

#### Parameters

`parent` Visual

The parent object for the dialog displayed by this handler.

## Methods

### <a id="DotNetBrowser_AvaloniaUi_Dialogs_DefaultAuthenticationHandler_Handle_DotNetBrowser_Net_Handlers_AuthenticateParameters_"></a> Handle\(AuthenticateParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
public AuthenticateResponse Handle(AuthenticateParameters parameters)
```

#### Parameters

`parameters` [AuthenticateParameters](DotNetBrowser.Net.Handlers.AuthenticateParameters.md)

the handler parameters.

#### Returns

 [AuthenticateResponse](DotNetBrowser.Net.Handlers.AuthenticateResponse.md)

an object that represents the response that should be
determined based on the provided parameters.

