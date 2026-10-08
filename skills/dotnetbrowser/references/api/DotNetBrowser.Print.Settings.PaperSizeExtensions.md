# <a id="DotNetBrowser_Print_Settings_PaperSizeExtensions"></a> Class PaperSizeExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IPaperSize%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class PaperSizeExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PaperSizeExtensions](DotNetBrowser.Print.Settings.PaperSizeExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_PaperSizeExtensions_SetPaperSize__1_DotNetBrowser_Print_Settings_IPaperSize___0__DotNetBrowser_Print_PaperSize_"></a> SetPaperSize<TPrintSettings\>\(IPaperSize<TPrintSettings\>, PaperSize\)

Sets the paper size for printing.

```csharp
public static TPrintSettings SetPaperSize<TPrintSettings>(this IPaperSize<TPrintSettings> obj, PaperSize paperSize) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPaperSize](DotNetBrowser.Print.Settings.IPaperSize\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPaperSize%601" data-throw-if-not-resolved="false"></xref> implementation.

`paperSize` [PaperSize](DotNetBrowser.Print.PaperSize.md)

The paper size used for printing.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified paper size is null.

