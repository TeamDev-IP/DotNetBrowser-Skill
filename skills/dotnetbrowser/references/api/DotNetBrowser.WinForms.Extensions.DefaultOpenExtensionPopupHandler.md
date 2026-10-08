# <a id="DotNetBrowser_WinForms_Extensions_DefaultOpenExtensionPopupHandler"></a> Class DefaultOpenExtensionPopupHandler

Namespace: [DotNetBrowser.WinForms.Extensions](DotNetBrowser.WinForms.Extensions.md)  
Assembly: DotNetBrowser.WinForms.dll  

Default extension popup handler, which displays an extension popup as a separate window.

```csharp
public sealed class DefaultOpenExtensionPopupHandler : IHandler<OpenExtensionPopupParameters>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DefaultOpenExtensionPopupHandler](DotNetBrowser.WinForms.Extensions.DefaultOpenExtensionPopupHandler.md)

#### Implements

IHandler<OpenExtensionPopupParameters\>

#### Inherited Members

[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype)

## Constructors

### <a id="DotNetBrowser_WinForms_Extensions_DefaultOpenExtensionPopupHandler__ctor_System_Windows_Forms_Control_"></a> DefaultOpenExtensionPopupHandler\(Control\)

Creates and initializes a new instance of <xref href="DotNetBrowser.WinForms.Extensions.DefaultOpenExtensionPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public DefaultOpenExtensionPopupHandler(Control parent)
```

#### Parameters

`parent` [Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control)

The parent object for the window displayed by this handler.

## Methods

### <a id="DotNetBrowser_WinForms_Extensions_DefaultOpenExtensionPopupHandler_Handle_DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_"></a> Handle\(OpenExtensionPopupParameters\)

This method is called when Chromium is about to display the extension popup window.

```csharp
public void Handle(OpenExtensionPopupParameters parameters)
```

#### Parameters

`parameters` OpenExtensionPopupParameters

The extension popup parameters.

