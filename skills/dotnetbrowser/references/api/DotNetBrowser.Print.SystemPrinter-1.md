# <a id="DotNetBrowser_Print_SystemPrinter_1"></a> Class SystemPrinter<TPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

A local or network printer available in the system.

```csharp
public sealed class SystemPrinter<TPrintSettings> : Printer<TPrintSettings>, IAutoDisposable where TPrintSettings : class, SystemPrinter.ISettings<TPrintSettings>
```

#### Type Parameters

`TPrintSettings` 

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Printer<TPrintSettings\>](DotNetBrowser.Print.Printer\-1.md) ← 
[SystemPrinter<TPrintSettings\>](DotNetBrowser.Print.SystemPrinter\-1.md)

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Inherited Members

[Printer<TPrintSettings\>.Capabilities](DotNetBrowser.Print.Printer\-1.md\#DotNetBrowser\_Print\_Printer\_1\_Capabilities), 
[Printer<TPrintSettings\>.DeviceName](DotNetBrowser.Print.Printer\-1.md\#DotNetBrowser\_Print\_Printer\_1\_DeviceName), 
[Printer<TPrintSettings\>.IsDefault](DotNetBrowser.Print.Printer\-1.md\#DotNetBrowser\_Print\_Printer\_1\_IsDefault), 
[Printer<TPrintSettings\>.PrintJob](DotNetBrowser.Print.Printer\-1.md\#DotNetBrowser\_Print\_Printer\_1\_PrintJob), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

