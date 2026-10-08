# <a id="DotNetBrowser_Print_Settings_CollateExtensions"></a> Class CollateExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.ICollate%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class CollateExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CollateExtensions](DotNetBrowser.Print.Settings.CollateExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_CollateExtensions_DisableCollatePrinting__1_DotNetBrowser_Print_Settings_ICollate___0__"></a> DisableCollatePrinting<TPrintSettings\>\(ICollate<TPrintSettings\>\)

Disables collate printing.

```csharp
public static TPrintSettings DisableCollatePrinting<TPrintSettings>(this ICollate<TPrintSettings> collate) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`collate` [ICollate](DotNetBrowser.Print.Settings.ICollate\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.ICollate%601" data-throw-if-not-resolved="false"></xref> implementation.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Collate is not supported by the printer.

### <a id="DotNetBrowser_Print_Settings_CollateExtensions_EnableCollatePrinting__1_DotNetBrowser_Print_Settings_ICollate___0__"></a> EnableCollatePrinting<TPrintSettings\>\(ICollate<TPrintSettings\>\)

Enables collate printing.

```csharp
public static TPrintSettings EnableCollatePrinting<TPrintSettings>(this ICollate<TPrintSettings> obj) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [ICollate](DotNetBrowser.Print.Settings.ICollate\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.ICollate%601" data-throw-if-not-resolved="false"></xref> implementation.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Collate is not supported by the printer.

