# <a id="DotNetBrowser_Print_Settings_IPaperSize_1"></a> Interface IPaperSize<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the paper size for printing.

```csharp
public interface IPaperSize<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[PaperSizeExtensions.SetPaperSize<TPrintSettings\>\(IPaperSize<TPrintSettings\>, PaperSize\)](DotNetBrowser.Print.Settings.PaperSizeExtensions.md\#DotNetBrowser\_Print\_Settings\_PaperSizeExtensions\_SetPaperSize\_\_1\_DotNetBrowser\_Print\_Settings\_IPaperSize\_\_\_0\_\_DotNetBrowser\_Print\_PaperSize\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
paper size.

## Properties

### <a id="DotNetBrowser_Print_Settings_IPaperSize_1_PaperSize"></a> PaperSize

Gets or sets the paper size for printing.

```csharp
PaperSize PaperSize { get; set; }
```

#### Property Value

 [PaperSize](DotNetBrowser.Print.PaperSize.md)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified paper size is null.

