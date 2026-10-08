# <a id="DotNetBrowser_Print_Printer_1"></a> Class Printer<TPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The base class for the printers.

```csharp
public abstract class Printer<TPrintSettings> : IAutoDisposable where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The print settings type available for this printer.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Printer<TPrintSettings\>](DotNetBrowser.Print.Printer\-1.md)

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Print_Printer_1_Capabilities"></a> Capabilities

Gets the capabilities of this printer.

```csharp
public Capabilities Capabilities { get; }
```

#### Property Value

 [Capabilities](DotNetBrowser.Print.Capabilities.md)

### <a id="DotNetBrowser_Print_Printer_1_DeviceName"></a> DeviceName

Gets the device name of this printer.

```csharp
public string DeviceName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Print_Printer_1_IsDefault"></a> IsDefault

Indicates whether this printer is the default system printer.

```csharp
public bool IsDefault { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Print_Printer_1_PrintJob"></a> PrintJob

Gets the current print job. This print job can be used to configure print settings.

```csharp
public IPrintJob<TPrintSettings> PrintJob { get; }
```

#### Property Value

 [IPrintJob](DotNetBrowser.Print.IPrintJob\-1.md)<TPrintSettings\>

