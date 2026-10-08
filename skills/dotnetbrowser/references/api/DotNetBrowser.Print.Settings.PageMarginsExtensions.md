# <a id="DotNetBrowser_Print_Settings_PageMarginsExtensions"></a> Class PageMarginsExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IPageMargins%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class PageMarginsExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PageMarginsExtensions](DotNetBrowser.Print.Settings.PageMarginsExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_PageMarginsExtensions_SetPageMargins__1_DotNetBrowser_Print_Settings_IPageMargins___0__DotNetBrowser_Print_PageMargins_"></a> SetPageMargins<TPrintSettings\>\(IPageMargins<TPrintSettings\>, PageMargins\)

Configures the page margins for printing

```csharp
public static TPrintSettings SetPageMargins<TPrintSettings>(this IPageMargins<TPrintSettings> obj, PageMargins pageMargins) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPageMargins](DotNetBrowser.Print.Settings.IPageMargins\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPageMargins%601" data-throw-if-not-resolved="false"></xref> implementation.

`pageMargins` [PageMargins](DotNetBrowser.Print.PageMargins.md)

The page margins for printing.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified page margins is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified page margins is not supported by the printer.

