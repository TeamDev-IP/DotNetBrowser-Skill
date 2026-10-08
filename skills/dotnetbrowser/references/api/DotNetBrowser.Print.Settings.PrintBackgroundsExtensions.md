# <a id="DotNetBrowser_Print_Settings_PrintBackgroundsExtensions"></a> Class PrintBackgroundsExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IPrintBackgrounds%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class PrintBackgroundsExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintBackgroundsExtensions](DotNetBrowser.Print.Settings.PrintBackgroundsExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_PrintBackgroundsExtensions_DisablePrintingBackgrounds__1_DotNetBrowser_Print_Settings_IPrintBackgrounds___0__"></a> DisablePrintingBackgrounds<TPrintSettings\>\(IPrintBackgrounds<TPrintSettings\>\)

Disables printing background graphics.

```csharp
public static TPrintSettings DisablePrintingBackgrounds<TPrintSettings>(this IPrintBackgrounds<TPrintSettings> obj) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPrintBackgrounds](DotNetBrowser.Print.Settings.IPrintBackgrounds\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPrintBackgrounds%601" data-throw-if-not-resolved="false"></xref> implementation.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The background graphics printing is not supported by the printer.

### <a id="DotNetBrowser_Print_Settings_PrintBackgroundsExtensions_EnablePrintingBackgrounds__1_DotNetBrowser_Print_Settings_IPrintBackgrounds___0__"></a> EnablePrintingBackgrounds<TPrintSettings\>\(IPrintBackgrounds<TPrintSettings\>\)

Enables printing background graphics.

```csharp
public static TPrintSettings EnablePrintingBackgrounds<TPrintSettings>(this IPrintBackgrounds<TPrintSettings> obj) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPrintBackgrounds](DotNetBrowser.Print.Settings.IPrintBackgrounds\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPrintBackgrounds%601" data-throw-if-not-resolved="false"></xref> implementation.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The background graphics printing is not supported by the printer.

