# <a id="DotNetBrowser_Browser_Handlers_OpenPopupParameters"></a> Class OpenPopupParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.OpenPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenPopupParameters : BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md) ← 
[OpenPopupParameters](DotNetBrowser.Browser.Handlers.OpenPopupParameters.md)

#### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.BrowserParameters.md\#DotNetBrowser\_Browser\_Handlers\_BrowserParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Handlers_OpenPopupParameters_PopupBrowser"></a> PopupBrowser

Gets the browser instance which should be opened in a popup window.

```csharp
public IBrowser PopupBrowser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Browser_Handlers_OpenPopupParameters_Rectangle"></a> Rectangle

Gets the initial bounds of the popup.

```csharp
public Rectangle Rectangle { get; }
```

#### Property Value

 [Rectangle](DotNetBrowser.Geometry.Rectangle.md)

## Methods

### <a id="DotNetBrowser_Browser_Handlers_OpenPopupParameters_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

