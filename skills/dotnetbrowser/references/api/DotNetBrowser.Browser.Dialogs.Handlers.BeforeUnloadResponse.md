# <a id="DotNetBrowser_Browser_Dialogs_Handlers_BeforeUnloadResponse"></a> Class BeforeUnloadResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.BeforeUnloadHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class BeforeUnloadResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BeforeUnloadResponse](DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_BeforeUnloadResponse_Leave"></a> Leave\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the user decided to leave the current
page.

```csharp
public static BeforeUnloadResponse Leave()
```

#### Returns

 [BeforeUnloadResponse](DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.BeforeUnloadHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_BeforeUnloadResponse_Stay"></a> Stay\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the user decided to stay on the
current page.

```csharp
public static BeforeUnloadResponse Stay()
```

#### Returns

 [BeforeUnloadResponse](DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.BeforeUnloadHandler" data-throw-if-not-resolved="false"></xref> implementation.

