# <a id="DotNetBrowser_Print_Settings_DuplexModeExtensions"></a> Class DuplexModeExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IDuplexMode%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class DuplexModeExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DuplexModeExtensions](DotNetBrowser.Print.Settings.DuplexModeExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_DuplexModeExtensions_SetDuplexMode__1_DotNetBrowser_Print_Settings_IDuplexMode___0__DotNetBrowser_Print_DuplexMode_"></a> SetDuplexMode<TPrintSettings\>\(IDuplexMode<TPrintSettings\>, DuplexMode\)

Sets the duplex mode.

```csharp
public static TPrintSettings SetDuplexMode<TPrintSettings>(this IDuplexMode<TPrintSettings> obj, DuplexMode duplexMode) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IDuplexMode](DotNetBrowser.Print.Settings.IDuplexMode\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IDuplexMode%601" data-throw-if-not-resolved="false"></xref> implementation.

`duplexMode` [DuplexMode](DotNetBrowser.Print.DuplexMode.md)

The duplex mode used for printing.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified duplex mode is not supported by the printer.

