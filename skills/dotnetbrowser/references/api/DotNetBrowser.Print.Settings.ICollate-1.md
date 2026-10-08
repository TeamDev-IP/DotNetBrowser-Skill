# <a id="DotNetBrowser_Print_Settings_ICollate_1"></a> Interface ICollate<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring collate printing.

```csharp
public interface ICollate<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[CollateExtensions.DisableCollatePrinting<TPrintSettings\>\(ICollate<TPrintSettings\>\)](DotNetBrowser.Print.Settings.CollateExtensions.md\#DotNetBrowser\_Print\_Settings\_CollateExtensions\_DisableCollatePrinting\_\_1\_DotNetBrowser\_Print\_Settings\_ICollate\_\_\_0\_\_), 
[CollateExtensions.EnableCollatePrinting<TPrintSettings\>\(ICollate<TPrintSettings\>\)](DotNetBrowser.Print.Settings.CollateExtensions.md\#DotNetBrowser\_Print\_Settings\_CollateExtensions\_EnableCollatePrinting\_\_1\_DotNetBrowser\_Print\_Settings\_ICollate\_\_\_0\_\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support collate
printing.

## Properties

### <a id="DotNetBrowser_Print_Settings_ICollate_1_CollatePrintingEnabled"></a> CollatePrintingEnabled

Enables or disables collate printing.

```csharp
bool CollatePrintingEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Collate is not supported by the printer.

