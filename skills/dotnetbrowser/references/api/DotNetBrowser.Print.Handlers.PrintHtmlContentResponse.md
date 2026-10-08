# <a id="DotNetBrowser_Print_Handlers_PrintHtmlContentResponse"></a> Class PrintHtmlContentResponse

Namespace: [DotNetBrowser.Print.Handlers](DotNetBrowser.Print.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class PrintHtmlContentResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Handlers_PrintHtmlContentResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to cancel printing.

```csharp
public static PrintHtmlContentResponse Cancel()
```

#### Returns

 [PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.md)

The <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Print_Handlers_PrintHtmlContentResponse_Print_DotNetBrowser_Print_SystemPrinter_DotNetBrowser_Print_SystemPrinter_IHtmlSettings__"></a> Print\(SystemPrinter<IHtmlSettings\>\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to proceed with the passed printer.

```csharp
public static PrintHtmlContentResponse Print(SystemPrinter<SystemPrinter.IHtmlSettings> printer)
```

#### Parameters

`printer` [SystemPrinter](DotNetBrowser.Print.SystemPrinter\-1.md)<[SystemPrinter](DotNetBrowser.Print.SystemPrinter.md).[IHtmlSettings](DotNetBrowser.Print.SystemPrinter.IHtmlSettings.md)\>

The printer to use.

#### Returns

 [PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.md)

The <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Print_Handlers_PrintHtmlContentResponse_Print_DotNetBrowser_Print_PdfPrinter_DotNetBrowser_Print_PdfPrinter_IHtmlSettings__"></a> Print\(PdfPrinter<IHtmlSettings\>\)

Creates a <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that
tells the Chromium engine to proceed with the passed printer.

```csharp
public static PrintHtmlContentResponse Print(PdfPrinter<PdfPrinter.IHtmlSettings> printer)
```

#### Parameters

`printer` [PdfPrinter](DotNetBrowser.Print.PdfPrinter\-1.md)<[PdfPrinter](DotNetBrowser.Print.PdfPrinter.md).[IHtmlSettings](DotNetBrowser.Print.PdfPrinter.IHtmlSettings.md)\>

The printer to use.

#### Returns

 [PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.md)

The <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> implementation.

