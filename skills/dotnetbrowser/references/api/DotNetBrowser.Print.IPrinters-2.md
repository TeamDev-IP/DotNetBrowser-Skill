# <a id="DotNetBrowser_Print_IPrinters_2"></a> Interface IPrinters<TPrintSettings, TPdfPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The collection of the available printers.

```csharp
public interface IPrinters<TPrintSettings, TPdfPrintSettings> : IReadOnlyList<SystemPrinter<TPrintSettings>>, IReadOnlyCollection<SystemPrinter<TPrintSettings>>, IEnumerable<SystemPrinter<TPrintSettings>>, IEnumerable where TPrintSettings : class, SystemPrinter.ISettings<TPrintSettings> where TPdfPrintSettings : class, PdfPrinter.ISettings<TPdfPrintSettings>
```

#### Type Parameters

`TPrintSettings` 

The print settings type available for these printers.

`TPdfPrintSettings` 

The PDF print settings type available for PDF printer.

#### Implements

[IReadOnlyList<SystemPrinter<TPrintSettings\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1), 
[IReadOnlyCollection<SystemPrinter<TPrintSettings\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1), 
[IEnumerable<SystemPrinter<TPrintSettings\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1), 
[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.ienumerable)

## Properties

### <a id="DotNetBrowser_Print_IPrinters_2_Default"></a> Default

Gets the default system printer.

```csharp
SystemPrinter<TPrintSettings> Default { get; }
```

#### Property Value

 [SystemPrinter](DotNetBrowser.Print.SystemPrinter\-1.md)<TPrintSettings\>

### <a id="DotNetBrowser_Print_IPrinters_2_Pdf"></a> Pdf

Gets the <xref href="DotNetBrowser.Print.PdfPrinter" data-throw-if-not-resolved="false"></xref> instance that allows you to print to PDF.

```csharp
PdfPrinter<TPdfPrintSettings> Pdf { get; }
```

#### Property Value

 [PdfPrinter](DotNetBrowser.Print.PdfPrinter\-1.md)<TPdfPrintSettings\>

