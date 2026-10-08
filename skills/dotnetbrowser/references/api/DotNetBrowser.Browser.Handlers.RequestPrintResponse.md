# <a id="DotNetBrowser_Browser_Handlers_RequestPrintResponse"></a> Class RequestPrintResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class RequestPrintResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[RequestPrintResponse](DotNetBrowser.Browser.Handlers.RequestPrintResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_Handlers_RequestPrintResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the printing should be canceled.

```csharp
public static RequestPrintResponse Cancel()
```

#### Returns

 [RequestPrintResponse](DotNetBrowser.Browser.Handlers.RequestPrintResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Handlers_RequestPrintResponse_Print"></a> Print\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to proceed with printing and
configure the print settings via the <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> and
<xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref> handlers.

```csharp
public static RequestPrintResponse Print()
```

#### Returns

 [RequestPrintResponse](DotNetBrowser.Browser.Handlers.RequestPrintResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Browser_Handlers_RequestPrintResponse_ShowPrintPreview"></a> ShowPrintPreview\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to display the Print Preview dialog.

```csharp
public static RequestPrintResponse ShowPrintPreview()
```

#### Returns

 [RequestPrintResponse](DotNetBrowser.Browser.Handlers.RequestPrintResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref> implementation.

