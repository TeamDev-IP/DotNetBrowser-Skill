# <a id="DotNetBrowser_Print_Settings_IPrintHeaderFooter_1"></a> Interface IPrintHeaderFooter<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring printing headers and footers.

```csharp
public interface IPrintHeaderFooter<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[PrintHeaderFooterExtensions.DisablePrintingHeaderFooter<TPrintSettings\>\(IPrintHeaderFooter<TPrintSettings\>\)](DotNetBrowser.Print.Settings.PrintHeaderFooterExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintHeaderFooterExtensions\_DisablePrintingHeaderFooter\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintHeaderFooter\_\_\_0\_\_), 
[PrintHeaderFooterExtensions.EnablePrintingHeaderFooter<TPrintSettings\>\(IPrintHeaderFooter<TPrintSettings\>\)](DotNetBrowser.Print.Settings.PrintHeaderFooterExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintHeaderFooterExtensions\_EnablePrintingHeaderFooter\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintHeaderFooter\_\_\_0\_\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
printing headers and footers.

## Properties

### <a id="DotNetBrowser_Print_Settings_IPrintHeaderFooter_1_PrintingHeaderFooterEnabled"></a> PrintingHeaderFooterEnabled

Enables or disables printing headers and footer.

```csharp
bool PrintingHeaderFooterEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The headers and footer printing is not supported by the printer.

