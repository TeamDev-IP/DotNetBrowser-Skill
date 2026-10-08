# <a id="DotNetBrowser_Print_SystemPrinter_ISettings_1"></a> Interface SystemPrinter.ISettings<T\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

Print settings available when printing HTML or PDF content on a physical printer.

```csharp
public interface SystemPrinter.ISettings<out T> : IPrintSettings, ICollate<T>, IColorModel<T>, ICopies<T>, IDuplexMode<T>, IPageRanges<T>, IPagesPerSheet<T>, IPaperSize<T>, IScaling<T> where T : class, IPrintSettings
```

#### Type Parameters

`T` 

The specific print settings type.

#### Implements

[IPrintSettings](DotNetBrowser.Print.Settings.IPrintSettings.md), 
[ICollate<T\>](DotNetBrowser.Print.Settings.ICollate\-1.md), 
[IColorModel<T\>](DotNetBrowser.Print.Settings.IColorModel\-1.md), 
[ICopies<T\>](DotNetBrowser.Print.Settings.ICopies\-1.md), 
[IDuplexMode<T\>](DotNetBrowser.Print.Settings.IDuplexMode\-1.md), 
[IPageRanges<T\>](DotNetBrowser.Print.Settings.IPageRanges\-1.md), 
[IPagesPerSheet<T\>](DotNetBrowser.Print.Settings.IPagesPerSheet\-1.md), 
[IPaperSize<T\>](DotNetBrowser.Print.Settings.IPaperSize\-1.md), 
[IScaling<T\>](DotNetBrowser.Print.Settings.IScaling\-1.md)

#### Extension Methods

[PrintSettingsExtensions.Apply<SystemPrinter.ISettings<T\>\>\(SystemPrinter.ISettings<T\>, Action<SystemPrinter.ISettings<T\>\>\)](DotNetBrowser.Print.Settings.PrintSettingsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSettingsExtensions\_Apply\_\_1\_\_\_0\_System\_Action\_\_\_0\_\_), 
[CollateExtensions.DisableCollatePrinting<T\>\(ICollate<T\>\)](DotNetBrowser.Print.Settings.CollateExtensions.md\#DotNetBrowser\_Print\_Settings\_CollateExtensions\_DisableCollatePrinting\_\_1\_DotNetBrowser\_Print\_Settings\_ICollate\_\_\_0\_\_), 
[CollateExtensions.EnableCollatePrinting<T\>\(ICollate<T\>\)](DotNetBrowser.Print.Settings.CollateExtensions.md\#DotNetBrowser\_Print\_Settings\_CollateExtensions\_EnableCollatePrinting\_\_1\_DotNetBrowser\_Print\_Settings\_ICollate\_\_\_0\_\_), 
[ColorModelExtensions.SetColorModel<T\>\(IColorModel<T\>, ColorModel\)](DotNetBrowser.Print.Settings.ColorModelExtensions.md\#DotNetBrowser\_Print\_Settings\_ColorModelExtensions\_SetColorModel\_\_1\_DotNetBrowser\_Print\_Settings\_IColorModel\_\_\_0\_\_DotNetBrowser\_Print\_ColorModel\_), 
[CopiesExtensions.SetCopies<T\>\(ICopies<T\>, int\)](DotNetBrowser.Print.Settings.CopiesExtensions.md\#DotNetBrowser\_Print\_Settings\_CopiesExtensions\_SetCopies\_\_1\_DotNetBrowser\_Print\_Settings\_ICopies\_\_\_0\_\_System\_Int32\_), 
[DuplexModeExtensions.SetDuplexMode<T\>\(IDuplexMode<T\>, DuplexMode\)](DotNetBrowser.Print.Settings.DuplexModeExtensions.md\#DotNetBrowser\_Print\_Settings\_DuplexModeExtensions\_SetDuplexMode\_\_1\_DotNetBrowser\_Print\_Settings\_IDuplexMode\_\_\_0\_\_DotNetBrowser\_Print\_DuplexMode\_), 
[PageRangesExtensions.SetPageRanges<T\>\(IPageRanges<T\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.PageRangesExtensions.md\#DotNetBrowser\_Print\_Settings\_PageRangesExtensions\_SetPageRanges\_\_1\_DotNetBrowser\_Print\_Settings\_IPageRanges\_\_\_0\_\_System\_Collections\_Generic\_IReadOnlyCollection\_DotNetBrowser\_Print\_PageRange\_\_), 
[PagesPerSheetExtensions.SetPagesPerSheet<T\>\(IPagesPerSheet<T\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.PagesPerSheetExtensions.md\#DotNetBrowser\_Print\_Settings\_PagesPerSheetExtensions\_SetPagesPerSheet\_\_1\_DotNetBrowser\_Print\_Settings\_IPagesPerSheet\_\_\_0\_\_DotNetBrowser\_Print\_PagesPerSheet\_), 
[PaperSizeExtensions.SetPaperSize<T\>\(IPaperSize<T\>, PaperSize\)](DotNetBrowser.Print.Settings.PaperSizeExtensions.md\#DotNetBrowser\_Print\_Settings\_PaperSizeExtensions\_SetPaperSize\_\_1\_DotNetBrowser\_Print\_Settings\_IPaperSize\_\_\_0\_\_DotNetBrowser\_Print\_PaperSize\_), 
[ScalingExtensions.SetScaling<T\>\(IScaling<T\>, Scaling\)](DotNetBrowser.Print.Settings.ScalingExtensions.md\#DotNetBrowser\_Print\_Settings\_ScalingExtensions\_SetScaling\_\_1\_DotNetBrowser\_Print\_Settings\_IScaling\_\_\_0\_\_DotNetBrowser\_Print\_Scaling\_)

