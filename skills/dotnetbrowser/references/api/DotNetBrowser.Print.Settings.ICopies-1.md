# <a id="DotNetBrowser_Print_Settings_ICopies_1"></a> Interface ICopies<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the number of copies to print.

```csharp
public interface ICopies<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[CopiesExtensions.SetCopies<TPrintSettings\>\(ICopies<TPrintSettings\>, int\)](DotNetBrowser.Print.Settings.CopiesExtensions.md\#DotNetBrowser\_Print\_Settings\_CopiesExtensions\_SetCopies\_\_1\_DotNetBrowser\_Print\_Settings\_ICopies\_\_\_0\_\_System\_Int32\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support specifying
copies.

## Properties

### <a id="DotNetBrowser_Print_Settings_ICopies_1_Copies"></a> Copies

Gets or sets the number of copies to print.

```csharp
int Copies { get; set; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified copies number is less than or equal to zero.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The specified copies number is not supported by the printer.

