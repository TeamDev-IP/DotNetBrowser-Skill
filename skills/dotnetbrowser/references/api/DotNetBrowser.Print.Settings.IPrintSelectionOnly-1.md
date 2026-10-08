# <a id="DotNetBrowser_Print_Settings_IPrintSelectionOnly_1"></a> Interface IPrintSelectionOnly<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring printing only the selected content.

```csharp
public interface IPrintSelectionOnly<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[PrintSelectionOnlyExtensions.DisablePrintingSelectionOnly<TPrintSettings\>\(IPrintSelectionOnly<TPrintSettings\>\)](DotNetBrowser.Print.Settings.PrintSelectionOnlyExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSelectionOnlyExtensions\_DisablePrintingSelectionOnly\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintSelectionOnly\_\_\_0\_\_), 
[PrintSelectionOnlyExtensions.EnablePrintingSelectionOnly<TPrintSettings\>\(IPrintSelectionOnly<TPrintSettings\>\)](DotNetBrowser.Print.Settings.PrintSelectionOnlyExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSelectionOnlyExtensions\_EnablePrintingSelectionOnly\_\_1\_DotNetBrowser\_Print\_Settings\_IPrintSelectionOnly\_\_\_0\_\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
printing only the selected content.

## Properties

### <a id="DotNetBrowser_Print_Settings_IPrintSelectionOnly_1_PrintingSelectionOnlyEnabled"></a> PrintingSelectionOnlyEnabled

Enables or disables printing only the selected content.

```csharp
bool PrintingSelectionOnlyEnabled { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Only the selected content printing is not supported by the printer.

