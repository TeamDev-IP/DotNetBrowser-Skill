# <a id="DotNetBrowser_Print_Settings_PageRangesExtensions"></a> Class PageRangesExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IPageRanges%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class PageRangesExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PageRangesExtensions](DotNetBrowser.Print.Settings.PageRangesExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_PageRangesExtensions_SetPageRanges__1_DotNetBrowser_Print_Settings_IPageRanges___0__System_Collections_Generic_IReadOnlyCollection_DotNetBrowser_Print_PageRange__"></a> SetPageRanges<TPrintSettings\>\(IPageRanges<TPrintSettings\>, IReadOnlyCollection<PageRange\>\)

Sets the collection of the page ranges to print.

```csharp
public static TPrintSettings SetPageRanges<TPrintSettings>(this IPageRanges<TPrintSettings> obj, IReadOnlyCollection<PageRange> pageRanges) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IPageRanges](DotNetBrowser.Print.Settings.IPageRanges\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IPageRanges%601" data-throw-if-not-resolved="false"></xref> implementation.

`pageRanges` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[PageRange](DotNetBrowser.Print.PageRange.md)\>

The collection of the page ranges to print.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The collection is null, empty, or contains null objects.

