# <a id="DotNetBrowser_Print_Settings_IPdfFilePath_1"></a> Interface IPdfFilePath<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the destination PDF file path.

```csharp
public interface IPdfFilePath<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[PdfFilePathExtensions.SetPdfFilePath<TPrintSettings\>\(IPdfFilePath<TPrintSettings\>, string\)](DotNetBrowser.Print.Settings.PdfFilePathExtensions.md\#DotNetBrowser\_Print\_Settings\_PdfFilePathExtensions\_SetPdfFilePath\_\_1\_DotNetBrowser\_Print\_Settings\_IPdfFilePath\_\_\_0\_\_System\_String\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support
configuring the destination PDF file path.

## Properties

### <a id="DotNetBrowser_Print_Settings_IPdfFilePath_1_PdfFilePath"></a> PdfFilePath

Gets or sets the full PDF file path.

```csharp
string PdfFilePath { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified file path is null, empty, or contain only white space.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The parent directory for the PDF file does not exist and cannot be created.

