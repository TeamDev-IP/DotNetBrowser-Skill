# <a id="DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters"></a> Class OpenExtensionPopupParameters

Namespace: [DotNetBrowser.Extensions.Handlers](DotNetBrowser.Extensions.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Extensions.IExtension.OpenExtensionPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenExtensionPopupParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[OpenExtensionPopupParameters](DotNetBrowser.Extensions.Handlers.OpenExtensionPopupParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_Extension"></a> Extension

Gets the extension that requests opening the popup.

```csharp
public IExtension Extension { get; }
```

#### Property Value

 [IExtension](DotNetBrowser.Extensions.IExtension.md)

### <a id="DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_PopupBrowser"></a> PopupBrowser

Gets the created popup browser.

```csharp
public IBrowser PopupBrowser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Extensions_Handlers_OpenExtensionPopupParameters_Url"></a> Url

Gets the URL of the popup.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

