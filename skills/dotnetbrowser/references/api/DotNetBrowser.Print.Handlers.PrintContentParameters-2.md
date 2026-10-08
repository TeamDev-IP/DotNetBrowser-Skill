# <a id="DotNetBrowser_Print_Handlers_PrintContentParameters_2"></a> Class PrintContentParameters<TPrintSettings, TPdfPrintSettings\>

Namespace: [DotNetBrowser.Print.Handlers](DotNetBrowser.Print.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for content printing handlers parameters.

```csharp
public class PrintContentParameters<TPrintSettings, TPdfPrintSettings> where TPrintSettings : class, SystemPrinter.ISettings<TPrintSettings> where TPdfPrintSettings : class, PdfPrinter.ISettings<TPdfPrintSettings>
```

#### Type Parameters

`TPrintSettings` 

The system print settings type.

`TPdfPrintSettings` 

The PDF print settings type.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintContentParameters<TPrintSettings, TPdfPrintSettings\>](DotNetBrowser.Print.Handlers.PrintContentParameters\-2.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Print_Handlers_PrintContentParameters_2_Browser"></a> Browser

Gets the browser associated with the handler.

```csharp
public IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Print_Handlers_PrintContentParameters_2_Printers"></a> Printers

Gets the collection of printers available in this handler.

```csharp
public IPrinters<TPrintSettings, TPdfPrintSettings> Printers { get; }
```

#### Property Value

 [IPrinters](DotNetBrowser.Print.IPrinters\-2.md)<TPrintSettings, TPdfPrintSettings\>

