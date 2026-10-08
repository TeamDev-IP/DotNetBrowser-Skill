# <a id="DotNetBrowser_Print_PdfPrinter_1"></a> Class PdfPrinter<TPrintSettings\>

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

A printer that allows you to print to PDF.

```csharp
public sealed class PdfPrinter<TPrintSettings> : Printer<TPrintSettings>, IAutoDisposable where TPrintSettings : class, PdfPrinter.ISettings<TPrintSettings>
```

#### Type Parameters

`TPrintSettings` 

The print settings type that can be applied to the print job.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Printer<TPrintSettings\>](DotNetBrowser.Print.Printer\-1.md) ← 
[PdfPrinter<TPrintSettings\>](DotNetBrowser.Print.PdfPrinter\-1.md)

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

