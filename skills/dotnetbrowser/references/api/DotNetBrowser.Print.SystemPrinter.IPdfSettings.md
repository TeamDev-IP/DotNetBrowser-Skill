# <a id="DotNetBrowser_Print_SystemPrinter_IPdfSettings"></a> Interface SystemPrinter.IPdfSettings

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

Print settings available when printing PDF content on a physical printer.

```csharp
public interface SystemPrinter.IPdfSettings : SystemPrinter.ISettings<SystemPrinter.IPdfSettings>, IPrintSettings, ICollate<SystemPrinter.IPdfSettings>, IColorModel<SystemPrinter.IPdfSettings>, ICopies<SystemPrinter.IPdfSettings>, IDuplexMode<SystemPrinter.IPdfSettings>, IPageRanges<SystemPrinter.IPdfSettings>, IPagesPerSheet<SystemPrinter.IPdfSettings>, IPaperSize<SystemPrinter.IPdfSettings>, IScaling<SystemPrinter.IPdfSettings>, IFit<SystemPrinter.IPdfSettings>
```

#### Implements

[SystemPrinter.ISettings<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.SystemPrinter.ISettings\-1.md), 
[IPrintSettings](DotNetBrowser.Print.Settings.IPrintSettings.md), 
[ICollate<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.ICollate\-1.md), 
[IColorModel<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IColorModel\-1.md), 
[ICopies<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.ICopies\-1.md), 
[IDuplexMode<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IDuplexMode\-1.md), 
[IPageRanges<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IPageRanges\-1.md), 
[IPagesPerSheet<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IPagesPerSheet\-1.md), 
[IPaperSize<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IPaperSize\-1.md), 
[IScaling<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IScaling\-1.md), 
[IFit<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.IFit\-1.md)

#### Extension Methods

[PrintSettingsExtensions.Apply<SystemPrinter.IPdfSettings\>\(SystemPrinter.IPdfSettings, Action<SystemPrinter.IPdfSettings\>\)](DotNetBrowser.Print.Settings.PrintSettingsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSettingsExtensions\_Apply\_\_1\_\_\_0\_System\_Action\_\_\_0\_\_), 
[CollateExtensions.DisableCollatePrinting<SystemPrinter.IPdfSettings\>\(ICollate<SystemPrinter.IPdfSettings\>\)](DotNetBrowser.Print.Settings.CollateExtensions.md\#DotNetBrowser\_Print\_Settings\_CollateExtensions\_DisableCollatePrinting\_\_1\_DotNetBrowser\_Print\_Settings\_ICollate\_\_\_0\_\_), 
[CollateExtensions.EnableCollatePrinting<SystemPrinter.IPdfSettings\>\(ICollate<SystemPrinter.IPdfSettings\>\)](DotNetBrowser.Print.Settings.CollateExtensions.md\#DotNetBrowser\_Print\_Settings\_CollateExtensions\_EnableCollatePrinting\_\_1\_DotNetBrowser\_Print\_Settings\_ICollate\_\_\_0\_\_), 
[ColorModelExtensions.SetColorModel<SystemPrinter.IPdfSettings\>\(IColorModel<SystemPrinter.IPdfSettings\>, ColorModel\)](DotNetBrowser.Print.Settings.ColorModelExtensions.md\#DotNetBrowser\_Print\_Settings\_ColorModelExtensions\_SetColorModel\_\_1\_DotNetBrowser\_Print\_Settings\_IColorModel\_\_\_0\_\_DotNetBrowser\_Print\_ColorModel\_), 
[CopiesExtensions.SetCopies<SystemPrinter.IPdfSettings\>\(ICopies<SystemPrinter.IPdfSettings\>, int\)](DotNetBrowser.Print.Settings.CopiesExtensions.md\#DotNetBrowser\_Print\_Settings\_CopiesExtensions\_SetCopies\_\_1\_DotNetBrowser\_Print\_Settings\_ICopies\_\_\_0\_\_System\_Int32\_), 
[DuplexModeExtensions.SetDuplexMode<SystemPrinter.IPdfSettings\>\(IDuplexMode<SystemPrinter.IPdfSettings\>, DuplexMode\)](DotNetBrowser.Print.Settings.DuplexModeExtensions.md\#DotNetBrowser\_Print\_Settings\_DuplexModeExtensions\_SetDuplexMode\_\_1\_DotNetBrowser\_Print\_Settings\_IDuplexMode\_\_\_0\_\_DotNetBrowser\_Print\_DuplexMode\_), 
[FitExtensions.SetFit<SystemPrinter.IPdfSettings\>\(IFit<SystemPrinter.IPdfSettings\>, Fit\)](DotNetBrowser.Print.Settings.FitExtensions.md\#DotNetBrowser\_Print\_Settings\_FitExtensions\_SetFit\_\_1\_DotNetBrowser\_Print\_Settings\_IFit\_\_\_0\_\_DotNetBrowser\_Print\_Fit\_), 
[PageRangesExtensions.SetPageRanges<SystemPrinter.IPdfSettings\>\(IPageRanges<SystemPrinter.IPdfSettings\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.PageRangesExtensions.md\#DotNetBrowser\_Print\_Settings\_PageRangesExtensions\_SetPageRanges\_\_1\_DotNetBrowser\_Print\_Settings\_IPageRanges\_\_\_0\_\_System\_Collections\_Generic\_IReadOnlyCollection\_DotNetBrowser\_Print\_PageRange\_\_), 
[PagesPerSheetExtensions.SetPagesPerSheet<SystemPrinter.IPdfSettings\>\(IPagesPerSheet<SystemPrinter.IPdfSettings\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.PagesPerSheetExtensions.md\#DotNetBrowser\_Print\_Settings\_PagesPerSheetExtensions\_SetPagesPerSheet\_\_1\_DotNetBrowser\_Print\_Settings\_IPagesPerSheet\_\_\_0\_\_DotNetBrowser\_Print\_PagesPerSheet\_), 
[PaperSizeExtensions.SetPaperSize<SystemPrinter.IPdfSettings\>\(IPaperSize<SystemPrinter.IPdfSettings\>, PaperSize\)](DotNetBrowser.Print.Settings.PaperSizeExtensions.md\#DotNetBrowser\_Print\_Settings\_PaperSizeExtensions\_SetPaperSize\_\_1\_DotNetBrowser\_Print\_Settings\_IPaperSize\_\_\_0\_\_DotNetBrowser\_Print\_PaperSize\_), 
[ScalingExtensions.SetScaling<SystemPrinter.IPdfSettings\>\(IScaling<SystemPrinter.IPdfSettings\>, Scaling\)](DotNetBrowser.Print.Settings.ScalingExtensions.md\#DotNetBrowser\_Print\_Settings\_ScalingExtensions\_SetScaling\_\_1\_DotNetBrowser\_Print\_Settings\_IScaling\_\_\_0\_\_DotNetBrowser\_Print\_Scaling\_)

