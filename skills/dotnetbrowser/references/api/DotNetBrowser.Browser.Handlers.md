# <a id="DotNetBrowser_Browser_Handlers"></a> Namespace DotNetBrowser.Browser.Handlers

### Classes

 [BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters)

The base class for <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> handlers parameters.

 [CreatePopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_CreatePopupParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.CreatePopupHandler" data-throw-if-not-resolved="false"></xref>.

 [CreatePopupResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_CreatePopupResponse)

The response to the <xref href="DotNetBrowser.Browser.IBrowser.CreatePopupHandler" data-throw-if-not-resolved="false"></xref>.

 [FrameParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters)

Represents the parameters of <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref>-related handlers associated with <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

 [InjectCssParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectCssParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.InjectCssHandler" data-throw-if-not-resolved="false"></xref>.

 [InjectCssResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectCssResponse)

The response to the <xref href="DotNetBrowser.Browser.IBrowser.InjectCssHandler" data-throw-if-not-resolved="false"></xref>.

 [InjectJsParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectJsParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.InjectJsHandler" data-throw-if-not-resolved="false"></xref>.

 [OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.OpenExtensionActionPopupHandler" data-throw-if-not-resolved="false"></xref>.

 [OpenPopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_OpenPopupParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.OpenPopupHandler" data-throw-if-not-resolved="false"></xref>.

 [RequestPdfDocumentPasswordParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.RequestPdfDocumentPasswordHandler" data-throw-if-not-resolved="false"></xref>.

 [RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse)

The response to the <xref href="DotNetBrowser.Browser.IBrowser.RequestPdfDocumentPasswordHandler" data-throw-if-not-resolved="false"></xref>.

 [RequestPrintParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref>.

 [RequestPrintResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintResponse)

The response to the <xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref>.

 [ShowContextMenuParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_ShowContextMenuParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref>.

 [ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_ShowContextMenuResponse)

The response to the <xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Browser_Handlers_BrowserParameters"></a> Class BrowserParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> handlers parameters.

```csharp
public class BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters)

##### Derived

[CreatePopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_CreatePopupParameters), 
[FrameParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters), 
[OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters), 
[OpenPopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_OpenPopupParameters), 
[PresentationRequest](DotNetBrowser.Cast.md#DotNetBrowser_Cast_PresentationRequest), 
[RequestPrintParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintParameters), 
[SaveCreditCardParameters](DotNetBrowser.Card.Handlers.md#DotNetBrowser_Card_Handlers_SaveCreditCardParameters), 
[SavePasswordParameters](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_SavePasswordParameters), 
[SaveUserDataProfileParameters](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_SaveUserDataProfileParameters), 
[ShowContextMenuParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_ShowContextMenuParameters), 
[StartDownloadParameters](DotNetBrowser.Downloads.Handlers.md#DotNetBrowser_Downloads_Handlers_StartDownloadParameters), 
[StartPresentationParameters](DotNetBrowser.Cast.Handlers.md#DotNetBrowser_Cast_Handlers_StartPresentationParameters), 
[StartSessionParameters](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionParameters), 
[UpdatePasswordParameters](DotNetBrowser.Passwords.Handlers.md#DotNetBrowser_Passwords_Handlers_UpdatePasswordParameters), 
[UpdateUserDataProfileParameters](DotNetBrowser.UserData.Handlers.md#DotNetBrowser_UserData_Handlers_UpdateUserDataProfileParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_Handlers_BrowserParameters_Browser"></a> Browser

Gets the <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance the handler is associated with.

```csharp
public IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

## <a id="DotNetBrowser_Browser_Handlers_CreatePopupParameters"></a> Class CreatePopupParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.CreatePopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CreatePopupParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[CreatePopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_CreatePopupParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_Handlers_CreatePopupParameters_TargetName"></a> TargetName

Gets the popup window target name that was passed through the <code>window.open()</code>
JavaScript function.

```csharp
public string TargetName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_Handlers_CreatePopupParameters_TargetUrl"></a> TargetUrl

Gets the target URL that will be loaded in the popup browser.

```csharp
public string TargetUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Browser_Handlers_CreatePopupParameters_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Browser_Handlers_CreatePopupResponse"></a> Class CreatePopupResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.CreatePopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CreatePopupResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CreatePopupResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_CreatePopupResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Browser_Handlers_CreatePopupResponse_Create"></a> Create\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the popup can be created.

```csharp
public static CreatePopupResponse Create()
```

##### Returns

 [CreatePopupResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_CreatePopupResponse)

The <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.CreatePopupHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Browser_Handlers_CreatePopupResponse_Suppress"></a> Suppress\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the popup creation should be
suppressed.

```csharp
public static CreatePopupResponse Suppress()
```

##### Returns

 [CreatePopupResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_CreatePopupResponse)

The <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.CreatePopupHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Browser_Handlers_FrameParameters"></a> Class FrameParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

Represents the parameters of <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref>-related handlers associated with <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

```csharp
public class FrameParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[FrameParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters)

##### Derived

[ConvertJsNameParameters](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameParameters), 
[InjectCssParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectCssParameters), 
[InjectJsParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectJsParameters), 
[RequestPdfDocumentPasswordParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_Handlers_FrameParameters_Frame"></a> Frame

Gets the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> instance associated with the handler.

```csharp
public IFrame Frame { get; }
```

##### Property Value

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

## <a id="DotNetBrowser_Browser_Handlers_InjectCssParameters"></a> Class InjectCssParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.InjectCssHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class InjectCssParameters : FrameParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[FrameParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters) ← 
[InjectCssParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectCssParameters)

##### Inherited Members

[FrameParameters.Frame](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters_Frame), 
[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Browser_Handlers_InjectCssResponse"></a> Class InjectCssResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.InjectCssHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class InjectCssResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[InjectCssResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectCssResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Browser_Handlers_InjectCssResponse_Inject_System_String_"></a> Inject\(string\)

Creates an <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse" data-throw-if-not-resolved="false"></xref> that injects the given <code class="paramref">customStylesheet</code> string that
represents a custom stylesheet
(CSS) into the document that is loaded in this browser instance.

```csharp
public static InjectCssResponse Inject(string customStylesheet)
```

##### Parameters

`customStylesheet` [string](https://learn.microsoft.com/dotnet/api/system.string)

The CSS code that will be injected into the document.

##### Returns

 [InjectCssResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectCssResponse)

The <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.InjectCssHandler" data-throw-if-not-resolved="false"></xref> implementation.

##### Remarks

If the CSS property defined in the given <code class="paramref">customStylesheet</code> string already exists
on the loaded HTML document, then the existing CSS property won't be overridden. The CSS
properties defined in the given <code class="paramref">customStylesheet</code> string will be applied only if
these properties aren't defined on the loaded document.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">customStylesheet</code> is null, empty or blank.

#### <a id="DotNetBrowser_Browser_Handlers_InjectCssResponse_Proceed"></a> Proceed\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it can proceed without injecting a custom
stylesheet.

```csharp
public static InjectCssResponse Proceed()
```

##### Returns

 [InjectCssResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectCssResponse)

The <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.InjectCssHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Browser_Handlers_InjectJsParameters"></a> Class InjectJsParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.InjectJsHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class InjectJsParameters : FrameParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[FrameParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters) ← 
[InjectJsParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_InjectJsParameters)

##### Inherited Members

[FrameParameters.Frame](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters_Frame), 
[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters"></a> Class OpenExtensionActionPopupParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.OpenExtensionActionPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenExtensionActionPopupParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters_ExtensionAction"></a> ExtensionAction

Gets the extension action that requests opening the popup.

```csharp
public IExtensionAction ExtensionAction { get; }
```

##### Property Value

 [IExtensionAction](DotNetBrowser.Extensions.md#DotNetBrowser_Extensions_IExtensionAction)

#### <a id="DotNetBrowser_Browser_Handlers_OpenExtensionActionPopupParameters_PopupBrowser"></a> PopupBrowser

Gets the created popup browser.

```csharp
public IBrowser PopupBrowser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

## <a id="DotNetBrowser_Browser_Handlers_OpenPopupParameters"></a> Class OpenPopupParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.OpenPopupHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class OpenPopupParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[OpenPopupParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_OpenPopupParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_Handlers_OpenPopupParameters_PopupBrowser"></a> PopupBrowser

Gets the browser instance which should be opened in a popup window.

```csharp
public IBrowser PopupBrowser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Browser_Handlers_OpenPopupParameters_Rectangle"></a> Rectangle

Gets the initial bounds of the popup.

```csharp
public Rectangle Rectangle { get; }
```

##### Property Value

 [Rectangle](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Rectangle)

### Methods

#### <a id="DotNetBrowser_Browser_Handlers_OpenPopupParameters_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordParameters"></a> Class RequestPdfDocumentPasswordParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.RequestPdfDocumentPasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RequestPdfDocumentPasswordParameters : FrameParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[FrameParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters) ← 
[RequestPdfDocumentPasswordParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordParameters)

##### Inherited Members

[FrameParameters.Frame](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters_Frame), 
[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordParameters_Url"></a> Url

Gets the URL of the encrypted PDF document.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse"></a> Class RequestPdfDocumentPasswordResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.RequestPdfDocumentPasswordHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RequestPdfDocumentPasswordResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse_Cancel"></a> Cancel

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to
cancels the password request.

```csharp
public static RequestPdfDocumentPasswordResponse Cancel
```

##### Field Value

 [RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse)

##### Remarks

<p>
    Without a password, the browser will fail to load the frame with the encrypted
    PDF document and a <xref href="DotNetBrowser.Navigation.INavigation.FrameLoadFailed" data-throw-if-not-resolved="false"></xref> event will be fired for
    that frame.
</p>

#### <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse_ShowPasswordDialog"></a> ShowPasswordDialog

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to
use the standard PDF viewer password dialog UI to load the encrypted PDF document.

```csharp
public static RequestPdfDocumentPasswordResponse ShowPasswordDialog
```

##### Field Value

 [RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse)

### Methods

#### <a id="DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse_Password_System_String_"></a> Password\(string\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to
use the <code>password</code> password to load the encrypted PDF document.

```csharp
public static RequestPdfDocumentPasswordResponse Password(string password)
```

##### Parameters

`password` [string](https://learn.microsoft.com/dotnet/api/system.string)

The password for the encrypted PDF document.

##### Returns

 [RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPdfDocumentPasswordResponse)

The <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.RequestPdfDocumentPasswordHandler" data-throw-if-not-resolved="false"></xref> implementation.

##### Remarks

<p>
    If the provided password is incorrect, the browser will fail to load the frame with
    the PDF document.
</p>

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">password</code> is null, empty, or contains only blank characters.

## <a id="DotNetBrowser_Browser_Handlers_RequestPrintParameters"></a> Class RequestPrintParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class RequestPrintParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[RequestPrintParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Browser_Handlers_RequestPrintResponse"></a> Class RequestPrintResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RequestPrintResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[RequestPrintResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Browser_Handlers_RequestPrintResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the printing should be canceled.

```csharp
public static RequestPrintResponse Cancel()
```

##### Returns

 [RequestPrintResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintResponse)

The <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Browser_Handlers_RequestPrintResponse_Print"></a> Print\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to proceed with printing and
configure the print settings via the <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> and
<xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref> handlers.

```csharp
public static RequestPrintResponse Print()
```

##### Returns

 [RequestPrintResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintResponse)

The <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Browser_Handlers_RequestPrintResponse_ShowPrintPreview"></a> ShowPrintPreview\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to display the Print Preview dialog.

```csharp
public static RequestPrintResponse ShowPrintPreview()
```

##### Returns

 [RequestPrintResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_RequestPrintResponse)

The <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters"></a> Class ShowContextMenuParameters

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowContextMenuParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[ShowContextMenuParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_ShowContextMenuParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_ExtensionMenuItems"></a> ExtensionMenuItems

Gets the collection of the extension context menu items.

```csharp
public IEnumerable<ContextMenuItem> ExtensionMenuItems { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[ContextMenuItem](DotNetBrowser.ContextMenu.md#DotNetBrowser_ContextMenu_ContextMenuItem)\>

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_FrameCharset"></a> FrameCharset

Gets the character encoding of the frame on which the menu is invoked.

```csharp
public string FrameCharset { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_FrameUrl"></a> FrameUrl

Gets the URL of the sub-frame that the context menu was invoked on.

```csharp
public string FrameUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_IsMainFrame"></a> IsMainFrame

Indicates whether the context menu is invoked on the main frame.

```csharp
public bool IsMainFrame { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_LinkText"></a> LinkText

Gets the text associated with the link.

```csharp
public string LinkText { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_LinkUrl"></a> LinkUrl

Gets the URL of the link that encloses the node the context menu
was invoked on.

```csharp
public string LinkUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_Location"></a> Location

Gets the context menu location. This location is related to the frame the context menu
is invoked on.

```csharp
public Point Location { get; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_MediaType"></a> MediaType

Gets the media type of the node the context menu is being invoked on.

```csharp
public MediaType MediaType { get; }
```

##### Property Value

 [MediaType](DotNetBrowser.Media.md#DotNetBrowser_Media_MediaType)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_PageUrl"></a> PageUrl

Gets the URL of the top level page that the context menu was invoked on.

```csharp
public string PageUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_SelectedText"></a> SelectedText

Gets the text of the selection that the context menu was invoked on.

```csharp
public string SelectedText { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_SourceUrl"></a> SourceUrl

Gets the source URL for the element that the context menu was
invoked on.

```csharp
public string SourceUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_SpellCheckMenu"></a> SpellCheckMenu

Gets the spell check submenu.

```csharp
public SpellCheckMenu SpellCheckMenu { get; }
```

##### Property Value

 [SpellCheckMenu](DotNetBrowser.SpellCheck.md#DotNetBrowser_SpellCheck_SpellCheckMenu)

### Methods

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuParameters_ToString"></a> ToString\(\)

Represent object as string

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

a string that represents the object

## <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuResponse"></a> Class ShowContextMenuResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowContextMenuResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_ShowContextMenuResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuResponse_Close"></a> Close\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser the context menu should be closed.

```csharp
public static ShowContextMenuResponse Close()
```

##### Returns

 [ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_ShowContextMenuResponse)

The <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Browser_Handlers_ShowContextMenuResponse_Select_DotNetBrowser_ContextMenu_ContextMenuItem_"></a> Select\(ContextMenuItem\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the <code>item</code> should be
selected. The browser will execute the
corresponding functionality of the selected context menu item. The context menu state
will be changed to closed.

```csharp
public static ShowContextMenuResponse Select(ContextMenuItem item)
```

##### Parameters

`item` [ContextMenuItem](DotNetBrowser.ContextMenu.md#DotNetBrowser_ContextMenu_ContextMenuItem)

The menu item that should be selected.

##### Returns

 [ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_ShowContextMenuResponse)

The <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.ShowContextMenuHandler" data-throw-if-not-resolved="false"></xref> implementation.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">item</code> is null.
