# <a id="DotNetBrowser_Print_Handlers_PrintPdfContentResponse"></a> Class PrintPdfContentResponse

Namespace: [DotNetBrowser.Print.Handlers](DotNetBrowser.Print.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class PrintPdfContentResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintPdfContentResponse](DotNetBrowser.Print.Handlers.PrintPdfContentResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Handlers_PrintPdfContentResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to cancel printing.

```csharp
public static PrintPdfContentResponse Cancel()
```

#### Returns

 [PrintPdfContentResponse](DotNetBrowser.Print.Handlers.PrintPdfContentResponse.md)

The <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Print_Handlers_PrintPdfContentResponse_Print_DotNetBrowser_Print_SystemPrinter_DotNetBrowser_Print_SystemPrinter_IPdfSettings__"></a> Print\(SystemPrinter<IPdfSettings\>\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to proceed with the passed printer.

```csharp
public static PrintPdfContentResponse Print(SystemPrinter<SystemPrinter.IPdfSettings> printer)
```

#### Parameters

`printer` [SystemPrinter](DotNetBrowser.Print.SystemPrinter\-1.md)<[SystemPrinter](DotNetBrowser.Print.SystemPrinter.md).[IPdfSettings](DotNetBrowser.Print.SystemPrinter.IPdfSettings.md)\>

The printer to use.

#### Returns

 [PrintPdfContentResponse](DotNetBrowser.Print.Handlers.PrintPdfContentResponse.md)

The <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Print_Handlers_PrintPdfContentResponse_Print_DotNetBrowser_Print_PdfPrinter_DotNetBrowser_Print_PdfPrinter_IPdfSettings__"></a> Print\(PdfPrinter<IPdfSettings\>\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to proceed with the passed printer.

```csharp
public static PrintPdfContentResponse Print(PdfPrinter<PdfPrinter.IPdfSettings> printer)
```

#### Parameters

`printer` [PdfPrinter](DotNetBrowser.Print.PdfPrinter\-1.md)<[PdfPrinter](DotNetBrowser.Print.PdfPrinter.md).[IPdfSettings](DotNetBrowser.Print.PdfPrinter.IPdfSettings.md)\>

The printer to use.

#### Returns

 [PrintPdfContentResponse](DotNetBrowser.Print.Handlers.PrintPdfContentResponse.md)

The <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

