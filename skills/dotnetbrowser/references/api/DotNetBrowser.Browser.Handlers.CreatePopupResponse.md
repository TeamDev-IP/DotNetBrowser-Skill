# <a id="DotNetBrowser_Browser_Handlers_CreatePopupResponse"></a> Class CreatePopupResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.CreatePopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CreatePopupResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CreatePopupResponse](DotNetBrowser.Browser.Handlers.CreatePopupResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_Handlers_CreatePopupResponse_Create"></a> Create\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the popup can be created.

```csharp
public static CreatePopupResponse Create()
```

#### Returns

 [CreatePopupResponse](DotNetBrowser.Browser.Handlers.CreatePopupResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.CreatePopupHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Handlers_CreatePopupResponse_Suppress"></a> Suppress\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the popup creation should be
suppressed.

```csharp
public static CreatePopupResponse Suppress()
```

#### Returns

 [CreatePopupResponse](DotNetBrowser.Browser.Handlers.CreatePopupResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.CreatePopupHandler" data-throw-if-not-resolved="false"></xref> implementation.

