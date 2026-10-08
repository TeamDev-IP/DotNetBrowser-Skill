# <a id="DotNetBrowser_WinUi3_Extensions_DefaultOpenExtensionPopupHandler"></a> Class DefaultOpenExtensionPopupHandler

Namespace: [DotNetBrowser.WinUi3.Extensions](DotNetBrowser.WinUi3.Extensions.md)  
Assembly: DotNetBrowser.WinUi3.dll  

Default extension popup handler, which displays an extension popup as a separate window.

```csharp
public sealed class DefaultOpenExtensionPopupHandler : IHandler<OpenExtensionPopupParameters>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DefaultOpenExtensionPopupHandler](DotNetBrowser.WinUi3.Extensions.DefaultOpenExtensionPopupHandler.md)

#### Implements

IHandler<OpenExtensionPopupParameters\>

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_WinUi3_Extensions_DefaultOpenExtensionPopupHandler__ctor_Microsoft_UI_Xaml_FrameworkElement_"></a> DefaultOpenExtensionPopupHandler\(FrameworkElement\)

Creates and initializes a new instance of <xref href="DotNetBrowser.WinUi3.Extensions.DefaultOpenExtensionPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public DefaultOpenExtensionPopupHandler(FrameworkElement parent)
```

#### Parameters

`parent` [FrameworkElement](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement)

The parent object for the window displayed by this handler.

## Methods

### <a id="DotNetBrowser_WinUi3_Extensions_DefaultOpenExtensionPopupHandler_Handle_DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_"></a> Handle\(OpenExtensionPopupParameters\)

This method is called when Chromium is about to display the extension popup window.

```csharp
public void Handle(OpenExtensionPopupParameters parameters)
```

#### Parameters

`parameters` OpenExtensionPopupParameters

The extension popup parameters.

