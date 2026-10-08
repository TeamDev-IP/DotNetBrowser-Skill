# <a id="DotNetBrowser_Print_Settings_IPageMargins_1"></a> Interface IPageMargins<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the page margins.

```csharp
public interface IPageMargins<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[PageMarginsExtensions.SetPageMargins<TPrintSettings\>\(IPageMargins<TPrintSettings\>, PageMargins\)](DotNetBrowser.Print.Settings.PageMarginsExtensions.md\#DotNetBrowser\_Print\_Settings\_PageMarginsExtensions\_SetPageMargins\_\_1\_DotNetBrowser\_Print\_Settings\_IPageMargins\_\_\_0\_\_DotNetBrowser\_Print\_PageMargins\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
the page margins.

## Properties

### <a id="DotNetBrowser_Print_Settings_IPageMargins_1_PageMargins"></a> PageMargins

Gets or sets the page margins for printing.

```csharp
PageMargins PageMargins { get; set; }
```

#### Property Value

 [PageMargins](DotNetBrowser.Print.PageMargins.md)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified page margins is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified page margins is not supported by the printer.

