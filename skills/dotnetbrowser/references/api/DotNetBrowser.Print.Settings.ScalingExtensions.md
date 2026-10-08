# <a id="DotNetBrowser_Print_Settings_ScalingExtensions"></a> Class ScalingExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IScaling%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class ScalingExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ScalingExtensions](DotNetBrowser.Print.Settings.ScalingExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_ScalingExtensions_SetScaling__1_DotNetBrowser_Print_Settings_IScaling___0__DotNetBrowser_Print_Scaling_"></a> SetScaling<TPrintSettings\>\(IScaling<TPrintSettings\>, Scaling\)

Sets the scaling for printing.

```csharp
public static TPrintSettings SetScaling<TPrintSettings>(this IScaling<TPrintSettings> obj, Scaling scaling) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IScaling](DotNetBrowser.Print.Settings.IScaling\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IScaling%601" data-throw-if-not-resolved="false"></xref> implementation.

`scaling` [Scaling](DotNetBrowser.Print.Scaling.md)

The scaling used for printing.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The specified scaling is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified scaling is not supported by the printer.

