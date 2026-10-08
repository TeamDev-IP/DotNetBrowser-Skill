# <a id="DotNetBrowser_Print_Settings_IPageRanges_1"></a> Interface IPageRanges<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the page ranges for printing.

```csharp
public interface IPageRanges<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[PageRangesExtensions.SetPageRanges<TPrintSettings\>\(IPageRanges<TPrintSettings\>, IReadOnlyCollection<PageRange\>\)](DotNetBrowser.Print.Settings.PageRangesExtensions.md\#DotNetBrowser\_Print\_Settings\_PageRangesExtensions\_SetPageRanges\_\_1\_DotNetBrowser\_Print\_Settings\_IPageRanges\_\_\_0\_\_System\_Collections\_Generic\_IReadOnlyCollection\_DotNetBrowser\_Print\_PageRange\_\_)

## Remarks

This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support specifying
page ranges.

## Properties

### <a id="DotNetBrowser_Print_Settings_IPageRanges_1_PageRanges"></a> PageRanges

Gets or sets the collection of the page ranges to print.

```csharp
IReadOnlyCollection<PageRange> PageRanges { get; set; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[PageRange](DotNetBrowser.Print.PageRange.md)\>

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The collection is null, empty, or contains null objects.

