# <a id="DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters"></a> Class OpenExtensionActionPopupParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.OpenExtensionActionPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenExtensionActionPopupParameters : BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md) ← 
[OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters.md)

#### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.BrowserParameters.md\#DotNetBrowser\_Browser\_Handlers\_BrowserParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters_ExtensionAction"></a> ExtensionAction

Gets the extension action that requests opening the popup.

```csharp
public IExtensionAction ExtensionAction { get; }
```

#### Property Value

 [IExtensionAction](DotNetBrowser.Extensions.IExtensionAction.md)

### <a id="DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters_PopupBrowser"></a> PopupBrowser

Gets the created popup browser.

```csharp
public IBrowser PopupBrowser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

