# <a id="DotNetBrowser_Print_Settings_IColorModel_1"></a> Interface IColorModel<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the color model for printing.

```csharp
public interface IColorModel<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[ColorModelExtensions.SetColorModel<TPrintSettings\>\(IColorModel<TPrintSettings\>, ColorModel\)](DotNetBrowser.Print.Settings.ColorModelExtensions.md\#DotNetBrowser\_Print\_Settings\_ColorModelExtensions\_SetColorModel\_\_1\_DotNetBrowser\_Print\_Settings\_IColorModel\_\_\_0\_\_DotNetBrowser\_Print\_ColorModel\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support color models.

## Properties

### <a id="DotNetBrowser_Print_Settings_IColorModel_1_ColorModel"></a> ColorModel

Gets or sets the color model.

```csharp
ColorModel ColorModel { get; set; }
```

#### Property Value

 [ColorModel](DotNetBrowser.Print.ColorModel.md)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified color model is not supported by the printer.

