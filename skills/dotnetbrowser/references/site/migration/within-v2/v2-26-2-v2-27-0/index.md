
# Migrating from 2.26.2 to 2.27.0

## Updated API

### `FitToPage` and `FitToPaper` print settings

In this version, we have removed the `Scaling.FitToPage` and `Scaling.FitToPaper` fields. These options are only useful when printing a PDF file with a system printer. When printing an HTML page or using the built-in PDF printer, the methods were no-op, confusing developers.

Instead, we introduce a new [`IFit.Fit`][fit] property, which is available only for printing PDF files with system printers.

**v2.26.2**

```csharp
browser.PrintPdfContentHandler = 
    new Handler<PrintPdfContentParameters, PrintPdfContentResponse>(p =>
{
    var printer = p.Printers.Default;
    var settings = printer.PrintJob.Settings;
    settings.Scaling = Scaling.FitToPage;
    // ...
    return PrintPdfContentResponse.Print(printer);
});
```

**v2.27.0**

```csharp
browser.PrintPdfContentHandler = 
    new Handler<PrintPdfContentParameters, PrintPdfContentResponse>(p =>
{
    var printer = p.Printers.Default;
    var settings = printer.PrintJob.Settings;
    settings.Fit = Fit.ToPage;
    // ...
    return PrintPdfContentResponse.Print(printer);
});
```


[fit]: https://api.dotnetbrowser.dev/2.27.0/html/P_DotNetBrowser_Print_Settings_IFit_1_Fit.htm
