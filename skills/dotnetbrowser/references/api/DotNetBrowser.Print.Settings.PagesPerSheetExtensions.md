# <a id="DotNetBrowser_Print_Settings_PagesPerSheetExtensions"></a> Class PagesPerSheetExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IPagesPerSheet%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class PagesPerSheetExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PagesPerSheetExtensions](DotNetBrowser.Print.Settings.PagesPerSheetExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_PagesPerSheetExtensions_SetPagesPerSheet__1_DotNetBrowser_Print_Settings_IPagesPerSheet___0__DotNetBrowser_Print_PagesPerSheet_"></a> SetPagesPerSheet<TPrintSettings\>\(IPagesPerSheet<TPrintSettings\>, PagesPerSheet\)

Sets the number of pages per sheet.

```csharp
public static TPrintSettings SetPagesPerSheet<TPrintSettings>(this IPagesPerSheet<TPrintSettings> obj, PagesPerSheet pagesPerSheet) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPagesPerSheet](DotNetBrowser.Print.Settings.IPagesPerSheet\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPagesPerSheet%601" data-throw-if-not-resolved="false"></xref> implementation.

`pagesPerSheet` [PagesPerSheet](DotNetBrowser.Print.PagesPerSheet.md)

The new number of pages per sheet.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified number of pages per sheet is not supported by the printer.

