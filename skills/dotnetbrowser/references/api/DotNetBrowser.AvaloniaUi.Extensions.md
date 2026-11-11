# <a id="DotNetBrowser_AvaloniaUi_Extensions"></a> Namespace DotNetBrowser.AvaloniaUi.Extensions

### Classes

 [DefaultOpenExtensionActionPopupHandler](DotNetBrowser.AvaloniaUi.Extensions.md#DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionActionPopupHandler)

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%601" data-throw-if-not-resolved="false"></xref> 
interface that opens a popup window with the specified <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.

 [DefaultOpenExtensionPopupHandler](DotNetBrowser.AvaloniaUi.Extensions.md#DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionPopupHandler)

Default extension popup handler, which displays an extension popup as a separate window.

## <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionActionPopupHandler"></a> Class DefaultOpenExtensionActionPopupHandler

Namespace: [DotNetBrowser.AvaloniaUi.Extensions](DotNetBrowser.AvaloniaUi.Extensions.md)  
Assembly: DotNetBrowser.AvaloniaUi.dll  

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%601" data-throw-if-not-resolved="false"></xref> 
interface that opens a popup window with the specified <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public class DefaultOpenExtensionActionPopupHandler : IHandler<OpenExtensionActionPopupParameters>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DefaultOpenExtensionActionPopupHandler](DotNetBrowser.AvaloniaUi.Extensions.md#DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionActionPopupHandler)

##### Implements

[IHandler<OpenExtensionActionPopupParameters\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionActionPopupHandler__ctor_Avalonia_Visual_"></a> DefaultOpenExtensionActionPopupHandler\(Visual\)

Initializes a new instance of the <xref href="DotNetBrowser.AvaloniaUi.Extensions.DefaultOpenExtensionActionPopupHandler" data-throw-if-not-resolved="false"></xref>
class with the specified parent visual.

```csharp
public DefaultOpenExtensionActionPopupHandler(Visual parent)
```

##### Parameters

`parent` Visual

The parent visual for the popup window.

### Methods

#### <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionActionPopupHandler_Handle_DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters_"></a> Handle\(OpenExtensionActionPopupParameters\)

Handles the specified <xref href="DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters" data-throw-if-not-resolved="false"></xref>.

```csharp
public void Handle(OpenExtensionActionPopupParameters parameters)
```

##### Parameters

`parameters` [OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters)

The parameters for opening the extension action popup.

## <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionPopupHandler"></a> Class DefaultOpenExtensionPopupHandler

Namespace: [DotNetBrowser.AvaloniaUi.Extensions](DotNetBrowser.AvaloniaUi.Extensions.md)  
Assembly: DotNetBrowser.AvaloniaUi.dll  

Default extension popup handler, which displays an extension popup as a separate window.

```csharp
public sealed class DefaultOpenExtensionPopupHandler : IHandler<OpenExtensionPopupParameters>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DefaultOpenExtensionPopupHandler](DotNetBrowser.AvaloniaUi.Extensions.md#DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionPopupHandler)

##### Implements

[IHandler<OpenExtensionPopupParameters\>](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionPopupHandler__ctor_Avalonia_Visual_"></a> DefaultOpenExtensionPopupHandler\(Visual\)

Creates and initializes a new instance of <xref href="DotNetBrowser.AvaloniaUi.Extensions.DefaultOpenExtensionPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public DefaultOpenExtensionPopupHandler(Visual parent)
```

##### Parameters

`parent` Visual

The parent object for the window displayed by this handler.

### Methods

#### <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionPopupHandler_Handle_DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_"></a> Handle\(OpenExtensionPopupParameters\)

This method is called when Chromium is about to display the extension popup window.

```csharp
public void Handle(OpenExtensionPopupParameters parameters)
```

##### Parameters

`parameters` [OpenExtensionPopupParameters](DotNetBrowser.Extensions.Handlers.md#DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters)

The extension popup parameters.
