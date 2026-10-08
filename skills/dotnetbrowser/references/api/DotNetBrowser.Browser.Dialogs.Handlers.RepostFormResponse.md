# <a id="DotNetBrowser_Browser_Dialogs_Handlers_RepostFormResponse"></a> Class RepostFormResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.RepostFormHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RepostFormResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[RepostFormResponse](DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_RepostFormResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the page reloading should be canceled.

```csharp
public static RepostFormResponse Cancel()
```

#### Returns

 [RepostFormResponse](DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.RepostFormHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_RepostFormResponse_Repost"></a> Repost\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that resubmitting POST data is allowed.

```csharp
public static RepostFormResponse Repost()
```

#### Returns

 [RepostFormResponse](DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.RepostFormHandler" data-throw-if-not-resolved="false"></xref> implementation.

