# <a id="DotNetBrowser_Print_SystemPrinter_IHtmlSettings"></a> Interface SystemPrinter.IHtmlSettings

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

Print settings available when printing HTML content on a physical printer.

```csharp
public interface SystemPrinter.IHtmlSettings : SystemPrinter.ISettings<SystemPrinter.IHtmlSettings>, IPrintSettings, ICollate<SystemPrinter.IHtmlSettings>, IColorModel<SystemPrinter.IHtmlSettings>, ICopies<SystemPrinter.IHtmlSettings>, IDuplexMode<SystemPrinter.IHtmlSettings>, IPageRanges<SystemPrinter.IHtmlSettings>, IPagesPerSheet<SystemPrinter.IHtmlSettings>, IPaperSize<SystemPrinter.IHtmlSettings>, IScaling<SystemPrinter.IHtmlSettings>, IPageMargins<SystemPrinter.IHtmlSettings>, IPrintHeaderFooter<SystemPrinter.IHtmlSettings>, IOrientation<SystemPrinter.IHtmlSettings>, IPrintBackgrounds<SystemPrinter.IHtmlSettings>, IPrintSelectionOnly<SystemPrinter.IHtmlSettings>, IHeaderTemplate<SystemPrinter.IHtmlSettings>, IFooterTemplate<SystemPrinter.IHtmlSettings>
```

#### Implements

[SystemPrinter.ISettings<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.SystemPrinter.ISettings\-1.md), 
[IPrintSettings](DotNetBrowser.Print.Settings.IPrintSettings.md), 
[ICollate<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.ICollate\-1.md), 
[IColorModel<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IColorModel\-1.md), 
[ICopies<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.ICopies\-1.md), 
[IDuplexMode<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IDuplexMode\-1.md), 
[IPageRanges<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPageRanges\-1.md), 
[IPagesPerSheet<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPagesPerSheet\-1.md), 
[IPaperSize<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPaperSize\-1.md), 
[IScaling<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IScaling\-1.md), 
[IPageMargins<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPageMargins\-1.md), 
[IPrintHeaderFooter<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPrintHeaderFooter\-1.md), 
[IOrientation<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IOrientation\-1.md), 
[IPrintBackgrounds<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPrintBackgrounds\-1.md), 
[IPrintSelectionOnly<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IPrintSelectionOnly\-1.md), 
[IHeaderTemplate<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IHeaderTemplate\-1.md), 
[IFooterTemplate<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.IFooterTemplate\-1.md)

#### Extension Methods

