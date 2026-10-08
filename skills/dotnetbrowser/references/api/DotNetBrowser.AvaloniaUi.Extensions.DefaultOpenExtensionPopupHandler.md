# <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionPopupHandler"></a> Class DefaultOpenExtensionPopupHandler

Namespace: [DotNetBrowser.AvaloniaUi.Extensions](DotNetBrowser.AvaloniaUi.Extensions.md)  
Assembly: DotNetBrowser.AvaloniaUi.dll  

Default extension popup handler, which displays an extension popup as a separate window.

```csharp
public sealed class DefaultOpenExtensionPopupHandler : IHandler<OpenExtensionPopupParameters>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DefaultOpenExtensionPopupHandler](DotNetBrowser.AvaloniaUi.Extensions.DefaultOpenExtensionPopupHandler.md)

#### Implements

[IHandler<OpenExtensionPopupParameters\>](DotNetBrowser.Handlers.IHandler\-1.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionPopupHandler__ctor_Avalonia_Visual_"></a> DefaultOpenExtensionPopupHandler\(Visual\)

Creates and initializes a new instance of <xref href="DotNetBrowser.AvaloniaUi.Extensions.DefaultOpenExtensionPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public DefaultOpenExtensionPopupHandler(Visual parent)
```

#### Parameters

`parent` Visual

The parent object for the window displayed by this handler.

## Methods

### <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionPopupHandler_Handle_DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_"></a> Handle\(OpenExtensionPopupParameters\)

This method is called when Chromium is about to display the extension popup window.

```csharp
public void Handle(OpenExtensionPopupParameters parameters)
```

#### Parameters

`parameters` [OpenExtensionPopupParameters](DotNetBrowser.Extensions.Handlers.OpenExtensionPopupParameters.md)

The extension popup parameters.

