# <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse"></a> Class RequestPdfDocumentPasswordResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.RequestPdfDocumentPasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RequestPdfDocumentPasswordResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse_Cancel"></a> Cancel

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to
cancels the password request.

```csharp
public static RequestPdfDocumentPasswordResponse Cancel
```

#### Field Value

 [RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.md)

#### Remarks

<p>
    Without a password, the browser will fail to load the frame with the encrypted
    PDF document and a <xref href="DotNetBrowser.Navigation.INavigation.FrameLoadFailed" data-throw-if-not-resolved="false"></xref> event will be fired for
    that frame.
</p>

### <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse_ShowPasswordDialog"></a> ShowPasswordDialog

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to
use the standard PDF viewer password dialog UI to load the encrypted PDF document.

```csharp
public static RequestPdfDocumentPasswordResponse ShowPasswordDialog
```

#### Field Value

 [RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.md)

## Methods

### <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse_Password_System_String_"></a> Password\(string\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to
use the <code>password</code> password to load the encrypted PDF document.

```csharp
public static RequestPdfDocumentPasswordResponse Password(string password)
```

#### Parameters

`password` [string](https://learn.microsoft.com/dotnet/api/system.string)

The password for the encrypted PDF document.

#### Returns

 [RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.RequestPdfDocumentPasswordHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Remarks

<p>
    If the provided password is incorrect, the browser will fail to load the frame with
    the PDF document.
</p>

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">password</code> is null, empty, or contains only blank characters.

