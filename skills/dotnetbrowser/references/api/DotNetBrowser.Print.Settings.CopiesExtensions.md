# <a id="DotNetBrowser_Print_Settings_CopiesExtensions"></a> Class CopiesExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.ICopies%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class CopiesExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CopiesExtensions](DotNetBrowser.Print.Settings.CopiesExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_CopiesExtensions_SetCopies__1_DotNetBrowser_Print_Settings_ICopies___0__System_Int32_"></a> SetCopies<TPrintSettings\>\(ICopies<TPrintSettings\>, int\)

Sets the number of copies to print.

```csharp
public static TPrintSettings SetCopies<TPrintSettings>(this ICopies<TPrintSettings> obj, int copies) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [ICopies](DotNetBrowser.Print.Settings.ICopies\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.ICopies%601" data-throw-if-not-resolved="false"></xref> implementation.

`copies` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The number of copies to print. Cannot be zero or negative.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified copies number is less than or equal to zero.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified copies number is not supported by the printer.

