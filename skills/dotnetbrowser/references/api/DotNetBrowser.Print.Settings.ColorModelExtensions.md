# <a id="DotNetBrowser_Print_Settings_ColorModelExtensions"></a> Class ColorModelExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IColorModel%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class ColorModelExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ColorModelExtensions](DotNetBrowser.Print.Settings.ColorModelExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_ColorModelExtensions_SetColorModel__1_DotNetBrowser_Print_Settings_IColorModel___0__DotNetBrowser_Print_ColorModel_"></a> SetColorModel<TPrintSettings\>\(IColorModel<TPrintSettings\>, ColorModel\)

Sets the color model used for printing.

```csharp
public static TPrintSettings SetColorModel<TPrintSettings>(this IColorModel<TPrintSettings> obj, ColorModel colorModel) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IColorModel](DotNetBrowser.Print.Settings.IColorModel\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IColorModel%601" data-throw-if-not-resolved="false"></xref> implementation.

`colorModel` [ColorModel](DotNetBrowser.Print.ColorModel.md)

The color model used for printing.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified color model is not supported by the printer.

