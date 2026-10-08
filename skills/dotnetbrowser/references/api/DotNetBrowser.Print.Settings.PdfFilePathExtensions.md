# <a id="DotNetBrowser_Print_Settings_PdfFilePathExtensions"></a> Class PdfFilePathExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IPdfFilePath%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class PdfFilePathExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PdfFilePathExtensions](DotNetBrowser.Print.Settings.PdfFilePathExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_PdfFilePathExtensions_SetPdfFilePath__1_DotNetBrowser_Print_Settings_IPdfFilePath___0__System_String_"></a> SetPdfFilePath<TPrintSettings\>\(IPdfFilePath<TPrintSettings\>, string\)

Sets the full PDF file path.

```csharp
public static TPrintSettings SetPdfFilePath<TPrintSettings>(this IPdfFilePath<TPrintSettings> obj, string pdfFilePath) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPdfFilePath](DotNetBrowser.Print.Settings.IPdfFilePath\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPdfFilePath%601" data-throw-if-not-resolved="false"></xref> implementation.

`pdfFilePath` [string](https://learn.microsoft.com/dotnet/api/system.string)

The full PDF file path. Cannot be null, empty, or contain only white space.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified file path is null, empty, or contain only white space.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The parent directory for the PDF file does not exist and cannot be created.

