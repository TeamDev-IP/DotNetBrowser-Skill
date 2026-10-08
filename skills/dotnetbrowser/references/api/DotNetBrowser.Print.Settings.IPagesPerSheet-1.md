# <a id="DotNetBrowser_Print_Settings_IPagesPerSheet_1"></a> Interface IPagesPerSheet<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the number of pages per sheet.

```csharp
public interface IPagesPerSheet<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[PagesPerSheetExtensions.SetPagesPerSheet<TPrintSettings\>\(IPagesPerSheet<TPrintSettings\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.PagesPerSheetExtensions.md\#DotNetBrowser\_Print\_Settings\_PagesPerSheetExtensions\_SetPagesPerSheet\_\_1\_DotNetBrowser\_Print\_Settings\_IPagesPerSheet\_\_\_0\_\_DotNetBrowser\_Print\_PagesPerSheet\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
the number of pages per sheet.

## Properties

### <a id="DotNetBrowser_Print_Settings_IPagesPerSheet_1_PagesPerSheet"></a> PagesPerSheet

Gets or sets the number of pages per sheet.

```csharp
PagesPerSheet PagesPerSheet { get; set; }
```

#### Property Value

 [PagesPerSheet](DotNetBrowser.Print.PagesPerSheet.md)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified number of pages per sheet is not supported by the printer.

