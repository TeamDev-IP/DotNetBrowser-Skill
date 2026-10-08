# <a id="DotNetBrowser_Print_Settings_IOrientation_1"></a> Interface IOrientation<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the page orientation.

```csharp
public interface IOrientation<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[OrientationExtensions.SetOrientation<TPrintSettings\>\(IOrientation<TPrintSettings\>, Orientation\)](DotNetBrowser.Print.Settings.OrientationExtensions.md\#DotNetBrowser\_Print\_Settings\_OrientationExtensions\_SetOrientation\_\_1\_DotNetBrowser\_Print\_Settings\_IOrientation\_\_\_0\_\_DotNetBrowser\_Print\_Orientation\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
the page orientation.

## Properties

### <a id="DotNetBrowser_Print_Settings_IOrientation_1_Orientation"></a> Orientation

Gets or sets the page orientation.

```csharp
Orientation Orientation { get; set; }
```

#### Property Value

 [Orientation](DotNetBrowser.Print.Orientation.md)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified page orientation is not supported by the printer.

