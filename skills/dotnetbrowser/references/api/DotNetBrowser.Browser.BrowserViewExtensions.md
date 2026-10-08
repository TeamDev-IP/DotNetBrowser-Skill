# <a id="DotNetBrowser_Browser_BrowserViewExtensions"></a> Class BrowserViewExtensions

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Browser.IBrowserView" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class BrowserViewExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserViewExtensions](DotNetBrowser.Browser.BrowserViewExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_BrowserViewExtensions_InitializeFrom_DotNetBrowser_Browser_IBrowserView_DotNetBrowser_Browser_IBrowser_"></a> InitializeFrom\(IBrowserView, IBrowser\)

Initialize a browser view from this particular <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance. If there is another browser view
bound to this browser instance, that view will be de-initialized.

```csharp
public static void InitializeFrom(this IBrowserView browserView, IBrowser browser)
```

#### Parameters

`browserView` [IBrowserView](DotNetBrowser.Browser.IBrowserView.md)

the browser view to initialize.

`browser` [IBrowser](DotNetBrowser.Browser.IBrowser.md)

the browser instance to initialize from.

