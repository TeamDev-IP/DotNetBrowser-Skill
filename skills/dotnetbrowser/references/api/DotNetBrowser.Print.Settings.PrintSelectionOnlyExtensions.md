# <a id="DotNetBrowser_Print_Settings_PrintSelectionOnlyExtensions"></a> Class PrintSelectionOnlyExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IPrintSelectionOnly%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class PrintSelectionOnlyExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintSelectionOnlyExtensions](DotNetBrowser.Print.Settings.PrintSelectionOnlyExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_PrintSelectionOnlyExtensions_DisablePrintingSelectionOnly__1_DotNetBrowser_Print_Settings_IPrintSelectionOnly___0__"></a> DisablePrintingSelectionOnly<TPrintSettings\>\(IPrintSelectionOnly<TPrintSettings\>\)

Disables printing only the selected content.

```csharp
public static TPrintSettings DisablePrintingSelectionOnly<TPrintSettings>(this IPrintSelectionOnly<TPrintSettings> obj) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPrintSelectionOnly](DotNetBrowser.Print.Settings.IPrintSelectionOnly\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPrintSelectionOnly%601" data-throw-if-not-resolved="false"></xref> implementation.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Only the selected content printing is not supported by the printer.

### <a id="DotNetBrowser_Print_Settings_PrintSelectionOnlyExtensions_EnablePrintingSelectionOnly__1_DotNetBrowser_Print_Settings_IPrintSelectionOnly___0__"></a> EnablePrintingSelectionOnly<TPrintSettings\>\(IPrintSelectionOnly<TPrintSettings\>\)

Enables printing only the selected content.

```csharp
public static TPrintSettings EnablePrintingSelectionOnly<TPrintSettings>(this IPrintSelectionOnly<TPrintSettings> obj) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPrintSelectionOnly](DotNetBrowser.Print.Settings.IPrintSelectionOnly\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPrintSelectionOnly%601" data-throw-if-not-resolved="false"></xref> implementation.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Only the selected content printing is not supported by the printer.

