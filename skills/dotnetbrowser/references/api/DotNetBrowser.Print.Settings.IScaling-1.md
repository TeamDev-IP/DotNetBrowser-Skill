# <a id="DotNetBrowser_Print_Settings_IScaling_1"></a> Interface IScaling<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the scaling for printing.

```csharp
public interface IScaling<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[ScalingExtensions.SetScaling<TPrintSettings\>\(IScaling<TPrintSettings\>, Scaling\)](DotNetBrowser.Print.Settings.ScalingExtensions.md\#DotNetBrowser\_Print\_Settings\_ScalingExtensions\_SetScaling\_\_1\_DotNetBrowser\_Print\_Settings\_IScaling\_\_\_0\_\_DotNetBrowser\_Print\_Scaling\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
the scaling for printing.

## Properties

### <a id="DotNetBrowser_Print_Settings_IScaling_1_Scaling"></a> Scaling

Gets or sets the scaling for printing.

```csharp
Scaling Scaling { get; set; }
```

#### Property Value

 [Scaling](DotNetBrowser.Print.Scaling.md)

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The specified scaling is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified scaling is not supported by the printer.

