# <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenExternalAppResponse"></a> Class OpenExternalAppResponse

Namespace: [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenExternalAppHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenExternalAppResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[OpenExternalAppResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenExternalAppResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the link should not be opened in
the external application.

```csharp
public static OpenExternalAppResponse Cancel()
```

#### Returns

 [OpenExternalAppResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenExternalAppHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Dialogs_Handlers_OpenExternalAppResponse_Open"></a> Open\(\)

Creates a <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the link should be opened in the
associated external application.

```csharp
public static OpenExternalAppResponse Open()
```

#### Returns

 [OpenExternalAppResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse.md)

The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.Dialogs.IDialogs.OpenExternalAppHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Remarks

<p>
    If the application is not running, the operating system should launch the application
    and open the link in it.
</p>