[PrintSettingsExtensions.Apply<SystemPrinter.IHtmlSettings\>\(SystemPrinter.IHtmlSettings, Action<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintSettingsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSettingsExtensions\_Apply\_\_1\_\_\_0\_System\_Action\_\_\_0\_\_), 
[CollateExtensions.DisableCollatePrinting<SystemPrinter.IHtmlSettings\>\(ICollate<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.CollateExtensions.md\#DotNetBrowser\_Print\_Settings\_CollateExtensions\_DisableCollatePrinting\_\_1\_DotNetBrowser\_Print\_Settings\_ICollate\_\_\_0\_\_), 
[PrintBackgroundsExtensions.DisablePrintingBackgrounds<SystemPrinter.IHtmlSettings\>\(IPrintBackgrounds<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintBackgroundsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintBackgroundsExtensions\_DisablePrintingBackgrounds\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintBackgrounds\_\_\_0\_\_), 
[PrintHeaderFooterExtensions.DisablePrintingHeaderFooter<SystemPrinter.IHtmlSettings\>\(IPrintHeaderFooter<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintHeaderFooterExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintHeaderFooterExtensions\_DisablePrintingHeaderFooter\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintHeaderFooter\_\_\_0\_\_), 
[PrintSelectionOnlyExtensions.DisablePrintingSelectionOnly<SystemPrinter.IHtmlSettings\>\(IPrintSelectionOnly<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintSelectionOnlyExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSelectionOnlyExtensions\_DisablePrintingSelectionOnly\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintSelectionOnly\_\_\_0\_\_), 
[CollateExtensions.EnableCollatePrinting<SystemPrinter.IHtmlSettings\>\(ICollate<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.CollateExtensions.md\#DotNetBrowser\_Print\_Settings\_CollateExtensions\_EnableCollatePrinting\_\_1\_DotNetBrowser\_Print\_Settings\_ICollate\_\_\_0\_\_), 
[PrintBackgroundsExtensions.EnablePrintingBackgrounds<SystemPrinter.IHtmlSettings\>\(IPrintBackgrounds<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintBackgroundsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintBackgroundsExtensions\_EnablePrintingBackgrounds\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintBackgrounds\_\_\_0\_\_), 
[PrintHeaderFooterExtensions.EnablePrintingHeaderFooter<SystemPrinter.IHtmlSettings\>\(IPrintHeaderFooter<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintHeaderFooterExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintHeaderFooterExtensions\_EnablePrintingHeaderFooter\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintHeaderFooter\_\_\_0\_\_), 
[PrintSelectionOnlyExtensions.EnablePrintingSelectionOnly<SystemPrinter.IHtmlSettings\>\(IPrintSelectionOnly<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.PrintSelectionOnlyExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSelectionOnlyExtensions\_EnablePrintingSelectionOnly\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintSelectionOnly\_\_\_0\_\_), 
[ColorModelExtensions.SetColorModel<SystemPrinter.IHtmlSettings\>\(IColorModel<SystemPrinter.IHtmlSettings\>, ColorModel\)](DotNetBrowser.Print.Settings.ColorModelExtensions.md\#DotNetBrowser\_Print\_Settings\_ColorModelExtensions\_SetColorModel\_\_1\_DotNetBrowser\_Print\_Settings\_IColorModel\_\_\_0\_\_DotNetBrowser\_Print\_ColorModel\_), 
[CopiesExtensions.SetCopies<SystemPrinter.IHtmlSettings\>\(ICopies<SystemPrinter.IHtmlSettings\>, int\)](DotNetBrowser.Print.Settings.CopiesExtensions.md\#DotNetBrowser\_Print\_Settings\_CopiesExtensions\_SetCopies\_\_1\_DotNetBrowser\_Print\_Settings\_ICopies\_\_\_0\_\_System\_Int32\_), 
[DuplexModeExtensions.SetDuplexMode<SystemPrinter.IHtmlSettings\>\(IDuplexMode<SystemPrinter.IHtmlSettings\>, DuplexMode\)](DotNetBrowser.Print.Settings.DuplexModeExtensions.md\#DotNetBrowser\_Print\_Settings\_DuplexModeExtensions\_SetDuplexMode\_\_1\_DotNetBrowser\_Print\_Settings\_IDuplexMode\_\_\_0\_\_DotNetBrowser\_Print\_DuplexMode\_), 
[FooterTemplateExtensions.SetFooterTemplate<SystemPrinter.IHtmlSettings\>\(IFooterTemplate<SystemPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.FooterTemplateExtensions.md\#DotNetBrowser\_Print\_Settings\_FooterTemplateExtensions\_SetFooterTemplate\_\_1\_DotNetBrowser\_Print\_Settings\_IFooterTemplate\_\_\_0\_\_System\_String\_), 
[HeaderTemplateExtensions.SetHeaderTemplate<SystemPrinter.IHtmlSettings\>\(IHeaderTemplate<SystemPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.HeaderTemplateExtensions.md\#DotNetBrowser\_Print\_Settings\_HeaderTemplateExtensions\_SetHeaderTemplate\_\_1\_DotNetBrowser\_Print\_Settings\_IHeaderTemplate\_\_\_0\_\_System\_String\_), 
[OrientationExtensions.SetOrientation<SystemPrinter.IHtmlSettings\>\(IOrientation<SystemPrinter.IHtmlSettings\>, Orientation\)](DotNetBrowser.Print.Settings.OrientationExtensions.md\#DotNetBrowser\_Print\_Settings\_OrientationExtensions\_SetOrientation\_\_1\_DotNetBrowser\_Print\_Settings\_IOrientation\_\_\_0\_\_DotNetBrowser\_Print\_Orientation\_), 
[PageMarginsExtensions.SetPageMargins<SystemPrinter.IHtmlSettings\>\(IPageMargins<SystemPrinter.IHtmlSettings\>, PageMargins\)](DotNetBrowser.Print.Settings.PageMarginsExtensions.md\#DotNetBrowser\_Print\_Settings\_PageMarginsExtensions\_SetPageMargins\_\_1\_DotNetBrowser\_Print\_Settings\_IPageMargins\_\_\_0\_\_DotNetBrowser\_Print\_PageMargins\_), 
[PageRangesExtensions.SetPageRanges<SystemPrinter.IHtmlSettings\>\(IPageRanges<SystemPrinter.IHtmlSettings\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.PageRangesExtensions.md\#DotNetBrowser\_Print\_Settings\_PageRangesExtensions\_SetPageRanges\_\_1\_DotNetBrowser\_Print\_Settings\_IPageRanges\_\_\_0\_\_System\_Collections\_Generic\_IReadOnlyCollection\_DotNetBrowser\_Print\_PageRange\_\_), 
[PagesPerSheetExtensions.SetPagesPerSheet<SystemPrinter.IHtmlSettings\>\(IPagesPerSheet<SystemPrinter.IHtmlSettings\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.PagesPerSheetExtensions.md\#DotNetBrowser\_Print\_Settings\_PagesPerSheetExtensions\_SetPagesPerSheet\_\_1\_DotNetBrowser\_Print\_Settings\_IPagesPerSheet\_\_\_0\_\_DotNetBrowser\_Print\_PagesPerSheet\_), 
[PaperSizeExtensions.SetPaperSize<SystemPrinter.IHtmlSettings\>\(IPaperSize<SystemPrinter.IHtmlSettings\>, PaperSize\)](DotNetBrowser.Print.Settings.PaperSizeExtensions.md\#DotNetBrowser\_Print\_Settings\_PaperSizeExtensions\_SetPaperSize\_\_1\_DotNetBrowser\_Print\_Settings\_IPaperSize\_\_\_0\_\_DotNetBrowser\_Print\_PaperSize\_), 
[ScalingExtensions.SetScaling<SystemPrinter.IHtmlSettings\>\(IScaling<SystemPrinter.IHtmlSettings\>, Scaling\)](DotNetBrowser.Print.Settings.ScalingExtensions.md\#DotNetBrowser\_Print\_Settings\_ScalingExtensions\_SetScaling\_\_1\_DotNetBrowser\_Print\_Settings\_IScaling\_\_\_0\_\_DotNetBrowser\_Print\_Scaling\_)

