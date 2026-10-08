# <a id="DotNetBrowser_Print_Settings_FitExtensions"></a> Class FitExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IFit%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class FitExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FitExtensions](DotNetBrowser.Print.Settings.FitExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_FitExtensions_SetFit__1_DotNetBrowser_Print_Settings_IFit___0__DotNetBrowser_Print_Fit_"></a> SetFit<TPrintSettings\>\(IFit<TPrintSettings\>, Fit\)

Sets the content fit for printing.

```csharp
public static TPrintSettings SetFit<TPrintSettings>(this IFit<TPrintSettings> obj, Fit fit) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IFit](DotNetBrowser.Print.Settings.IFit\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IFit%601" data-throw-if-not-resolved="false"></xref> implementation.

`fit` [Fit](DotNetBrowser.Print.Fit.md)

The content fit used for printing.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The specified fit is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified fit is not supported by the printer.

