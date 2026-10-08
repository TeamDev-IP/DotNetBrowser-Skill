# <a id="DotNetBrowser_Print_Capabilities"></a> Class Capabilities

Namespace: [DotNetBrowser.Print](DotNetBrowser.Print.md)  
Assembly: DotNetBrowser.dll  

The capabilities of a printer.

```csharp
public sealed class Capabilities
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Capabilities](DotNetBrowser.Print.Capabilities.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Print_Capabilities_CanCollate"></a> CanCollate

Indicates whether the printer supports collate printing.

```csharp
public bool CanCollate { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Print_Capabilities_ColorModels"></a> ColorModels

Gets the list of the <xref href="DotNetBrowser.Print.ColorModel" data-throw-if-not-resolved="false"></xref> values supported by the printer.

```csharp
public IReadOnlyList<ColorModel> ColorModels { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ColorModel](DotNetBrowser.Print.ColorModel.md)\>

### <a id="DotNetBrowser_Print_Capabilities_DuplexModes"></a> DuplexModes

Gets the collection of the <xref href="DotNetBrowser.Print.DuplexMode" data-throw-if-not-resolved="false"></xref> values supported by the printer.

```csharp
public IReadOnlyCollection<DuplexMode> DuplexModes { get; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[DuplexMode](DotNetBrowser.Print.DuplexMode.md)\>

### <a id="DotNetBrowser_Print_Capabilities_MaxCopies"></a> MaxCopies

Gets the maximum number of copies that the printer can make.

```csharp
public int MaxCopies { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="DotNetBrowser_Print_Capabilities_PaperSizes"></a> PaperSizes

Gets the collection of the <xref href="DotNetBrowser.Print.PaperSize" data-throw-if-not-resolved="false"></xref> values supported by the printer.

```csharp
public IReadOnlyCollection<PaperSize> PaperSizes { get; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[PaperSize](DotNetBrowser.Print.PaperSize.md)\>

