# <a id="DotNetBrowser_Print_Settings_PrintHeaderFooterExtensions"></a> Class PrintHeaderFooterExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IPrintHeaderFooter%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class PrintHeaderFooterExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintHeaderFooterExtensions](DotNetBrowser.Print.Settings.PrintHeaderFooterExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_PrintHeaderFooterExtensions_DisablePrintingHeaderFooter__1_DotNetBrowser_Print_Settings_IPrintHeaderFooter___0__"></a> DisablePrintingHeaderFooter<TPrintSettings\>\(IPrintHeaderFooter<TPrintSettings\>\)

Disables printing headers and footers.

```csharp
public static TPrintSettings DisablePrintingHeaderFooter<TPrintSettings>(this IPrintHeaderFooter<TPrintSettings> obj) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPrintHeaderFooter](DotNetBrowser.Print.Settings.IPrintHeaderFooter\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPrintHeaderFooter%601" data-throw-if-not-resolved="false"></xref> implementation.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The headers and footer printing is not supported by the printer.

### <a id="DotNetBrowser_Print_Settings_PrintHeaderFooterExtensions_EnablePrintingHeaderFooter__1_DotNetBrowser_Print_Settings_IPrintHeaderFooter___0__"></a> EnablePrintingHeaderFooter<TPrintSettings\>\(IPrintHeaderFooter<TPrintSettings\>\)

Enables printing headers and footers.

```csharp
public static TPrintSettings EnablePrintingHeaderFooter<TPrintSettings>(this IPrintHeaderFooter<TPrintSettings> obj) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPrintHeaderFooter](DotNetBrowser.Print.Settings.IPrintHeaderFooter\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPrintHeaderFooter%601" data-throw-if-not-resolved="false"></xref> implementation.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The headers and footer printing is not supported by the printer.

