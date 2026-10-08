# <a id="DotNetBrowser_Print_PdfPrinter_ISettings_1"></a> Interface PdfPrinter.ISettings<T\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The print settings available when printing HTML or PDF content on the PDF printer.

```csharp
public interface PdfPrinter.ISettings<out T> : IPrintSettings, IPageRanges<T>, IPagesPerSheet<T>, IPdfFilePath<T>, IScaling<T> where T : class, IPrintSettings
```

#### Type Parameters

`T` 

The specific print settings type.

#### Implements

[IPrintSettings](DotNetBrowser.Print.Settings.IPrintSettings.md), 
[IPageRanges<T\>](DotNetBrowser.Print.Settings.IPageRanges\-1.md), 
[IPagesPerSheet<T\>](DotNetBrowser.Print.Settings.IPagesPerSheet\-1.md), 
[IPdfFilePath<T\>](DotNetBrowser.Print.Settings.IPdfFilePath\-1.md), 
[IScaling<T\>](DotNetBrowser.Print.Settings.IScaling\-1.md)

#### Extension Methods

[PrintSettingsExtensions.Apply<PdfPrinter.ISettings<T\>\>\(PdfPrinter.ISettings<T\>, Action<PdfPrinter.ISettings<T\>\>\)](DotNetBrowser.Print.Settings.PrintSettingsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSettingsExtensions\_Apply\_\_1\_\_\_0\_System\_Action\_\_\_0\_\_), 
[PageRangesExtensions.SetPageRanges<T\>\(IPageRanges<T\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.PageRangesExtensions.md\#DotNetBrowser\_Print\_Settings\_PageRangesExtensions\_SetPageRanges\_\_1\_DotNetBrowser\_Print\_Settings\_IPageRanges\_\_\_0\_\_System\_Collections\_Generic\_IReadOnlyCollection\_DotNetBrowser\_Print\_PageRange\_\_), 
[PagesPerSheetExtensions.SetPagesPerSheet<T\>\(IPagesPerSheet<T\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.PagesPerSheetExtensions.md\#DotNetBrowser\_Print\_Settings\_PagesPerSheetExtensions\_SetPagesPerSheet\_\_1\_DotNetBrowser\_Print\_Settings\_IPagesPerSheet\_\_\_0\_\_DotNetBrowser\_Print\_PagesPerSheet\_), 
[PdfFilePathExtensions.SetPdfFilePath<T\>\(IPdfFilePath<T\>, string\)](DotNetBrowser.Print.Settings.PdfFilePathExtensions.md\#DotNetBrowser\_Print\_Settings\_PdfFilePathExtensions\_SetPdfFilePath\_\_1\_DotNetBrowser\_Print\_Settings\_IPdfFilePath\_\_\_0\_\_System\_String\_), 
[ScalingExtensions.SetScaling<T\>\(IScaling<T\>, Scaling\)](DotNetBrowser.Print.Settings.ScalingExtensions.md\#DotNetBrowser\_Print\_Settings\_ScalingExtensions\_SetScaling\_\_1\_DotNetBrowser\_Print\_Settings\_IScaling\_\_\_0\_\_DotNetBrowser\_Print\_Scaling\_)

