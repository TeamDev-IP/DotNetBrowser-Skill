# <a id="DotNetBrowser_Print_PdfPrinter_IHtmlSettings"></a> Interface PdfPrinter.IHtmlSettings

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The print settings available when printing HTML content on the PDF printer.

```csharp
public interface PdfPrinter.IHtmlSettings : PdfPrinter.ISettings<PdfPrinter.IHtmlSettings>, IPrintSettings, IPageRanges<PdfPrinter.IHtmlSettings>, IPagesPerSheet<PdfPrinter.IHtmlSettings>, IPdfFilePath<PdfPrinter.IHtmlSettings>, IScaling<PdfPrinter.IHtmlSettings>, IPageMargins<PdfPrinter.IHtmlSettings>, IPrintHeaderFooter<PdfPrinter.IHtmlSettings>, IOrientation<PdfPrinter.IHtmlSettings>, IPrintBackgrounds<PdfPrinter.IHtmlSettings>, IPrintSelectionOnly<PdfPrinter.IHtmlSettings>, IPaperSize<PdfPrinter.IHtmlSettings>, IHeaderTemplate<PdfPrinter.IHtmlSettings>, IFooterTemplate<PdfPrinter.IHtmlSettings>
```

#### Implements

[PdfPrinter.ISettings<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.PdfPrinter.ISettings\-1.md), 
[IPrintSettings](DotNetBrowser.Print.Settings.IPrintSettings.md), 
[IPageRanges<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPageRanges\-1.md), 
[IPagesPerSheet<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPagesPerSheet\-1.md), 
[IPdfFilePath<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPdfFilePath\-1.md), 
[IScaling<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IScaling\-1.md), 
[IPageMargins<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPageMargins\-1.md), 
[IPrintHeaderFooter<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPrintHeaderFooter\-1.md), 
[IOrientation<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IOrientation\-1.md), 
[IPrintBackgrounds<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPrintBackgrounds\-1.md), 
[IPrintSelectionOnly<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPrintSelectionOnly\-1.md), 
[IPaperSize<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPaperSize\-1.md), 
[IHeaderTemplate<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IHeaderTemplate\-1.md), 
[IFooterTemplate<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IFooterTemplate\-1.md)

#### Extension Methods

