# <a id="DotNetBrowser_Print_Settings_IDuplexMode_1"></a> Interface IDuplexMode<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the duplex mode for printing.

```csharp
public interface IDuplexMode<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[DuplexModeExtensions.SetDuplexMode<TPrintSettings\>\(IDuplexMode<TPrintSettings\>, DuplexMode\)](DotNetBrowser.Print.Settings.DuplexModeExtensions.md\#DotNetBrowser\_Print\_Settings\_DuplexModeExtensions\_SetDuplexMode\_\_1\_DotNetBrowser\_Print\_Settings\_IDuplexMode\_\_\_0\_\_DotNetBrowser\_Print\_DuplexMode\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support specifying
duplex mode.

## Properties

### <a id="DotNetBrowser_Print_Settings_IDuplexMode_1_DuplexMode"></a> DuplexMode

Gets or sets the duplex mode.

```csharp
DuplexMode DuplexMode { get; set; }
```

#### Property Value

 [DuplexMode](DotNetBrowser.Print.DuplexMode.md)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified duplex mode is not supported by the printer.

