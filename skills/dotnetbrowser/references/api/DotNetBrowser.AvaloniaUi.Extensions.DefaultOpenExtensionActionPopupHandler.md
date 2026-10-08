# <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionActionPopupHandler"></a> Class DefaultOpenExtensionActionPopupHandler

Namespace: [DotNetBrowser.AvaloniaUi.Extensions](DotNetBrowser.AvaloniaUi.Extensions.md)  
Assembly: DotNetBrowser.AvaloniaUi.dll  

The default implementation of the <xref href="DotNetBrowser.Handlers.IHandler%601" data-throw-if-not-resolved="false"></xref> 
interface that opens a popup window with the specified <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public class DefaultOpenExtensionActionPopupHandler : IHandler<OpenExtensionActionPopupParameters>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DefaultOpenExtensionActionPopupHandler](DotNetBrowser.AvaloniaUi.Extensions.DefaultOpenExtensionActionPopupHandler.md)

#### Implements

[IHandler<OpenExtensionActionPopupParameters\>](DotNetBrowser.Handlers.IHandler\-1.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionActionPopupHandler__ctor_Avalonia_Visual_"></a> DefaultOpenExtensionActionPopupHandler\(Visual\)

Initializes a new instance of the <xref href="DotNetBrowser.AvaloniaUi.Extensions.DefaultOpenExtensionActionPopupHandler" data-throw-if-not-resolved="false"></xref>
class with the specified parent visual.

```csharp
public DefaultOpenExtensionActionPopupHandler(Visual parent)
```

#### Parameters

`parent` Visual

The parent visual for the popup window.

## Methods

### <a id="DotNetBrowser_AvaloniaUi_Extensions_DefaultOpenExtensionActionPopupHandler_Handle_DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters_"></a> Handle\(OpenExtensionActionPopupParameters\)

Handles the specified <xref href="DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters" data-throw-if-not-resolved="false"></xref>.

```csharp
public void Handle(OpenExtensionActionPopupParameters parameters)
```

#### Parameters

`parameters` [OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters.md)

The parameters for opening the extension action popup.