[PrintSettingsExtensions.Apply<PdfPrinter.IHtmlSettings\>\(PdfPrinter.IHtmlSettings, Action<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintSettingsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSettingsExtensions\_Apply\_\_1\_\_\_0\_System\_Action\_\_\_0\_\_), 
[PrintBackgroundsExtensions.DisablePrintingBackgrounds<PdfPrinter.IHtmlSettings\>\(IPrintBackgrounds<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintBackgroundsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintBackgroundsExtensions\_DisablePrintingBackgrounds\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintBackgrounds\_\_\_0\_\_), 
[PrintHeaderFooterExtensions.DisablePrintingHeaderFooter<PdfPrinter.IHtmlSettings\>\(IPrintHeaderFooter<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintHeaderFooterExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintHeaderFooterExtensions\_DisablePrintingHeaderFooter\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintHeaderFooter\_\_\_0\_\_), 
[PrintSelectionOnlyExtensions.DisablePrintingSelectionOnly<PdfPrinter.IHtmlSettings\>\(IPrintSelectionOnly<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintSelectionOnlyExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSelectionOnlyExtensions\_DisablePrintingSelectionOnly\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintSelectionOnly\_\_\_0\_\_), 
[PrintBackgroundsExtensions.EnablePrintingBackgrounds<PdfPrinter.IHtmlSettings\>\(IPrintBackgrounds<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintBackgroundsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintBackgroundsExtensions\_EnablePrintingBackgrounds\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintBackgrounds\_\_\_0\_\_), 
[PrintHeaderFooterExtensions.EnablePrintingHeaderFooter<PdfPrinter.IHtmlSettings\>\(IPrintHeaderFooter<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintHeaderFooterExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintHeaderFooterExtensions\_EnablePrintingHeaderFooter\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintHeaderFooter\_\_\_0\_\_), 
[PrintSelectionOnlyExtensions.EnablePrintingSelectionOnly<PdfPrinter.IHtmlSettings\>\(IPrintSelectionOnly<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintSelectionOnlyExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSelectionOnlyExtensions\_EnablePrintingSelectionOnly\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintSelectionOnly\_\_\_0\_\_), 
[FooterTemplateExtensions.SetFooterTemplate<PdfPrinter.IHtmlSettings\>\(IFooterTemplate<PdfPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.FooterTemplateExtensions.md\#DotNetBrowser\_Print\_Settings\_FooterTemplateExtensions\_SetFooterTemplate\_\_1\_DotNetBrowser\_Print\_Settings\_IFooterTemplate\_\_\_0\_\_System\_String\_), 
[HeaderTemplateExtensions.SetHeaderTemplate<PdfPrinter.IHtmlSettings\>\(IHeaderTemplate<PdfPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.HeaderTemplateExtensions.md\#DotNetBrowser\_Print\_Settings\_HeaderTemplateExtensions\_SetHeaderTemplate\_\_1\_DotNetBrowser\_Print\_Settings\_IHeaderTemplate\_\_\_0\_\_System\_String\_), 
[OrientationExtensions.SetOrientation<PdfPrinter.IHtmlSettings\>\(IOrientation<PdfPrinter.IHtmlSettings\>, Orientation\)](DotNetBrowser.Print.Settings.OrientationExtensions.md\#DotNetBrowser\_Print\_Settings\_OrientationExtensions\_SetOrientation\_\_1\_DotNetBrowser\_Print\_Settings\_IOrientation\_\_\_0\_\_DotNetBrowser\_Print\_Orientation\_), 
[PageMarginsExtensions.SetPageMargins<PdfPrinter.IHtmlSettings\>\(IPageMargins<PdfPrinter.IHtmlSettings\>, PageMargins\)](DotNetBrowser.Print.Settings.PageMarginsExtensions.md\#DotNetBrowser\_Print\_Settings\_PageMarginsExtensions\_SetPageMargins\_\_1\_DotNetBrowser\_Print\_Settings\_IPageMargins\_\_\_0\_\_DotNetBrowser\_Print\_PageMargins\_), 
[PageRangesExtensions.SetPageRanges<PdfPrinter.IHtmlSettings\>\(IPageRanges<PdfPrinter.IHtmlSettings\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.PageRangesExtensions.md\#DotNetBrowser\_Print\_Settings\_PageRangesExtensions\_SetPageRanges\_\_1\_DotNetBrowser\_Print\_Settings\_IPageRanges\_\_\_0\_\_System\_Collections\_Generic\_IReadOnlyCollection\_DotNetBrowser\_Print\_PageRange\_\_), 
[PagesPerSheetExtensions.SetPagesPerSheet<PdfPrinter.IHtmlSettings\>\(IPagesPerSheet<PdfPrinter.IHtmlSettings\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.PagesPerSheetExtensions.md\#DotNetBrowser\_Print\_Settings\_PagesPerSheetExtensions\_SetPagesPerSheet\_\_1\_DotNetBrowser\_Print\_Settings\_IPagesPerSheet\_\_\_0\_\_DotNetBrowser\_Print\_PagesPerSheet\_), 
[PaperSizeExtensions.SetPaperSize<PdfPrinter.IHtmlSettings\>\(IPaperSize<PdfPrinter.IHtmlSettings\>, PaperSize\)](DotNetBrowser.Print.Settings.PaperSizeExtensions.md\#DotNetBrowser\_Print\_Settings\_PaperSizeExtensions\_SetPaperSize\_\_1\_DotNetBrowser\_Print\_Settings\_IPaperSize\_\_\_0\_\_DotNetBrowser\_Print\_PaperSize\_), 
[PdfFilePathExtensions.SetPdfFilePath<PdfPrinter.IHtmlSettings\>\(IPdfFilePath<PdfPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.PdfFilePathExtensions.md\#DotNetBrowser\_Print\_Settings\_PdfFilePathExtensions\_SetPdfFilePath\_\_1\_DotNetBrowser\_Print\_Settings\_IPdfFilePath\_\_\_0\_\_System\_String\_), 
[ScalingExtensions.SetScaling<PdfPrinter.IHtmlSettings\>\(IScaling<PdfPrinter.IHtmlSettings\>, Scaling\)](DotNetBrowser.Print.Settings.ScalingExtensions.md\#DotNetBrowser\_Print\_Settings\_ScalingExtensions\_SetScaling\_\_1\_DotNetBrowser\_Print\_Settings\_IScaling\_\_\_0\_\_DotNetBrowser\_Print\_Scaling\_)

