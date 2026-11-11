# <a id="DotNetBrowser_Print"></a> Namespace DotNetBrowser.Print

### Namespaces

 [DotNetBrowser.Print.Events](DotNetBrowser.Print.Events.md)

 [DotNetBrowser.Print.Handlers](DotNetBrowser.Print.Handlers.md)

 [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)

### Classes

 [Capabilities](DotNetBrowser.Print.md#DotNetBrowser_Print_Capabilities)

The capabilities of a printer.

 [PageMargins](DotNetBrowser.Print.md#DotNetBrowser_Print_PageMargins)

The page margins used for printing.

 [PageRange](DotNetBrowser.Print.md#DotNetBrowser_Print_PageRange)

The page range to be printed.

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

The paper size used for printing.

 [PdfPrinter<TPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_1)

A printer that allows you to print to PDF.

 [PdfPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter)

A printer that allows you to print to PDF.

 [Printer<TPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1)

The base class for the printers.

 [Scaling](DotNetBrowser.Print.md#DotNetBrowser_Print_Scaling)

The scaling used for printing.

 [SystemPrinter<TPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_1)

A local or network printer available in the system.

 [SystemPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter)

A local or network printer available in the system.

### Interfaces

 [PdfPrinter.IHtmlSettings](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_IHtmlSettings)

The print settings available when printing HTML content on the PDF printer.

 [SystemPrinter.IHtmlSettings](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_IHtmlSettings)

Print settings available when printing HTML content on a physical printer.

 [PdfPrinter.IPdfSettings](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_IPdfSettings)

The print settings available when printing PDF content on the PDF printer.

 [SystemPrinter.IPdfSettings](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_IPdfSettings)

Print settings available when printing PDF content on a physical printer.

 [IPrintJob<TPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_IPrintJob_1)

A printing operation that is currently in-progress.

 [IPrinters<TPrintSettings, TPdfPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_IPrinters_2)

The collection of the available printers.

 [SystemPrinter.ISettings<T\>](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_ISettings_1)

Print settings available when printing HTML or PDF content on a physical printer.

 [PdfPrinter.ISettings<T\>](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_ISettings_1)

The print settings available when printing HTML or PDF content on the PDF printer.

### Enums

 [ColorModel](DotNetBrowser.Print.md#DotNetBrowser_Print_ColorModel)

The color models used for printing.

 [DuplexMode](DotNetBrowser.Print.md#DotNetBrowser_Print_DuplexMode)

The duplex modes used for printing.

 [Fit](DotNetBrowser.Print.md#DotNetBrowser_Print_Fit)

The content fit used for printing.

 [Orientation](DotNetBrowser.Print.md#DotNetBrowser_Print_Orientation)

The page orientation values used for printing.

 [PagesPerSheet](DotNetBrowser.Print.md#DotNetBrowser_Print_PagesPerSheet)

The pages per sheet values that Chromium supports.

 [PaperSize.Unit](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize_Unit)

The measurement unit of the paper size.

## <a id="DotNetBrowser_Print_Capabilities"></a> Class Capabilities

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The capabilities of a printer.

```csharp
public sealed class Capabilities
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Capabilities](DotNetBrowser.Print.md#DotNetBrowser_Print_Capabilities)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Print_Capabilities_CanCollate"></a> CanCollate

Indicates whether the printer supports collate printing.

```csharp
public bool CanCollate { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Print_Capabilities_ColorModels"></a> ColorModels

Gets the list of the <xref href="DotNetBrowser.Print.ColorModel" data-throw-if-not-resolved="false"></xref> values supported by the printer.

```csharp
public IReadOnlyList<ColorModel> ColorModels { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ColorModel](DotNetBrowser.Print.md#DotNetBrowser_Print_ColorModel)\>

#### <a id="DotNetBrowser_Print_Capabilities_DuplexModes"></a> DuplexModes

Gets the collection of the <xref href="DotNetBrowser.Print.DuplexMode" data-throw-if-not-resolved="false"></xref> values supported by the printer.

```csharp
public IReadOnlyCollection<DuplexMode> DuplexModes { get; }
```

##### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[DuplexMode](DotNetBrowser.Print.md#DotNetBrowser_Print_DuplexMode)\>

#### <a id="DotNetBrowser_Print_Capabilities_MaxCopies"></a> MaxCopies

Gets the maximum number of copies that the printer can make.

```csharp
public int MaxCopies { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Print_Capabilities_PaperSizes"></a> PaperSizes

Gets the collection of the <xref href="DotNetBrowser.Print.PaperSize" data-throw-if-not-resolved="false"></xref> values supported by the printer.

```csharp
public IReadOnlyCollection<PaperSize> PaperSizes { get; }
```

##### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)\>

## <a id="DotNetBrowser_Print_PageMargins"></a> Class PageMargins

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The page margins used for printing.

```csharp
public sealed class PageMargins
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PageMargins](DotNetBrowser.Print.md#DotNetBrowser_Print_PageMargins)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Print_PageMargins__ctor_System_Int32_System_Int32_System_Int32_System_Int32_"></a> PageMargins\(int, int, int, int\)

Creates custom margins for the web page in points. One point equals 1/72 of an inch.

```csharp
public PageMargins(int left, int right, int top, int bottom)
```

##### Parameters

`left` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The margin on the left side of the sheet. Cannot be negative.

`right` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The margin on the right side of the sheet. Cannot be negative.

`top` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The margin on the top side of the sheet. Cannot be negative.

`bottom` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The margin on the bottom side of the sheet. Cannot be negative.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Any of the parameters is negative.

### Fields

#### <a id="DotNetBrowser_Print_PageMargins_Default"></a> Default

The default margins for the page.

```csharp
public static readonly PageMargins Default
```

##### Field Value

 [PageMargins](DotNetBrowser.Print.md#DotNetBrowser_Print_PageMargins)

#### <a id="DotNetBrowser_Print_PageMargins_None"></a> None

The empty margins for the page.

```csharp
public static readonly PageMargins None
```

##### Field Value

 [PageMargins](DotNetBrowser.Print.md#DotNetBrowser_Print_PageMargins)

### Properties

#### <a id="DotNetBrowser_Print_PageMargins_Bottom"></a> Bottom

Gets the margin on the bottom side of the sheet.

```csharp
public int Bottom { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Print_PageMargins_Left"></a> Left

Gets the margin on the left side of the sheet.

```csharp
public int Left { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Print_PageMargins_Right"></a> Right

Gets the margin on the right side of the sheet.

```csharp
public int Right { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Print_PageMargins_Top"></a> Top

Gets the margin on the top side of the sheet.

```csharp
public int Top { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### Methods

#### <a id="DotNetBrowser_Print_PageMargins_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Print_PageMargins_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Print_PageRange"></a> Class PageRange

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The page range to be printed.

```csharp
public sealed class PageRange
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PageRange](DotNetBrowser.Print.md#DotNetBrowser_Print_PageRange)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Print_PageRange__ctor_System_Int32_System_Int32_"></a> PageRange\(int, int\)

Creates a new page range instance.

```csharp
public PageRange(int from, int to)
```

##### Parameters

`from` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The 1-based number of the first page within the range.

`to` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The 1-based number of the last page within the range.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">from</code> is greater than <code class="paramref">to</code>.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">from</code> is less than or equal to zero.

### Properties

#### <a id="DotNetBrowser_Print_PageRange_From"></a> From

Gets the number of the first page within the range.

```csharp
public int From { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Print_PageRange_To"></a> To

Gets the number of the last page within the range.

```csharp
public int To { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### Methods

#### <a id="DotNetBrowser_Print_PageRange_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Print_PageRange_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Print_PaperSize"></a> Class PaperSize

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The paper size used for printing.

```csharp
public sealed class PaperSize
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Print_PaperSize_Iso2A0"></a> Iso2A0

ISO standard sheet media size "2A0".

```csharp
public static readonly PaperSize Iso2A0
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA0"></a> IsoA0

ISO standard sheet media size "A0".

```csharp
public static readonly PaperSize IsoA0
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA0X3"></a> IsoA0X3

ISO standard sheet media size "A0x3".

```csharp
public static readonly PaperSize IsoA0X3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA1"></a> IsoA1

ISO standard sheet media size "A1".

```csharp
public static readonly PaperSize IsoA1
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA10"></a> IsoA10

ISO standard sheet media size "A10".

```csharp
public static readonly PaperSize IsoA10
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA1X3"></a> IsoA1X3

ISO standard sheet media size "A1x3".

```csharp
public static readonly PaperSize IsoA1X3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA1X4"></a> IsoA1X4

ISO standard sheet media size "A1x4".

```csharp
public static readonly PaperSize IsoA1X4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA2"></a> IsoA2

ISO standard sheet media size "A2".

```csharp
public static readonly PaperSize IsoA2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA2X3"></a> IsoA2X3

ISO standard sheet media size "A2x3".

```csharp
public static readonly PaperSize IsoA2X3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA2X4"></a> IsoA2X4

ISO standard sheet media size "A2x4".

```csharp
public static readonly PaperSize IsoA2X4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA2X5"></a> IsoA2X5

ISO standard sheet media size "A2x5".

```csharp
public static readonly PaperSize IsoA2X5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA3"></a> IsoA3

ISO standard sheet media size "A3".

```csharp
public static readonly PaperSize IsoA3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA3Extra"></a> IsoA3Extra

ISO standard sheet media size "A3 Extra".

```csharp
public static readonly PaperSize IsoA3Extra
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA3X3"></a> IsoA3X3

ISO standard sheet media size "A3x3".

```csharp
public static readonly PaperSize IsoA3X3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA3X4"></a> IsoA3X4

ISO standard sheet media size "A3x4".

```csharp
public static readonly PaperSize IsoA3X4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA3X5"></a> IsoA3X5

ISO standard sheet media size "A3x5".

```csharp
public static readonly PaperSize IsoA3X5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA3X6"></a> IsoA3X6

ISO standard sheet media size "A3x6".

```csharp
public static readonly PaperSize IsoA3X6
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA3X7"></a> IsoA3X7

ISO standard sheet media size "A3x7".

```csharp
public static readonly PaperSize IsoA3X7
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4"></a> IsoA4

ISO standard sheet media size "A4".

```csharp
public static readonly PaperSize IsoA4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4Extra"></a> IsoA4Extra

ISO standard sheet media size "A4 Extra".

```csharp
public static readonly PaperSize IsoA4Extra
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4Tab"></a> IsoA4Tab

ISO standard sheet media size "A4 Tab".

```csharp
public static readonly PaperSize IsoA4Tab
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4X3"></a> IsoA4X3

ISO standard sheet media size "A4x3".

```csharp
public static readonly PaperSize IsoA4X3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4X4"></a> IsoA4X4

ISO standard sheet media size "A4x4".

```csharp
public static readonly PaperSize IsoA4X4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4X5"></a> IsoA4X5

ISO standard sheet media size "A4x5".

```csharp
public static readonly PaperSize IsoA4X5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4X6"></a> IsoA4X6

ISO standard sheet media size "A4x6".

```csharp
public static readonly PaperSize IsoA4X6
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4X7"></a> IsoA4X7

ISO standard sheet media size "A4x7".

```csharp
public static readonly PaperSize IsoA4X7
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4X8"></a> IsoA4X8

ISO standard sheet media size "A4x8".

```csharp
public static readonly PaperSize IsoA4X8
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA4X9"></a> IsoA4X9

ISO standard sheet media size "A4x9".

```csharp
public static readonly PaperSize IsoA4X9
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA5"></a> IsoA5

ISO standard sheet media size "A5".

```csharp
public static readonly PaperSize IsoA5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA5Extra"></a> IsoA5Extra

ISO standard sheet media size "A5 Extra".

```csharp
public static readonly PaperSize IsoA5Extra
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA6"></a> IsoA6

ISO standard sheet media size "A6".

```csharp
public static readonly PaperSize IsoA6
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA7"></a> IsoA7

ISO standard sheet media size "A7".

```csharp
public static readonly PaperSize IsoA7
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA8"></a> IsoA8

ISO standard sheet media size "A8".

```csharp
public static readonly PaperSize IsoA8
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoA9"></a> IsoA9

ISO standard sheet media size "A9".

```csharp
public static readonly PaperSize IsoA9
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB0"></a> IsoB0

ISO standard sheet media size "B0".

```csharp
public static readonly PaperSize IsoB0
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB1"></a> IsoB1

ISO standard sheet media size "B1".

```csharp
public static readonly PaperSize IsoB1
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB10"></a> IsoB10

ISO standard sheet media size "B10".

```csharp
public static readonly PaperSize IsoB10
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB2"></a> IsoB2

ISO standard sheet media size "B2".

```csharp
public static readonly PaperSize IsoB2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB3"></a> IsoB3

ISO standard sheet media size "B3".

```csharp
public static readonly PaperSize IsoB3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB4"></a> IsoB4

ISO standard sheet media size "B4".

```csharp
public static readonly PaperSize IsoB4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB5"></a> IsoB5

ISO standard sheet media size "B5".

```csharp
public static readonly PaperSize IsoB5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB5Extra"></a> IsoB5Extra

ISO standard sheet media size "B5 Extra".

```csharp
public static readonly PaperSize IsoB5Extra
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB6"></a> IsoB6

ISO standard sheet media size "B6".

```csharp
public static readonly PaperSize IsoB6
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB6C4"></a> IsoB6C4

ISO standard sheet media size "B6C4".

```csharp
public static readonly PaperSize IsoB6C4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB7"></a> IsoB7

ISO standard sheet media size "B7".

```csharp
public static readonly PaperSize IsoB7
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB8"></a> IsoB8

ISO standard sheet media size "B8".

```csharp
public static readonly PaperSize IsoB8
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoB9"></a> IsoB9

ISO standard sheet media size "B9".

```csharp
public static readonly PaperSize IsoB9
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC0"></a> IsoC0

ISO standard sheet media size "C0".

```csharp
public static readonly PaperSize IsoC0
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC1"></a> IsoC1

ISO standard sheet media size "C1".

```csharp
public static readonly PaperSize IsoC1
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC10"></a> IsoC10

ISO standard sheet media size "C10".

```csharp
public static readonly PaperSize IsoC10
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC2"></a> IsoC2

ISO standard sheet media size "C2".

```csharp
public static readonly PaperSize IsoC2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC3"></a> IsoC3

ISO standard sheet media size "C3".

```csharp
public static readonly PaperSize IsoC3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC4"></a> IsoC4

ISO standard sheet media size "C4".

```csharp
public static readonly PaperSize IsoC4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC5"></a> IsoC5

ISO standard sheet media size "C5".

```csharp
public static readonly PaperSize IsoC5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC6"></a> IsoC6

ISO standard sheet media size "C6".

```csharp
public static readonly PaperSize IsoC6
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC6C5"></a> IsoC6C5

ISO standard sheet media size "C6C5".

```csharp
public static readonly PaperSize IsoC6C5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC7"></a> IsoC7

ISO standard sheet media size "C7".

```csharp
public static readonly PaperSize IsoC7
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC7C6"></a> IsoC7C6

ISO standard sheet media size "C7C6".

```csharp
public static readonly PaperSize IsoC7C6
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC8"></a> IsoC8

ISO standard sheet media size "C8".

```csharp
public static readonly PaperSize IsoC8
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoC9"></a> IsoC9

ISO standard sheet media size "C9".

```csharp
public static readonly PaperSize IsoC9
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoDl"></a> IsoDl

ISO standard sheet media size "DL".

```csharp
public static readonly PaperSize IsoDl
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoRa0"></a> IsoRa0

ISO standard sheet media size "RA0".

```csharp
public static readonly PaperSize IsoRa0
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoRa1"></a> IsoRa1

ISO standard sheet media size "RA1".

```csharp
public static readonly PaperSize IsoRa1
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoRa2"></a> IsoRa2

ISO standard sheet media size "RA2".

```csharp
public static readonly PaperSize IsoRa2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoSra0"></a> IsoSra0

ISO standard sheet media size "SRA0".

```csharp
public static readonly PaperSize IsoSra0
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoSra1"></a> IsoSra1

ISO standard sheet media size "SRA1".

```csharp
public static readonly PaperSize IsoSra1
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_IsoSra2"></a> IsoSra2

ISO standard sheet media size "SRA2".

```csharp
public static readonly PaperSize IsoSra2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB0"></a> JisB0

Japanese standard sheet media size "B0 (JIS)".

```csharp
public static readonly PaperSize JisB0
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB1"></a> JisB1

Japanese standard sheet media size "B1 (JIS)".

```csharp
public static readonly PaperSize JisB1
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB10"></a> JisB10

Japanese standard sheet media size "B10 (JIS)".

```csharp
public static readonly PaperSize JisB10
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB2"></a> JisB2

Japanese standard sheet media size "B2 (JIS)".

```csharp
public static readonly PaperSize JisB2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB3"></a> JisB3

Japanese standard sheet media size "B3 (JIS)".

```csharp
public static readonly PaperSize JisB3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB4"></a> JisB4

Japanese standard sheet media size "B4 (JIS)".

```csharp
public static readonly PaperSize JisB4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB5"></a> JisB5

Japanese standard sheet media size "B5 (JIS)".

```csharp
public static readonly PaperSize JisB5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB6"></a> JisB6

Japanese standard sheet media size "B6 (JIS)".

```csharp
public static readonly PaperSize JisB6
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB7"></a> JisB7

Japanese standard sheet media size "B7 (JIS)".

```csharp
public static readonly PaperSize JisB7
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB8"></a> JisB8

Japanese standard sheet media size "B8 (JIS)".

```csharp
public static readonly PaperSize JisB8
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisB9"></a> JisB9

Japanese standard sheet media size "B9 (JIS)".

```csharp
public static readonly PaperSize JisB9
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JisExec"></a> JisExec

Japanese standard sheet media size "Executive (JIS)".

```csharp
public static readonly PaperSize JisExec
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JpnChou2"></a> JpnChou2

Japanese standard sheet media size "Choukei 2".

```csharp
public static readonly PaperSize JpnChou2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JpnChou3"></a> JpnChou3

Japanese standard sheet media size "Choukei 3".

```csharp
public static readonly PaperSize JpnChou3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JpnChou4"></a> JpnChou4

Japanese standard sheet media size "Choukei 4".

```csharp
public static readonly PaperSize JpnChou4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JpnHagaki"></a> JpnHagaki

Japanese standard sheet media size "Hagaki".

```csharp
public static readonly PaperSize JpnHagaki
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JpnKahu"></a> JpnKahu

Japanese standard sheet media size "Kahu Envelope".

```csharp
public static readonly PaperSize JpnKahu
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JpnKaku2"></a> JpnKaku2

Japanese standard sheet media size "Kaku 2".

```csharp
public static readonly PaperSize JpnKaku2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JpnOufuku"></a> JpnOufuku

Japanese standard sheet media size "Oufuku Hagaki".

```csharp
public static readonly PaperSize JpnOufuku
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_JpnYou4"></a> JpnYou4

Japanese standard sheet media size "You 4".

```csharp
public static readonly PaperSize JpnYou4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na10X11"></a> Na10X11

North American standard sheet media size "10x11".

```csharp
public static readonly PaperSize Na10X11
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na10X13"></a> Na10X13

North American standard sheet media size "10x13".

```csharp
public static readonly PaperSize Na10X13
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na10X14"></a> Na10X14

North American standard sheet media size "10x14".

```csharp
public static readonly PaperSize Na10X14
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na10X15"></a> Na10X15

North American standard sheet media size "10x15".

```csharp
public static readonly PaperSize Na10X15
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na11X12"></a> Na11X12

North American standard sheet media size "11x12".

```csharp
public static readonly PaperSize Na11X12
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na11X15"></a> Na11X15

North American standard sheet media size "11x15".

```csharp
public static readonly PaperSize Na11X15
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na12X19"></a> Na12X19

North American standard sheet media size "12x19".

```csharp
public static readonly PaperSize Na12X19
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na5X7"></a> Na5X7

North American standard sheet media size "5x7".

```csharp
public static readonly PaperSize Na5X7
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na6X9"></a> Na6X9

North American standard sheet media size "6x9".

```csharp
public static readonly PaperSize Na6X9
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na7X9"></a> Na7X9

North American standard sheet media size "7x9".

```csharp
public static readonly PaperSize Na7X9
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Na9X11"></a> Na9X11

North American standard sheet media size "9x11".

```csharp
public static readonly PaperSize Na9X11
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaA2"></a> NaA2

North American standard sheet media size "A2".

```csharp
public static readonly PaperSize NaA2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaArchA"></a> NaArchA

North American standard sheet media size "Arch A".

```csharp
public static readonly PaperSize NaArchA
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaArchB"></a> NaArchB

North American standard sheet media size "Arch B".

```csharp
public static readonly PaperSize NaArchB
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaArchC"></a> NaArchC

North American standard sheet media size "Arch C".

```csharp
public static readonly PaperSize NaArchC
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaArchD"></a> NaArchD

North American standard sheet media size "Arch D".

```csharp
public static readonly PaperSize NaArchD
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaArchE"></a> NaArchE

North American standard sheet media size "Arch E".

```csharp
public static readonly PaperSize NaArchE
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaAsmeF"></a> NaAsmeF

North American standard sheet media size "ASME F".

```csharp
public static readonly PaperSize NaAsmeF
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaBPlus"></a> NaBPlus

North American standard sheet media size "B-plus".

```csharp
public static readonly PaperSize NaBPlus
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaC"></a> NaC

North American standard sheet media size "C".

```csharp
public static readonly PaperSize NaC
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaC5"></a> NaC5

North American standard sheet media size "C5".

```csharp
public static readonly PaperSize NaC5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaD"></a> NaD

North American standard sheet media size "D".

```csharp
public static readonly PaperSize NaD
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaE"></a> NaE

North American standard sheet media size "E".

```csharp
public static readonly PaperSize NaE
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaEdp"></a> NaEdp

North American standard sheet media size "EDP".

```csharp
public static readonly PaperSize NaEdp
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaEurEdp"></a> NaEurEdp

North American standard sheet media size "European EDP".

```csharp
public static readonly PaperSize NaEurEdp
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaExecutive"></a> NaExecutive

North American standard sheet media size "Executive".

```csharp
public static readonly PaperSize NaExecutive
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaF"></a> NaF

North American standard sheet media size "F".

```csharp
public static readonly PaperSize NaF
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaFanfoldEur"></a> NaFanfoldEur

North American standard sheet media size "FanFold European".

```csharp
public static readonly PaperSize NaFanfoldEur
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaFanfoldUs"></a> NaFanfoldUs

North American standard sheet media size "FanFold US".

```csharp
public static readonly PaperSize NaFanfoldUs
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaFoolscap"></a> NaFoolscap

North American standard sheet media size "FanFold German Legal".

```csharp
public static readonly PaperSize NaFoolscap
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaGovtLegal"></a> NaGovtLegal

North American standard sheet media size "Government Legal".

```csharp
public static readonly PaperSize NaGovtLegal
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaGovtLetter"></a> NaGovtLetter

North American standard sheet media size "Government Letter".

```csharp
public static readonly PaperSize NaGovtLetter
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaIndex3X5"></a> NaIndex3X5

North American standard sheet media size "Index 3x5".

```csharp
public static readonly PaperSize NaIndex3X5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaIndex4X6"></a> NaIndex4X6

North American standard sheet media size "Index 4x6".

```csharp
public static readonly PaperSize NaIndex4X6
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaIndex4X6Ext"></a> NaIndex4X6Ext

North American standard sheet media size "Index 4x6 ext".

```csharp
public static readonly PaperSize NaIndex4X6Ext
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaIndex5X8"></a> NaIndex5X8

North American standard sheet media size "Index 5x8".

```csharp
public static readonly PaperSize NaIndex5X8
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaInvoice"></a> NaInvoice

North American standard sheet media size "Invoice".

```csharp
public static readonly PaperSize NaInvoice
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaLedger"></a> NaLedger

North American standard sheet media size "Tabloid".

```csharp
public static readonly PaperSize NaLedger
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaLegal"></a> NaLegal

North American standard sheet media size "Legal".

```csharp
public static readonly PaperSize NaLegal
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaLegalExtra"></a> NaLegalExtra

North American standard sheet media size "Legal extra".

```csharp
public static readonly PaperSize NaLegalExtra
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaLetter"></a> NaLetter

North American standard sheet media size "Letter".

```csharp
public static readonly PaperSize NaLetter
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaLetterExtra"></a> NaLetterExtra

North American standard sheet media size "Letter extra".

```csharp
public static readonly PaperSize NaLetterExtra
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaLetterPlus"></a> NaLetterPlus

North American standard sheet media size "Letter plus".

```csharp
public static readonly PaperSize NaLetterPlus
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaMonarch"></a> NaMonarch

North American standard sheet media size "Monarch".

```csharp
public static readonly PaperSize NaMonarch
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaNumber10"></a> NaNumber10

North American standard sheet media size "Envelope #10".

```csharp
public static readonly PaperSize NaNumber10
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaNumber11"></a> NaNumber11

North American standard sheet media size "Envelope #11".

```csharp
public static readonly PaperSize NaNumber11
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaNumber12"></a> NaNumber12

North American standard sheet media size "Envelope #12".

```csharp
public static readonly PaperSize NaNumber12
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaNumber14"></a> NaNumber14

North American standard sheet media size "Envelope #14".

```csharp
public static readonly PaperSize NaNumber14
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaNumber9"></a> NaNumber9

North American standard sheet media size "Envelope #9".

```csharp
public static readonly PaperSize NaNumber9
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaPersonal"></a> NaPersonal

North American standard sheet media size "Personal".

```csharp
public static readonly PaperSize NaPersonal
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaQuarto"></a> NaQuarto

North American standard sheet media size "Quarto".

```csharp
public static readonly PaperSize NaQuarto
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaSuperA"></a> NaSuperA

North American standard sheet media size "Super A".

```csharp
public static readonly PaperSize NaSuperA
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaSuperB"></a> NaSuperB

North American standard sheet media size "Super B".

```csharp
public static readonly PaperSize NaSuperB
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_NaWideFormat"></a> NaWideFormat

North American standard sheet media size "Wide format".

```csharp
public static readonly PaperSize NaWideFormat
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmDaiPaKai"></a> OmDaiPaKai

Chinese standard sheet media size "Dai-pa-kai".

```csharp
public static readonly PaperSize OmDaiPaKai
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmFolio"></a> OmFolio

Other metric standard sheet media size "Folio".

```csharp
public static readonly PaperSize OmFolio
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmFolioSp"></a> OmFolioSp

Other metric standard sheet media size "Folio SP".

```csharp
public static readonly PaperSize OmFolioSp
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmInvite"></a> OmInvite

Other metric standard sheet media size "Invite Envelope".

```csharp
public static readonly PaperSize OmInvite
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmItalian"></a> OmItalian

Other metric standard sheet media size "Italian Envelope".

```csharp
public static readonly PaperSize OmItalian
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmJuuroKuKai"></a> OmJuuroKuKai

Chinese standard sheet media size "Juuro-ku-kai".

```csharp
public static readonly PaperSize OmJuuroKuKai
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmLargePhoto"></a> OmLargePhoto

Other metric standard sheet media size "Large photo".

```csharp
public static readonly PaperSize OmLargePhoto
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmPaKai"></a> OmPaKai

Chinese standard sheet media size "Pa-kai".

```csharp
public static readonly PaperSize OmPaKai
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmPostfix"></a> OmPostfix

Other metric standard sheet media size "Postfix Envelope".

```csharp
public static readonly PaperSize OmPostfix
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_OmSmallPhoto"></a> OmSmallPhoto

Other metric standard sheet media size "Small photo".

```csharp
public static readonly PaperSize OmSmallPhoto
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc1"></a> Prc1

Chinese standard sheet media size "prc1 Envelope".

```csharp
public static readonly PaperSize Prc1
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc10"></a> Prc10

Chinese standard sheet media size "prc10 Envelope".

```csharp
public static readonly PaperSize Prc10
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc16K"></a> Prc16K

Chinese standard sheet media size "prc 16k".

```csharp
public static readonly PaperSize Prc16K
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc2"></a> Prc2

Chinese standard sheet media size "prc2 Envelope".

```csharp
public static readonly PaperSize Prc2
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc3"></a> Prc3

Chinese standard sheet media size "prc3 Envelope".

```csharp
public static readonly PaperSize Prc3
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc32K"></a> Prc32K

Chinese standard sheet media size "prc 32k".

```csharp
public static readonly PaperSize Prc32K
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc4"></a> Prc4

Chinese standard sheet media size "prc4 Envelope".

```csharp
public static readonly PaperSize Prc4
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc5"></a> Prc5

Chinese standard sheet media size "prc5 Envelope".

```csharp
public static readonly PaperSize Prc5
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc6"></a> Prc6

Chinese standard sheet media size "prc6 Envelope".

```csharp
public static readonly PaperSize Prc6
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc7"></a> Prc7

Chinese standard sheet media size "prc7 Envelope".

```csharp
public static readonly PaperSize Prc7
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Prc8"></a> Prc8

Chinese standard sheet media size "prc8 Envelope".

```csharp
public static readonly PaperSize Prc8
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Roc16K"></a> Roc16K

Chinese standard sheet media size "ROC 16K".

```csharp
public static readonly PaperSize Roc16K
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

#### <a id="DotNetBrowser_Print_PaperSize_Roc8K"></a> Roc8K

Chinese standard sheet media size "ROC 8K".

```csharp
public static readonly PaperSize Roc8K
```

##### Field Value

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

### Properties

#### <a id="DotNetBrowser_Print_PaperSize_Height"></a> Height

Gets the paper height in microns.

```csharp
public int Height { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Print_PaperSize_Name"></a> Name

Gets the paper size name.

```csharp
public string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Print_PaperSize_Width"></a> Width

Gets the paper width in microns.

```csharp
public int Width { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### Methods

#### <a id="DotNetBrowser_Print_PaperSize_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Print_PaperSize_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### <a id="DotNetBrowser_Print_PaperSize_Of_System_Single_System_Single_DotNetBrowser_Print_PaperSize_Unit_System_String_"></a> Of\(float, float, Unit, string\)

Creates a new paper size setting.

```csharp
public static PaperSize Of(float width, float height, PaperSize.Unit unit, string name)
```

##### Parameters

`width` [float](https://learn.microsoft.com/dotnet/api/system.single)

The paper size width.

`height` [float](https://learn.microsoft.com/dotnet/api/system.single)

The paper size height.

`unit` [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize).[Unit](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize_Unit)

The <code class="paramref">width</code> and <code class="paramref">height</code> measurement unit.

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The name of the paper size.

##### Returns

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

The paper size used for printing.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">width</code> is negative.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">height</code> is negative.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">name</code> is null , empty or contains only white space.

#### <a id="DotNetBrowser_Print_PaperSize_Of_System_Single_System_Single_DotNetBrowser_Print_PaperSize_Unit_"></a> Of\(float, float, Unit\)

Creates a new paper size setting.

```csharp
public static PaperSize Of(float width, float height, PaperSize.Unit unit)
```

##### Parameters

`width` [float](https://learn.microsoft.com/dotnet/api/system.single)

The paper size width.

`height` [float](https://learn.microsoft.com/dotnet/api/system.single)

The paper size height.

`unit` [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize).[Unit](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize_Unit)

The <code class="paramref">width</code> and <code class="paramref">height</code> measurement unit.

##### Returns

 [PaperSize](DotNetBrowser.Print.md#DotNetBrowser_Print_PaperSize)

The paper size used for printing.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">width</code> is negative.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">height</code> is negative.

#### <a id="DotNetBrowser_Print_PaperSize_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Print_PdfPrinter"></a> Class PdfPrinter

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

A printer that allows you to print to PDF.

```csharp
public static class PdfPrinter
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PdfPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Print_PdfPrinter_1"></a> Class PdfPrinter<TPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

A printer that allows you to print to PDF.

```csharp
public sealed class PdfPrinter<TPrintSettings> : Printer<TPrintSettings>, IAutoDisposable where TPrintSettings : class, PdfPrinter.ISettings<TPrintSettings>
```

##### Type Parameters

`TPrintSettings` 

The print settings type that can be applied to the print job.

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Printer<TPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1) ← 
[PdfPrinter<TPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_1)

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Inherited Members

[Printer<TPrintSettings\>.Capabilities](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1_Capabilities), 
[Printer<TPrintSettings\>.DeviceName](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1_DeviceName), 
[Printer<TPrintSettings\>.IsDefault](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1_IsDefault), 
[Printer<TPrintSettings\>.PrintJob](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1_PrintJob), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Print_Printer_1"></a> Class Printer<TPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The base class for the printers.

```csharp
public abstract class Printer<TPrintSettings> : IAutoDisposable where TPrintSettings : class, IPrintSettings
```

##### Type Parameters

`TPrintSettings` 

The print settings type available for this printer.

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Printer<TPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1)

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Print_Printer_1_Capabilities"></a> Capabilities

Gets the capabilities of this printer.

```csharp
public Capabilities Capabilities { get; }
```

##### Property Value

 [Capabilities](DotNetBrowser.Print.md#DotNetBrowser_Print_Capabilities)

#### <a id="DotNetBrowser_Print_Printer_1_DeviceName"></a> DeviceName

Gets the device name of this printer.

```csharp
public string DeviceName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Print_Printer_1_IsDefault"></a> IsDefault

Indicates whether this printer is the default system printer.

```csharp
public bool IsDefault { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Print_Printer_1_PrintJob"></a> PrintJob

Gets the current print job. This print job can be used to configure print settings.

```csharp
public IPrintJob<TPrintSettings> PrintJob { get; }
```

##### Property Value

 [IPrintJob](DotNetBrowser.Print.md#DotNetBrowser_Print_IPrintJob_1)<TPrintSettings\>

## <a id="DotNetBrowser_Print_Scaling"></a> Class Scaling

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The scaling used for printing.

```csharp
public sealed class Scaling
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Scaling](DotNetBrowser.Print.md#DotNetBrowser_Print_Scaling)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Fields

#### <a id="DotNetBrowser_Print_Scaling_Default"></a> Default

The default scaling for the printing content.

```csharp
public static readonly Scaling Default
```

##### Field Value

 [Scaling](DotNetBrowser.Print.md#DotNetBrowser_Print_Scaling)

### Methods

#### <a id="DotNetBrowser_Print_Scaling_Custom_System_Int32_"></a> Custom\(int\)

Creates a custom scaling which scales the content according to the given scale factor.

```csharp
public static Scaling Custom(int scaleFactor)
```

##### Parameters

`scaleFactor` [int](https://learn.microsoft.com/dotnet/api/system.int32)

       The scale factor to apply to the content, where 

       <pre><code class="lang-csharp">100</code></pre>

is a normal size. Should
       be in the range from 

       <pre><code class="lang-csharp">10</code></pre>

to 

<pre><code class="lang-csharp">200</code></pre>

.

##### Returns

 [Scaling](DotNetBrowser.Print.md#DotNetBrowser_Print_Scaling)

The scaling used for printing.

##### Exceptions

 [ArgumentOutOfRangeException](https://learn.microsoft.com/dotnet/api/system.argumentoutofrangeexception)

       The <code class="paramref">scaleFactor</code> is out of range.
       Should be in the range from 

       <pre><code class="lang-csharp">10</code></pre>

to 

<pre><code class="lang-csharp">200</code></pre>

.

#### <a id="DotNetBrowser_Print_Scaling_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

##### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Print_Scaling_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

##### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## <a id="DotNetBrowser_Print_SystemPrinter"></a> Class SystemPrinter

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

A local or network printer available in the system.

```csharp
public static class SystemPrinter
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SystemPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Print_SystemPrinter_1"></a> Class SystemPrinter<TPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

A local or network printer available in the system.

```csharp
public sealed class SystemPrinter<TPrintSettings> : Printer<TPrintSettings>, IAutoDisposable where TPrintSettings : class, SystemPrinter.ISettings<TPrintSettings>
```

##### Type Parameters

`TPrintSettings` 

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Printer<TPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1) ← 
[SystemPrinter<TPrintSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_1)

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Inherited Members

[Printer<TPrintSettings\>.Capabilities](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1_Capabilities), 
[Printer<TPrintSettings\>.DeviceName](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1_DeviceName), 
[Printer<TPrintSettings\>.IsDefault](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1_IsDefault), 
[Printer<TPrintSettings\>.PrintJob](DotNetBrowser.Print.md#DotNetBrowser_Print_Printer_1_PrintJob), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Print_IPrintJob_1"></a> Interface IPrintJob<TPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

A printing operation that is currently in-progress.

```csharp
public interface IPrintJob<TPrintSettings> : IAutoDisposable where TPrintSettings : class, IPrintSettings
```

##### Type Parameters

`TPrintSettings` 

The type of print settings that can be applied to this job.

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Print_IPrintJob_1_Settings"></a> Settings

Gets the configurable settings of this print job.

```csharp
TPrintSettings Settings { get; }
```

##### Property Value

 TPrintSettings

#### <a id="DotNetBrowser_Print_IPrintJob_1_PageCountUpdated"></a> PageCountUpdated

Occurs when the total number of pages to be printed is updated.

```csharp
event EventHandler<PageCountUpdatedEventArgs<TPrintSettings>> PageCountUpdated
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PageCountUpdatedEventArgs](DotNetBrowser.Print.Events.md#DotNetBrowser_Print_Events_PageCountUpdatedEventArgs_1)<TPrintSettings\>\>

##### Remarks

The page count is updated each time when the
<xref href="DotNetBrowser.Print.Settings.IPrintSettings.Apply" data-throw-if-not-resolved="false"></xref> method is called.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Print_IPrintJob_1_PrintCompleted"></a> PrintCompleted

Occurs when the printing operation is completed.

```csharp
event EventHandler<PrintCompletedEventArgs<TPrintSettings>> PrintCompleted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PrintCompletedEventArgs](DotNetBrowser.Print.Events.md#DotNetBrowser_Print_Events_PrintCompletedEventArgs_1)<TPrintSettings\>\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Print_IPrinters_2"></a> Interface IPrinters<TPrintSettings, TPdfPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The collection of the available printers.

```csharp
public interface IPrinters<TPrintSettings, TPdfPrintSettings> : IReadOnlyList<SystemPrinter<TPrintSettings>>, IReadOnlyCollection<SystemPrinter<TPrintSettings>>, IEnumerable<SystemPrinter<TPrintSettings>>, IEnumerable where TPrintSettings : class, SystemPrinter.ISettings<TPrintSettings> where TPdfPrintSettings : class, PdfPrinter.ISettings<TPdfPrintSettings>
```

##### Type Parameters

`TPrintSettings` 

The print settings type available for these printers.

`TPdfPrintSettings` 

The PDF print settings type available for PDF printer.

##### Implements

[IReadOnlyList<SystemPrinter<TPrintSettings\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1), 
[IReadOnlyCollection<SystemPrinter<TPrintSettings\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1), 
[IEnumerable<SystemPrinter<TPrintSettings\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1), 
[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.ienumerable)

### Properties

#### <a id="DotNetBrowser_Print_IPrinters_2_Default"></a> Default

Gets the default system printer.

```csharp
SystemPrinter<TPrintSettings> Default { get; }
```

##### Property Value

 [SystemPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_1)<TPrintSettings\>

#### <a id="DotNetBrowser_Print_IPrinters_2_Pdf"></a> Pdf

Gets the <xref href="DotNetBrowser.Print.PdfPrinter" data-throw-if-not-resolved="false"></xref> instance that allows you to print to PDF.

```csharp
PdfPrinter<TPdfPrintSettings> Pdf { get; }
```

##### Property Value

 [PdfPrinter](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_1)<TPdfPrintSettings\>

## <a id="DotNetBrowser_Print_PdfPrinter_IHtmlSettings"></a> Interface PdfPrinter.IHtmlSettings

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The print settings available when printing HTML content on the PDF printer.

```csharp
public interface PdfPrinter.IHtmlSettings : PdfPrinter.ISettings<PdfPrinter.IHtmlSettings>, IPrintSettings, IPageRanges<PdfPrinter.IHtmlSettings>, IPagesPerSheet<PdfPrinter.IHtmlSettings>, IPdfFilePath<PdfPrinter.IHtmlSettings>, IScaling<PdfPrinter.IHtmlSettings>, IPageMargins<PdfPrinter.IHtmlSettings>, IPrintHeaderFooter<PdfPrinter.IHtmlSettings>, IOrientation<PdfPrinter.IHtmlSettings>, IPrintBackgrounds<PdfPrinter.IHtmlSettings>, IPrintSelectionOnly<PdfPrinter.IHtmlSettings>, IPaperSize<PdfPrinter.IHtmlSettings>, IHeaderTemplate<PdfPrinter.IHtmlSettings>, IFooterTemplate<PdfPrinter.IHtmlSettings>
```

##### Implements

[PdfPrinter.ISettings<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_ISettings_1), 
[IPrintSettings](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintSettings), 
[IPageRanges<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPageRanges_1), 
[IPagesPerSheet<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPagesPerSheet_1), 
[IPdfFilePath<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPdfFilePath_1), 
[IScaling<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IScaling_1), 
[IPageMargins<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPageMargins_1), 
[IPrintHeaderFooter<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintHeaderFooter_1), 
[IOrientation<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IOrientation_1), 
[IPrintBackgrounds<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintBackgrounds_1), 
[IPrintSelectionOnly<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintSelectionOnly_1), 
[IPaperSize<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPaperSize_1), 
[IHeaderTemplate<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IHeaderTemplate_1), 
[IFooterTemplate<PdfPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IFooterTemplate_1)

##### Extension Methods

[PrintSettingsExtensions.Apply<PdfPrinter.IHtmlSettings\>\(PdfPrinter.IHtmlSettings, Action<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSettingsExtensions_Apply__1___0_System_Action___0__), 
[PrintBackgroundsExtensions.DisablePrintingBackgrounds<PdfPrinter.IHtmlSettings\>\(IPrintBackgrounds<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintBackgroundsExtensions_DisablePrintingBackgrounds__1_DotNetBrowser_Print_Settings_IPrintBackgrounds___0__), 
[PrintHeaderFooterExtensions.DisablePrintingHeaderFooter<PdfPrinter.IHtmlSettings\>\(IPrintHeaderFooter<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintHeaderFooterExtensions_DisablePrintingHeaderFooter__1_DotNetBrowser_Print_Settings_IPrintHeaderFooter___0__), 
[PrintSelectionOnlyExtensions.DisablePrintingSelectionOnly<PdfPrinter.IHtmlSettings\>\(IPrintSelectionOnly<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSelectionOnlyExtensions_DisablePrintingSelectionOnly__1_DotNetBrowser_Print_Settings_IPrintSelectionOnly___0__), 
[PrintBackgroundsExtensions.EnablePrintingBackgrounds<PdfPrinter.IHtmlSettings\>\(IPrintBackgrounds<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintBackgroundsExtensions_EnablePrintingBackgrounds__1_DotNetBrowser_Print_Settings_IPrintBackgrounds___0__), 
[PrintHeaderFooterExtensions.EnablePrintingHeaderFooter<PdfPrinter.IHtmlSettings\>\(IPrintHeaderFooter<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintHeaderFooterExtensions_EnablePrintingHeaderFooter__1_DotNetBrowser_Print_Settings_IPrintHeaderFooter___0__), 
[PrintSelectionOnlyExtensions.EnablePrintingSelectionOnly<PdfPrinter.IHtmlSettings\>\(IPrintSelectionOnly<PdfPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSelectionOnlyExtensions_EnablePrintingSelectionOnly__1_DotNetBrowser_Print_Settings_IPrintSelectionOnly___0__), 
[FooterTemplateExtensions.SetFooterTemplate<PdfPrinter.IHtmlSettings\>\(IFooterTemplate<PdfPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_FooterTemplateExtensions_SetFooterTemplate__1_DotNetBrowser_Print_Settings_IFooterTemplate___0__System_String_), 
[HeaderTemplateExtensions.SetHeaderTemplate<PdfPrinter.IHtmlSettings\>\(IHeaderTemplate<PdfPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_HeaderTemplateExtensions_SetHeaderTemplate__1_DotNetBrowser_Print_Settings_IHeaderTemplate___0__System_String_), 
[OrientationExtensions.SetOrientation<PdfPrinter.IHtmlSettings\>\(IOrientation<PdfPrinter.IHtmlSettings\>, Orientation\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_OrientationExtensions_SetOrientation__1_DotNetBrowser_Print_Settings_IOrientation___0__DotNetBrowser_Print_Orientation_), 
[PageMarginsExtensions.SetPageMargins<PdfPrinter.IHtmlSettings\>\(IPageMargins<PdfPrinter.IHtmlSettings\>, PageMargins\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PageMarginsExtensions_SetPageMargins__1_DotNetBrowser_Print_Settings_IPageMargins___0__DotNetBrowser_Print_PageMargins_), 
[PageRangesExtensions.SetPageRanges<PdfPrinter.IHtmlSettings\>\(IPageRanges<PdfPrinter.IHtmlSettings\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PageRangesExtensions_SetPageRanges__1_DotNetBrowser_Print_Settings_IPageRanges___0__System_Collections_Generic_IReadOnlyCollection_DotNetBrowser_Print_PageRange__), 
[PagesPerSheetExtensions.SetPagesPerSheet<PdfPrinter.IHtmlSettings\>\(IPagesPerSheet<PdfPrinter.IHtmlSettings\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PagesPerSheetExtensions_SetPagesPerSheet__1_DotNetBrowser_Print_Settings_IPagesPerSheet___0__DotNetBrowser_Print_PagesPerSheet_), 
[PaperSizeExtensions.SetPaperSize<PdfPrinter.IHtmlSettings\>\(IPaperSize<PdfPrinter.IHtmlSettings\>, PaperSize\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PaperSizeExtensions_SetPaperSize__1_DotNetBrowser_Print_Settings_IPaperSize___0__DotNetBrowser_Print_PaperSize_), 
[PdfFilePathExtensions.SetPdfFilePath<PdfPrinter.IHtmlSettings\>\(IPdfFilePath<PdfPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PdfFilePathExtensions_SetPdfFilePath__1_DotNetBrowser_Print_Settings_IPdfFilePath___0__System_String_), 
[ScalingExtensions.SetScaling<PdfPrinter.IHtmlSettings\>\(IScaling<PdfPrinter.IHtmlSettings\>, Scaling\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ScalingExtensions_SetScaling__1_DotNetBrowser_Print_Settings_IScaling___0__DotNetBrowser_Print_Scaling_)

## <a id="DotNetBrowser_Print_PdfPrinter_IPdfSettings"></a> Interface PdfPrinter.IPdfSettings

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The print settings available when printing PDF content on the PDF printer.

```csharp
public interface PdfPrinter.IPdfSettings : PdfPrinter.ISettings<PdfPrinter.IPdfSettings>, IPrintSettings, IPageRanges<PdfPrinter.IPdfSettings>, IPagesPerSheet<PdfPrinter.IPdfSettings>, IPdfFilePath<PdfPrinter.IPdfSettings>, IScaling<PdfPrinter.IPdfSettings>
```

##### Implements

[PdfPrinter.ISettings<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_PdfPrinter_ISettings_1), 
[IPrintSettings](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintSettings), 
[IPageRanges<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPageRanges_1), 
[IPagesPerSheet<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPagesPerSheet_1), 
[IPdfFilePath<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPdfFilePath_1), 
[IScaling<PdfPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IScaling_1)

##### Extension Methods

[PrintSettingsExtensions.Apply<PdfPrinter.IPdfSettings\>\(PdfPrinter.IPdfSettings, Action<PdfPrinter.IPdfSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSettingsExtensions_Apply__1___0_System_Action___0__), 
[PageRangesExtensions.SetPageRanges<PdfPrinter.IPdfSettings\>\(IPageRanges<PdfPrinter.IPdfSettings\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PageRangesExtensions_SetPageRanges__1_DotNetBrowser_Print_Settings_IPageRanges___0__System_Collections_Generic_IReadOnlyCollection_DotNetBrowser_Print_PageRange__), 
[PagesPerSheetExtensions.SetPagesPerSheet<PdfPrinter.IPdfSettings\>\(IPagesPerSheet<PdfPrinter.IPdfSettings\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PagesPerSheetExtensions_SetPagesPerSheet__1_DotNetBrowser_Print_Settings_IPagesPerSheet___0__DotNetBrowser_Print_PagesPerSheet_), 
[PdfFilePathExtensions.SetPdfFilePath<PdfPrinter.IPdfSettings\>\(IPdfFilePath<PdfPrinter.IPdfSettings\>, string\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PdfFilePathExtensions_SetPdfFilePath__1_DotNetBrowser_Print_Settings_IPdfFilePath___0__System_String_), 
[ScalingExtensions.SetScaling<PdfPrinter.IPdfSettings\>\(IScaling<PdfPrinter.IPdfSettings\>, Scaling\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ScalingExtensions_SetScaling__1_DotNetBrowser_Print_Settings_IScaling___0__DotNetBrowser_Print_Scaling_)

## <a id="DotNetBrowser_Print_PdfPrinter_ISettings_1"></a> Interface PdfPrinter.ISettings<T\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The print settings available when printing HTML or PDF content on the PDF printer.

```csharp
public interface PdfPrinter.ISettings<out T> : IPrintSettings, IPageRanges<T>, IPagesPerSheet<T>, IPdfFilePath<T>, IScaling<T> where T : class, IPrintSettings
```

##### Type Parameters

`T` 

The specific print settings type.

##### Implements

[IPrintSettings](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintSettings), 
[IPageRanges<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPageRanges_1), 
[IPagesPerSheet<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPagesPerSheet_1), 
[IPdfFilePath<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPdfFilePath_1), 
[IScaling<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IScaling_1)

##### Extension Methods

[PrintSettingsExtensions.Apply<PdfPrinter.ISettings<T\>\>\(PdfPrinter.ISettings<T\>, Action<PdfPrinter.ISettings<T\>\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSettingsExtensions_Apply__1___0_System_Action___0__), 
[PageRangesExtensions.SetPageRanges<T\>\(IPageRanges<T\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PageRangesExtensions_SetPageRanges__1_DotNetBrowser_Print_Settings_IPageRanges___0__System_Collections_Generic_IReadOnlyCollection_DotNetBrowser_Print_PageRange__), 
[PagesPerSheetExtensions.SetPagesPerSheet<T\>\(IPagesPerSheet<T\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PagesPerSheetExtensions_SetPagesPerSheet__1_DotNetBrowser_Print_Settings_IPagesPerSheet___0__DotNetBrowser_Print_PagesPerSheet_), 
[PdfFilePathExtensions.SetPdfFilePath<T\>\(IPdfFilePath<T\>, string\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PdfFilePathExtensions_SetPdfFilePath__1_DotNetBrowser_Print_Settings_IPdfFilePath___0__System_String_), 
[ScalingExtensions.SetScaling<T\>\(IScaling<T\>, Scaling\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ScalingExtensions_SetScaling__1_DotNetBrowser_Print_Settings_IScaling___0__DotNetBrowser_Print_Scaling_)

## <a id="DotNetBrowser_Print_SystemPrinter_IHtmlSettings"></a> Interface SystemPrinter.IHtmlSettings

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

Print settings available when printing HTML content on a physical printer.

```csharp
public interface SystemPrinter.IHtmlSettings : SystemPrinter.ISettings<SystemPrinter.IHtmlSettings>, IPrintSettings, ICollate<SystemPrinter.IHtmlSettings>, IColorModel<SystemPrinter.IHtmlSettings>, ICopies<SystemPrinter.IHtmlSettings>, IDuplexMode<SystemPrinter.IHtmlSettings>, IPageRanges<SystemPrinter.IHtmlSettings>, IPagesPerSheet<SystemPrinter.IHtmlSettings>, IPaperSize<SystemPrinter.IHtmlSettings>, IScaling<SystemPrinter.IHtmlSettings>, IPageMargins<SystemPrinter.IHtmlSettings>, IPrintHeaderFooter<SystemPrinter.IHtmlSettings>, IOrientation<SystemPrinter.IHtmlSettings>, IPrintBackgrounds<SystemPrinter.IHtmlSettings>, IPrintSelectionOnly<SystemPrinter.IHtmlSettings>, IHeaderTemplate<SystemPrinter.IHtmlSettings>, IFooterTemplate<SystemPrinter.IHtmlSettings>
```

##### Implements

[SystemPrinter.ISettings<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_ISettings_1), 
[IPrintSettings](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintSettings), 
[ICollate<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ICollate_1), 
[IColorModel<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IColorModel_1), 
[ICopies<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ICopies_1), 
[IDuplexMode<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IDuplexMode_1), 
[IPageRanges<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPageRanges_1), 
[IPagesPerSheet<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPagesPerSheet_1), 
[IPaperSize<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPaperSize_1), 
[IScaling<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IScaling_1), 
[IPageMargins<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPageMargins_1), 
[IPrintHeaderFooter<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintHeaderFooter_1), 
[IOrientation<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IOrientation_1), 
[IPrintBackgrounds<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintBackgrounds_1), 
[IPrintSelectionOnly<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintSelectionOnly_1), 
[IHeaderTemplate<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IHeaderTemplate_1), 
[IFooterTemplate<SystemPrinter.IHtmlSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IFooterTemplate_1)

##### Extension Methods

[PrintSettingsExtensions.Apply<SystemPrinter.IHtmlSettings\>\(SystemPrinter.IHtmlSettings, Action<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSettingsExtensions_Apply__1___0_System_Action___0__), 
[CollateExtensions.DisableCollatePrinting<SystemPrinter.IHtmlSettings\>\(ICollate<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_CollateExtensions_DisableCollatePrinting__1_DotNetBrowser_Print_Settings_ICollate___0__), 
[PrintBackgroundsExtensions.DisablePrintingBackgrounds<SystemPrinter.IHtmlSettings\>\(IPrintBackgrounds<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintBackgroundsExtensions_DisablePrintingBackgrounds__1_DotNetBrowser_Print_Settings_IPrintBackgrounds___0__), 
[PrintHeaderFooterExtensions.DisablePrintingHeaderFooter<SystemPrinter.IHtmlSettings\>\(IPrintHeaderFooter<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintHeaderFooterExtensions_DisablePrintingHeaderFooter__1_DotNetBrowser_Print_Settings_IPrintHeaderFooter___0__), 
[PrintSelectionOnlyExtensions.DisablePrintingSelectionOnly<SystemPrinter.IHtmlSettings\>\(IPrintSelectionOnly<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSelectionOnlyExtensions_DisablePrintingSelectionOnly__1_DotNetBrowser_Print_Settings_IPrintSelectionOnly___0__), 
[CollateExtensions.EnableCollatePrinting<SystemPrinter.IHtmlSettings\>\(ICollate<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_CollateExtensions_EnableCollatePrinting__1_DotNetBrowser_Print_Settings_ICollate___0__), 
[PrintBackgroundsExtensions.EnablePrintingBackgrounds<SystemPrinter.IHtmlSettings\>\(IPrintBackgrounds<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintBackgroundsExtensions_EnablePrintingBackgrounds__1_DotNetBrowser_Print_Settings_IPrintBackgrounds___0__), 
[PrintHeaderFooterExtensions.EnablePrintingHeaderFooter<SystemPrinter.IHtmlSettings\>\(IPrintHeaderFooter<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintHeaderFooterExtensions_EnablePrintingHeaderFooter__1_DotNetBrowser_Print_Settings_IPrintHeaderFooter___0__), 
[PrintSelectionOnlyExtensions.EnablePrintingSelectionOnly<SystemPrinter.IHtmlSettings\>\(IPrintSelectionOnly<SystemPrinter.IHtmlSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSelectionOnlyExtensions_EnablePrintingSelectionOnly__1_DotNetBrowser_Print_Settings_IPrintSelectionOnly___0__), 
[ColorModelExtensions.SetColorModel<SystemPrinter.IHtmlSettings\>\(IColorModel<SystemPrinter.IHtmlSettings\>, ColorModel\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ColorModelExtensions_SetColorModel__1_DotNetBrowser_Print_Settings_IColorModel___0__DotNetBrowser_Print_ColorModel_), 
[CopiesExtensions.SetCopies<SystemPrinter.IHtmlSettings\>\(ICopies<SystemPrinter.IHtmlSettings\>, int\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_CopiesExtensions_SetCopies__1_DotNetBrowser_Print_Settings_ICopies___0__System_Int32_), 
[DuplexModeExtensions.SetDuplexMode<SystemPrinter.IHtmlSettings\>\(IDuplexMode<SystemPrinter.IHtmlSettings\>, DuplexMode\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_DuplexModeExtensions_SetDuplexMode__1_DotNetBrowser_Print_Settings_IDuplexMode___0__DotNetBrowser_Print_DuplexMode_), 
[FooterTemplateExtensions.SetFooterTemplate<SystemPrinter.IHtmlSettings\>\(IFooterTemplate<SystemPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_FooterTemplateExtensions_SetFooterTemplate__1_DotNetBrowser_Print_Settings_IFooterTemplate___0__System_String_), 
[HeaderTemplateExtensions.SetHeaderTemplate<SystemPrinter.IHtmlSettings\>\(IHeaderTemplate<SystemPrinter.IHtmlSettings\>, string\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_HeaderTemplateExtensions_SetHeaderTemplate__1_DotNetBrowser_Print_Settings_IHeaderTemplate___0__System_String_), 
[OrientationExtensions.SetOrientation<SystemPrinter.IHtmlSettings\>\(IOrientation<SystemPrinter.IHtmlSettings\>, Orientation\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_OrientationExtensions_SetOrientation__1_DotNetBrowser_Print_Settings_IOrientation___0__DotNetBrowser_Print_Orientation_), 
[PageMarginsExtensions.SetPageMargins<SystemPrinter.IHtmlSettings\>\(IPageMargins<SystemPrinter.IHtmlSettings\>, PageMargins\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PageMarginsExtensions_SetPageMargins__1_DotNetBrowser_Print_Settings_IPageMargins___0__DotNetBrowser_Print_PageMargins_), 
[PageRangesExtensions.SetPageRanges<SystemPrinter.IHtmlSettings\>\(IPageRanges<SystemPrinter.IHtmlSettings\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PageRangesExtensions_SetPageRanges__1_DotNetBrowser_Print_Settings_IPageRanges___0__System_Collections_Generic_IReadOnlyCollection_DotNetBrowser_Print_PageRange__), 
[PagesPerSheetExtensions.SetPagesPerSheet<SystemPrinter.IHtmlSettings\>\(IPagesPerSheet<SystemPrinter.IHtmlSettings\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PagesPerSheetExtensions_SetPagesPerSheet__1_DotNetBrowser_Print_Settings_IPagesPerSheet___0__DotNetBrowser_Print_PagesPerSheet_), 
[PaperSizeExtensions.SetPaperSize<SystemPrinter.IHtmlSettings\>\(IPaperSize<SystemPrinter.IHtmlSettings\>, PaperSize\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PaperSizeExtensions_SetPaperSize__1_DotNetBrowser_Print_Settings_IPaperSize___0__DotNetBrowser_Print_PaperSize_), 
[ScalingExtensions.SetScaling<SystemPrinter.IHtmlSettings\>\(IScaling<SystemPrinter.IHtmlSettings\>, Scaling\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ScalingExtensions_SetScaling__1_DotNetBrowser_Print_Settings_IScaling___0__DotNetBrowser_Print_Scaling_)

## <a id="DotNetBrowser_Print_SystemPrinter_IPdfSettings"></a> Interface SystemPrinter.IPdfSettings

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

Print settings available when printing PDF content on a physical printer.

```csharp
public interface SystemPrinter.IPdfSettings : SystemPrinter.ISettings<SystemPrinter.IPdfSettings>, IPrintSettings, ICollate<SystemPrinter.IPdfSettings>, IColorModel<SystemPrinter.IPdfSettings>, ICopies<SystemPrinter.IPdfSettings>, IDuplexMode<SystemPrinter.IPdfSettings>, IPageRanges<SystemPrinter.IPdfSettings>, IPagesPerSheet<SystemPrinter.IPdfSettings>, IPaperSize<SystemPrinter.IPdfSettings>, IScaling<SystemPrinter.IPdfSettings>, IFit<SystemPrinter.IPdfSettings>
```

##### Implements

[SystemPrinter.ISettings<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.md#DotNetBrowser_Print_SystemPrinter_ISettings_1), 
[IPrintSettings](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintSettings), 
[ICollate<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ICollate_1), 
[IColorModel<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IColorModel_1), 
[ICopies<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ICopies_1), 
[IDuplexMode<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IDuplexMode_1), 
[IPageRanges<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPageRanges_1), 
[IPagesPerSheet<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPagesPerSheet_1), 
[IPaperSize<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPaperSize_1), 
[IScaling<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IScaling_1), 
[IFit<SystemPrinter.IPdfSettings\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IFit_1)

##### Extension Methods

[PrintSettingsExtensions.Apply<SystemPrinter.IPdfSettings\>\(SystemPrinter.IPdfSettings, Action<SystemPrinter.IPdfSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSettingsExtensions_Apply__1___0_System_Action___0__), 
[CollateExtensions.DisableCollatePrinting<SystemPrinter.IPdfSettings\>\(ICollate<SystemPrinter.IPdfSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_CollateExtensions_DisableCollatePrinting__1_DotNetBrowser_Print_Settings_ICollate___0__), 
[CollateExtensions.EnableCollatePrinting<SystemPrinter.IPdfSettings\>\(ICollate<SystemPrinter.IPdfSettings\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_CollateExtensions_EnableCollatePrinting__1_DotNetBrowser_Print_Settings_ICollate___0__), 
[ColorModelExtensions.SetColorModel<SystemPrinter.IPdfSettings\>\(IColorModel<SystemPrinter.IPdfSettings\>, ColorModel\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ColorModelExtensions_SetColorModel__1_DotNetBrowser_Print_Settings_IColorModel___0__DotNetBrowser_Print_ColorModel_), 
[CopiesExtensions.SetCopies<SystemPrinter.IPdfSettings\>\(ICopies<SystemPrinter.IPdfSettings\>, int\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_CopiesExtensions_SetCopies__1_DotNetBrowser_Print_Settings_ICopies___0__System_Int32_), 
[DuplexModeExtensions.SetDuplexMode<SystemPrinter.IPdfSettings\>\(IDuplexMode<SystemPrinter.IPdfSettings\>, DuplexMode\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_DuplexModeExtensions_SetDuplexMode__1_DotNetBrowser_Print_Settings_IDuplexMode___0__DotNetBrowser_Print_DuplexMode_), 
[FitExtensions.SetFit<SystemPrinter.IPdfSettings\>\(IFit<SystemPrinter.IPdfSettings\>, Fit\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_FitExtensions_SetFit__1_DotNetBrowser_Print_Settings_IFit___0__DotNetBrowser_Print_Fit_), 
[PageRangesExtensions.SetPageRanges<SystemPrinter.IPdfSettings\>\(IPageRanges<SystemPrinter.IPdfSettings\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PageRangesExtensions_SetPageRanges__1_DotNetBrowser_Print_Settings_IPageRanges___0__System_Collections_Generic_IReadOnlyCollection_DotNetBrowser_Print_PageRange__), 
[PagesPerSheetExtensions.SetPagesPerSheet<SystemPrinter.IPdfSettings\>\(IPagesPerSheet<SystemPrinter.IPdfSettings\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PagesPerSheetExtensions_SetPagesPerSheet__1_DotNetBrowser_Print_Settings_IPagesPerSheet___0__DotNetBrowser_Print_PagesPerSheet_), 
[PaperSizeExtensions.SetPaperSize<SystemPrinter.IPdfSettings\>\(IPaperSize<SystemPrinter.IPdfSettings\>, PaperSize\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PaperSizeExtensions_SetPaperSize__1_DotNetBrowser_Print_Settings_IPaperSize___0__DotNetBrowser_Print_PaperSize_), 
[ScalingExtensions.SetScaling<SystemPrinter.IPdfSettings\>\(IScaling<SystemPrinter.IPdfSettings\>, Scaling\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ScalingExtensions_SetScaling__1_DotNetBrowser_Print_Settings_IScaling___0__DotNetBrowser_Print_Scaling_)

## <a id="DotNetBrowser_Print_SystemPrinter_ISettings_1"></a> Interface SystemPrinter.ISettings<T\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

Print settings available when printing HTML or PDF content on a physical printer.

```csharp
public interface SystemPrinter.ISettings<out T> : IPrintSettings, ICollate<T>, IColorModel<T>, ICopies<T>, IDuplexMode<T>, IPageRanges<T>, IPagesPerSheet<T>, IPaperSize<T>, IScaling<T> where T : class, IPrintSettings
```

##### Type Parameters

`T` 

The specific print settings type.

##### Implements

[IPrintSettings](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPrintSettings), 
[ICollate<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ICollate_1), 
[IColorModel<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IColorModel_1), 
[ICopies<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ICopies_1), 
[IDuplexMode<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IDuplexMode_1), 
[IPageRanges<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPageRanges_1), 
[IPagesPerSheet<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPagesPerSheet_1), 
[IPaperSize<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IPaperSize_1), 
[IScaling<T\>](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_IScaling_1)

##### Extension Methods

[PrintSettingsExtensions.Apply<SystemPrinter.ISettings<T\>\>\(SystemPrinter.ISettings<T\>, Action<SystemPrinter.ISettings<T\>\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PrintSettingsExtensions_Apply__1___0_System_Action___0__), 
[CollateExtensions.DisableCollatePrinting<T\>\(ICollate<T\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_CollateExtensions_DisableCollatePrinting__1_DotNetBrowser_Print_Settings_ICollate___0__), 
[CollateExtensions.EnableCollatePrinting<T\>\(ICollate<T\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_CollateExtensions_EnableCollatePrinting__1_DotNetBrowser_Print_Settings_ICollate___0__), 
[ColorModelExtensions.SetColorModel<T\>\(IColorModel<T\>, ColorModel\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ColorModelExtensions_SetColorModel__1_DotNetBrowser_Print_Settings_IColorModel___0__DotNetBrowser_Print_ColorModel_), 
[CopiesExtensions.SetCopies<T\>\(ICopies<T\>, int\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_CopiesExtensions_SetCopies__1_DotNetBrowser_Print_Settings_ICopies___0__System_Int32_), 
[DuplexModeExtensions.SetDuplexMode<T\>\(IDuplexMode<T\>, DuplexMode\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_DuplexModeExtensions_SetDuplexMode__1_DotNetBrowser_Print_Settings_IDuplexMode___0__DotNetBrowser_Print_DuplexMode_), 
[PageRangesExtensions.SetPageRanges<T\>\(IPageRanges<T\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PageRangesExtensions_SetPageRanges__1_DotNetBrowser_Print_Settings_IPageRanges___0__System_Collections_Generic_IReadOnlyCollection_DotNetBrowser_Print_PageRange__), 
[PagesPerSheetExtensions.SetPagesPerSheet<T\>\(IPagesPerSheet<T\>, PagesPerSheet\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PagesPerSheetExtensions_SetPagesPerSheet__1_DotNetBrowser_Print_Settings_IPagesPerSheet___0__DotNetBrowser_Print_PagesPerSheet_), 
[PaperSizeExtensions.SetPaperSize<T\>\(IPaperSize<T\>, PaperSize\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_PaperSizeExtensions_SetPaperSize__1_DotNetBrowser_Print_Settings_IPaperSize___0__DotNetBrowser_Print_PaperSize_), 
[ScalingExtensions.SetScaling<T\>\(IScaling<T\>, Scaling\)](DotNetBrowser.Print.Settings.md#DotNetBrowser_Print_Settings_ScalingExtensions_SetScaling__1_DotNetBrowser_Print_Settings_IScaling___0__DotNetBrowser_Print_Scaling_)

## <a id="DotNetBrowser_Print_ColorModel"></a> Enum ColorModel

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The color models used for printing.

```csharp
public enum ColorModel
```

### Fields

`Black = 8` 

BLACK color model.



`BrotherBrScript3Black = 25` 

BROTHER_BR_SCRIPT_3_BLACK color model. Used in Brother BRScript3 color printer PPDs.



`BrotherBrScript3Color = 24` 

BROTHER_BR_SCRIPT_3_COLOR color model. Used in Brother BRScript3 color printer PPDs.



`BrotherCupsColor = 22` 

BROTHER_CUPS_COLOR color model. Used in Brother color laser printer PPDs.



`BrotherCupsMono = 23` 

BROTHER_CUPS_MONO color model. Used in Brother color laser printer PPDs.



`CanonCnColorModeColor = 32` 

Used in Canon CN printer PPDs.



`CanonCnColorModeMono = 33` 

Used in Canon CN printer PPDs.



`CanonCnijGrayScaleOne = 34` 

Used in Canon CNIJ printer PPDs.



`CanonCnijGrayScaleZero = 35` 

Used in Canon CNIJ printer PPDs.



`Cmy = 5` 

CMY color model.



`CmyPlusK = 7` 

CMYPlusK represents CMY+K color model.



`Cmyk = 4` 

CMYK color model.



`Color = 3` 

COLOR color model.



`ColorModeColor = 13` 

COLOR_MODE_COLOR color model. Used in Samsung printer PPDs.



`ColorModeMonochrome = 14` 

COLOR_MODE_MONOCHROME color model. Used in Samsung printer PPDs.



`EpsonInkColor = 26` 

Used in Epson printer PPDs.



`EpsonInkMono = 27` 

Used in Epson printer PPDs.



`Gray = 2` 

GRAY color model.



`Grayscale = 9` 

GRAYSCALE color model.



`HpColorBlack = 16` 

HP_COLOR_BLACK color model. Used in HP color printer PPDs.



`HpColorColor = 15` 

HP_COLOR_COLOR color model. Used in HP color printer PPDs.



`HpPjlColorAsGrayNo = 42` 

Used in HP printer PPDs.



`HpPjlColorAsGrayYes = 43` 

Used in HP printer PPDs.



`Kcmy = 6` 

KCMY color model.



`KonicaMinoltaSelectColorColor = 36` 

Used in Konica Minolta printer PPDs.



`KonicaMinoltaSelectColorGrayscale = 37` 

Used in Konica Minolta printer PPDs.



`OkiOkControlColor = 38` 

Used in OKI printer PPDs.



`OkiOkControlGray = 39` 

Used in OKI printer PPDs.



`PrintoutModeNormal = 17` 

PRINTOUT_MODE_NORMAL color model. Used in Foomatic PPDs.



`PrintoutModeNormalGray = 18` 

PRINTOUT_MODE_NORMAL_GRAY color model. Used in Foomatic PPDs.



`ProcessColorModelCmyk = 19` 

PROCESS_COLOR_MODEL_CMYK color model. Used in Canon printer PPDs.



`ProcessColorModelGreyscale = 20` 

PROCESS_COLOR_MODEL_GREYSCALE color model. Used in Canon printer PPDs.



`ProcessColorModelRgb = 21` 

PROCESS_COLOR_MODEL_RGB color model. Used in Canon printer PPDs



`Rgb = 10` 

RGB color model.



`Rgb16 = 11` 

RGB16 color model.



`Rgba = 12` 

RGBA color model.



`SharpArcModeCmBw = 29` 

Used in Sharp printer PPDs.



`SharpArcModeCmColor = 28` 

Used in Sharp printer PPDs.



`Unknown = 1` 

Reserved value.



`XeroxXrOutputControlPrintAsColor = 40` 

Used in Xerox printer PPDs.



`XeroxXrOutputControlPrintAsGrayscale = 41` 

Used in Xerox printer PPDs.



`XeroxXrxColorAutomatic = 30` 

Used in Xerox printer PPDs.



`XeroxXrxColorBw = 31` 

Used in Xerox printer PPDs.

## <a id="DotNetBrowser_Print_DuplexMode"></a> Enum DuplexMode

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The duplex modes used for printing.

```csharp
public enum DuplexMode
```

### Fields

`LongEdge = 3` 

Two-sided printing, flipping on the long edge.



`ShortEdge = 4` 

Two-sided printing, flipping on the short edge.



`Simplex = 2` 

One-sided printing.



`Unknown = 1` 

The duplex mode is unknown.

## <a id="DotNetBrowser_Print_Fit"></a> Enum Fit

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The content fit used for printing.

```csharp
public enum Fit
```

### Fields

`ToPage = 1` 

Fit the content of the page.



`ToPaper = 2` 

Fit the content of the paper.

## <a id="DotNetBrowser_Print_Orientation"></a> Enum Orientation

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The page orientation values used for printing.

```csharp
public enum Orientation
```

### Fields

`Landscape = 1` 

The landscape orientation.



`Portrait = 2` 

The portrait orientation.

## <a id="DotNetBrowser_Print_PagesPerSheet"></a> Enum PagesPerSheet

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The pages per sheet values that Chromium supports.

```csharp
public enum PagesPerSheet
```

### Fields

`Four = 4` 

Four pages per sheet.



`Nine = 9` 

Nine pages per sheet.



`One = 1` 

One page per sheet.



`Six = 6` 

Six pages per sheet.



`Sixteen = 16` 

Sixteen pages per sheet.



`Two = 2` 

Two pages per sheet.

## <a id="DotNetBrowser_Print_PaperSize_Unit"></a> Enum PaperSize.Unit

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The measurement unit of the paper size.

```csharp
public enum PaperSize.Unit
```

### Fields

`Inches = 1` 

The paper size is measured in inches.



`Microns = 2` 

The paper size is measured in microns.



`Millimeters = 0` 

The paper size is measured in millimeters.
