# <a id="DotNetBrowser_Print_Settings_IFit_1"></a> Interface IFit<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the content fit for printing.

```csharp
public interface IFit<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[FitExtensions.SetFit<TPrintSettings\>\(IFit<TPrintSettings\>, Fit\)](DotNetBrowser.Print.Settings.FitExtensions.md\#DotNetBrowser\_Print\_Settings\_FitExtensions\_SetFit\_\_1\_DotNetBrowser\_Print\_Settings\_IFit\_\_\_0\_\_DotNetBrowser\_Print\_Fit\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
the content fit for printing.

## Properties

### <a id="DotNetBrowser_Print_Settings_IFit_1_Fit"></a> Fit

Gets or sets the content fit for printing.

```csharp
Fit Fit { get; set; }
```

#### Property Value

 [Fit](DotNetBrowser.Print.Fit.md)

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The specified fit is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified fit is not supported by the printer.

