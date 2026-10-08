# <a id="DotNetBrowser_Browser_Dialogs_Handlers_ConfirmResponse"></a> Class ConfirmResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.ConfirmHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ConfirmResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ConfirmResponse](DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_ConfirmResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the JavaScript confirmation dialog should
be canceled.

```csharp
public static ConfirmResponse Cancel()
```

#### Returns

 [ConfirmResponse](DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.ConfirmHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_ConfirmResponse_Ok"></a> Ok\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the JavaScript confirmation dialog should
be closed with the
"OK" action.

```csharp
public static ConfirmResponse Ok()
```

#### Returns

 [ConfirmResponse](DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.ConfirmHandler" data-throw-if-not-resolved="false"></xref> implementation.

