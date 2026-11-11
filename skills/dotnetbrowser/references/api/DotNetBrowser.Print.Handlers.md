# <a id="DotNetBrowser_Print_Handlers"></a> Namespace DotNetBrowser.Print.Handlers

### Classes

 [PrintContentParameters<TPrintSettings, TPdfPrintSettings\>](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintContentParameters_2)

The base class for content printing handlers parameters.

 [PrintHtmlContentParameters](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintHtmlContentParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref>.

 [PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintHtmlContentResponse)

A response for the <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref>.

 [PrintPdfContentParameters](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintPdfContentParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref>.

 [PrintPdfContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintPdfContentResponse)

A response for the <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Print_Handlers_PrintContentParameters_2"></a> Class PrintContentParameters<TPrintSettings, TPdfPrintSettings\>

Namespace: [DotNetBrowser.Print.Handlers](DotNetBrowser.Print.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for content printing handlers parameters.

```csharp
public class PrintContentParameters<TPrintSettings, TPdfPrintSettings> where TPrintSettings : class, SystemPrinter.ISettings<TPrintSettings> where TPdfPrintSettings : class, PdfPrinter.ISettings<TPdfPrintSettings>
```

##### Type Parameters

`TPrintSettings` 

The system print settings type.

`TPdfPrintSettings` 

The PDF print settings type.

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintContentParameters<TPrintSettings, TPdfPrintSettings\>](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintContentParameters_2)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Print_Handlers_PrintContentParameters_2_Browser"></a> Browser

Gets the browser associated with the handler.

```csharp
public IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Print_Handlers_PrintContentParameters_2_Printers"></a> Printers

Gets the collection of printers available in this handler.

```csharp
public IPrinters<TPrintSettings, TPdfPrintSettings> Printers { get; }
```

##### Property Value

 [IPrinters](DotNetBrowser.Print.md#DotNetBrowser_Print_IPrinters_2)<TPrintSettings, TPdfPrintSettings\>

## <a id="DotNetBrowser_Print_Handlers_PrintHtmlContentParameters"></a> Class PrintHtmlContentParameters

Namespace: [DotNetBrowser.Print.Handlers](DotNetBrowser.Print.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class PrintHtmlContentParameters : PrintContentParameters<SystemPrinter.IHtmlSettings, PdfPrinter.IHtmlSettings>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintContentParameters<SystemPrinter.IHtmlSettings, PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintContentParameters_2) ← 
[PrintHtmlContentParameters](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintHtmlContentParameters)

##### Inherited Members

[PrintContentParameters<SystemPrinter.IHtmlSettings, PdfPrinter.IHtmlSettings\>.Browser](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintContentParameters_2_Browser), 
[PrintContentParameters<SystemPrinter.IHtmlSettings, PdfPrinter.IHtmlSettings\>.Printers](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintContentParameters_2_Printers), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Print_Handlers_PrintHtmlContentResponse"></a> Class PrintHtmlContentResponse

Namespace: [DotNetBrowser.Print.Handlers](DotNetBrowser.Print.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class PrintHtmlContentResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintHtmlContentResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Print_Handlers_PrintHtmlContentResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to cancel printing.

```csharp
public static PrintHtmlContentResponse Cancel()
```

##### Returns

 [PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintHtmlContentResponse)

The <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Print_Handlers_PrintHtmlContentResponse_Print_DotNetBrowser_Print_SystemPrinter_DotNetBrowser_Print_SystemPrinter_IHtmlSettings__"></a> Print\(SystemPrinter<IHtmlSettings\>\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to proceed with the passed printer.

```csharp
public static PrintHtmlContentResponse Print(SystemPrinter<SystemPrinter.IHtmlSettings> printer)
```

##### Parameters

`printer` [SystemPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_1)<[SystemPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter).[IHtmlSettings](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_IHtmlSettings)\>

The printer to use.

##### Returns

 [PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintHtmlContentResponse)

The <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Print_Handlers_PrintHtmlContentResponse_Print_DotNetBrowser_Print_PdfPrinter_DotNetBrowser_Print_PdfPrinter_IHtmlSettings__"></a> Print\(PdfPrinter<IHtmlSettings\>\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to proceed with the passed printer.

```csharp
public static PrintHtmlContentResponse Print(PdfPrinter<PdfPrinter.IHtmlSettings> printer)
```

##### Parameters

`printer` [PdfPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_1)<[PdfPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter).[IHtmlSettings](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_IHtmlSettings)\>

The printer to use.

##### Returns

 [PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintHtmlContentResponse)

The <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

## <a id="DotNetBrowser_Print_Handlers_PrintPdfContentParameters"></a> Class PrintPdfContentParameters

Namespace: [DotNetBrowser.Print.Handlers](DotNetBrowser.Print.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class PrintPdfContentParameters : PrintContentParameters<SystemPrinter.IPdfSettings, PdfPrinter.IPdfSettings>
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintContentParameters<SystemPrinter.IPdfSettings, PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintContentParameters_2) ← 
[PrintPdfContentParameters](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintPdfContentParameters)

##### Inherited Members

[PrintContentParameters<SystemPrinter.IPdfSettings, PdfPrinter.IPdfSettings\>.Browser](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintContentParameters_2_Browser), 
[PrintContentParameters<SystemPrinter.IPdfSettings, PdfPrinter.IPdfSettings\>.Printers](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintContentParameters_2_Printers), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Print_Handlers_PrintPdfContentResponse"></a> Class PrintPdfContentResponse

Namespace: [DotNetBrowser.Print.Handlers](DotNetBrowser.Print.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class PrintPdfContentResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintPdfContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintPdfContentResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Print_Handlers_PrintPdfContentResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to cancel printing.

```csharp
public static PrintPdfContentResponse Cancel()
```

##### Returns

 [PrintPdfContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintPdfContentResponse)

The <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Print_Handlers_PrintPdfContentResponse_Print_DotNetBrowser_Print_SystemPrinter_DotNetBrowser_Print_SystemPrinter_IPdfSettings__"></a> Print\(SystemPrinter<IPdfSettings\>\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to proceed with the passed printer.

```csharp
public static PrintPdfContentResponse Print(SystemPrinter<SystemPrinter.IPdfSettings> printer)
```

##### Parameters

`printer` [SystemPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_1)<[SystemPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter).[IPdfSettings](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_IPdfSettings)\>

The printer to use.

##### Returns

 [PrintPdfContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintPdfContentResponse)

The <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Print_Handlers_PrintPdfContentResponse_Print_DotNetBrowser_Print_PdfPrinter_DotNetBrowser_Print_PdfPrinter_IPdfSettings__"></a> Print\(PdfPrinter<IPdfSettings\>\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to proceed with the passed printer.

```csharp
public static PrintPdfContentResponse Print(PdfPrinter<PdfPrinter.IPdfSettings> printer)
```

##### Parameters

`printer` [PdfPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_1)<[PdfPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter).[IPdfSettings](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_IPdfSettings)\>

The printer to use.

##### Returns

 [PrintPdfContentResponse](DotNetBrowser.Print.Handlers.md#DotNetBrowser_Print_Handlers_PrintPdfContentResponse)

The <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref> implementation.
