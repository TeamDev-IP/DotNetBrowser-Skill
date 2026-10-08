# <a id="DotNetBrowser_Print_Settings_OrientationExtensions"></a> Class OrientationExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IOrientation%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class OrientationExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[OrientationExtensions](DotNetBrowser.Print.Settings.OrientationExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_OrientationExtensions_SetOrientation__1_DotNetBrowser_Print_Settings_IOrientation___0__DotNetBrowser_Print_Orientation_"></a> SetOrientation<TPrintSettings\>\(IOrientation<TPrintSettings\>, Orientation\)

Sets the page orientation.

```csharp
public static TPrintSettings SetOrientation<TPrintSettings>(this IOrientation<TPrintSettings> obj, Orientation orientation) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IOrientation](DotNetBrowser.Print.Settings.IOrientation\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IOrientation%601" data-throw-if-not-resolved="false"></xref> implementation.

`orientation` [Orientation](DotNetBrowser.Print.Orientation.md)

The page orientation.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified page orientation is not supported by the printer.

