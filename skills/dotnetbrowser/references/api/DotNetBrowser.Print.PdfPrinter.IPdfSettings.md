# <a id="DotNetBrowser_Print_PdfPrinter_IPdfSettings"></a> Interface PdfPrinter.IPdfSettings

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The print settings available when printing PDF content on the PDF printer.

```csharp
public interface PdfPrinter.IPdfSettings : PdfPrinter.ISettings<PdfPrinter.IPdfSettings>, IPrintSettings, IPageRanges<PdfPrinter.IPdfSettings>, IPagesPerSheet<PdfPrinter.IPdfSettings>, IPdfFilePath<PdfPrinter.IPdfSettings>, IScaling<PdfPrinter.IPdfSettings>
```

#### Implements

[PdfPrinter.ISettings<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.PdfPrinter.ISettings\-1.md), 
[IPrintSettings](DotNetBrowser.Print.Settings.IPrintSettings.md), 
[IPageRanges<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IPageRanges\-1.md), 
[IPagesPerSheet<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IPagesPerSheet\-1.md), 
[IPdfFilePath<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IPdfFilePath\-1.md), 
[IScaling<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IScaling\-1.md)

#### Extension Methods

[PrintSettingsExtensions.Apply<PdfPrinter.IPdfSettings\>\(PdfPrinter.IPdfSettings, Action<PdfPrinter.IPdfSettings\>\)](DotNetBrowser.Print.Settings.PrintSettingsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSettingsExtensions\_Apply\_\_1\_\_\_0\_System\_Action\_\_\_0\_\_), 
[PageRangesExtensions.SetPageRanges<PdfPrinter.IPdfSettings\>\(IPageRanges<PdfPrinter.IPdfSettings\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.PageRangesExtensions.md\#DotNetBrowser\_Print\_Settings\_PageRangesExtensions\_SetPageRanges\_\_1\_DotNetBrowser\_Print\_Settings\_IPageRanges\_\_\_0\_\_System\_Collections\_Generic\_IReadOnlyCollection\_DotNetBrowser\_Print\_PageRange\_\_), 
[PagesPerSheetExtensions.SetPagesPerSheet<PdfPrinter.IPdfSettings\>\(IPagesPerSheet<PdfPrinter.IPdfSettings\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.PagesPerSheetExtensions.md\#DotNetBrowser\_Print\_Settings\_PagesPerSheetExtensions\_SetPagesPerSheet\_\_1\_DotNetBrowser\_Print\_Settings\_IPagesPerSheet\_\_\_0\_\_DotNetBrowser\_Print\_PagesPerSheet\_), 
[PdfFilePathExtensions.SetPdfFilePath<PdfPrinter.IPdfSettings\>\(IPdfFilePath<PdfPrinter.IPdfSettings\>, string\)](DotNetBrowser.Print.Settings.PdfFilePathExtensions.md\#DotNetBrowser\_Print\_Settings\_PdfFilePathExtensions\_SetPdfFilePath\_\_1\_DotNetBrowser\_Print\_Settings\_IPdfFilePath\_\_\_0\_\_System\_String\_), 
[ScalingExtensions.SetScaling<PdfPrinter.IPdfSettings\>\(IScaling<PdfPrinter.IPdfSettings\>, Scaling\)](DotNetBrowser.Print.Settings.ScalingExtensions.md\#DotNetBrowser\_Print\_Settings\_ScalingExtensions\_SetScaling\_\_1\_DotNetBrowser\_Print\_Settings\_IScaling\_\_\_0\_\_DotNetBrowser\_Print\_Scaling\_)

