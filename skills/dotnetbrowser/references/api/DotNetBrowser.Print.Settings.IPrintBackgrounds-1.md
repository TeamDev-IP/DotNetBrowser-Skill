# <a id="DotNetBrowser_Print_Settings_IPrintBackgrounds_1"></a> Interface IPrintBackgrounds<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring printing background graphics.

```csharp
public interface IPrintBackgrounds<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[PrintBackgroundsExtensions.DisablePrintingBackgrounds<TPrintSettings\>\(IPrintBackgrounds<TPrintSettings\>\)](DotNetBrowser.Print.Settings.PrintBackgroundsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintBackgroundsExtensions\_DisablePrintingBackgrounds\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintBackgrounds\_\_\_0\_\_), 
[PrintBackgroundsExtensions.EnablePrintingBackgrounds<TPrintSettings\>\(IPrintBackgrounds<TPrintSettings\>\)](DotNetBrowser.Print.Settings.PrintBackgroundsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintBackgroundsExtensions\_EnablePrintingBackgrounds\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintBackgrounds\_\_\_0\_\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
printing background graphics.

## Properties

### <a id="DotNetBrowser_Print_Settings_IPrintBackgrounds_1_PrintingBackgroundsEnabled"></a> PrintingBackgroundsEnabled

Enables or disables printing background graphics.

```csharp
bool PrintingBackgroundsEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The background graphics printing is not supported by the printer.

