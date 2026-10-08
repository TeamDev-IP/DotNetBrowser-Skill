# <a id="DotNetBrowser_WinForms_Dialogs_DefaultAuthenticationHandler"></a> Class DefaultAuthenticationHandler

Namespace: [DotNetBrowser.WinForms.Dialogs](DotNetBrowser.WinForms.Dialogs.md)  
Assembly: DotNetBrowser.WinForms.dll  

Default WinForms authentication handler, which displays an authentication dialog.

```csharp
public class DefaultAuthenticationHandler : DialogHandlerBase, IHandler<AuthenticateParameters, AuthenticateResponse>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DialogHandlerBase](DotNetBrowser.WinForms.Dialogs.DialogHandlerBase.md) ← 
[DefaultAuthenticationHandler](DotNetBrowser.WinForms.Dialogs.DefaultAuthenticationHandler.md)

#### Implements

IHandler<AuthenticateParameters, AuthenticateResponse\>

#### Inherited Members

[DialogHandlerBase.Parent](DotNetBrowser.WinForms.Dialogs.DialogHandlerBase.md\#DotNetBrowser\_WinForms\_Dialogs\_DialogHandlerBase\_Parent), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

## Constructors

### <a id="DotNetBrowser_WinForms_Dialogs_DefaultAuthenticationHandler__ctor_System_Windows_Forms_Control_"></a> DefaultAuthenticationHandler\(Control\)

Creates and initializes the dialog handler.

```csharp
public DefaultAuthenticationHandler(Control parent)
```

#### Parameters

`parent` [Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control)

The parent object for the dialog displayed by this handler.

## Methods

### <a id="DotNetBrowser_WinForms_Dialogs_DefaultAuthenticationHandler_Handle_DotNetBrowser_Net_Handlers_AuthenticateParameters_"></a> Handle\(AuthenticateParameters\)

This method is called when the Chromium callback needs a response that may be
determined based on the provided parameters.

```csharp
public AuthenticateResponse Handle(AuthenticateParameters parameters)
```

#### Parameters

`parameters` AuthenticateParameters

the handler parameters.

#### Returns

 AuthenticateResponse

an object that represents the response that should be
determined based on the provided parameters.

