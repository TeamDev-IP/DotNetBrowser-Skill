# <a id="DotNetBrowser_Dom_XPath_IXPathResult"></a> Interface IXPathResult

Namespace: [DotNetBrowser.Dom.XPath](DotNetBrowser.Dom.XPath.md)  
Assembly: DotNetBrowser.dll  

Represents the result of the XPath expression evaluation.

```csharp
public interface IXPathResult
```

## Properties

### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Bool"></a> Bool

Gets the boolean value of the evaluation result.

```csharp
bool? Bool { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)?

### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Iterator"></a> Iterator

Gets the iterator which allows requesting the
items from the Chromium engine during the iterating.

```csharp
IEnumerable<INode> Iterator { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[INode](DotNetBrowser.Dom.INode.md)\>

### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Node"></a> Node

Gets the DOM node returned as the result of evaluation.

```csharp
INode Node { get; }
```

#### Property Value

 [INode](DotNetBrowser.Dom.INode.md)

### <a id="DotNetBrowser_Dom_XPath_IXPathResult_NodesSnapshot"></a> NodesSnapshot

Gets the snapshot collection of the DOM nodes.
If evaluation result type is not ordered or
unordered node iterator then returns null.

```csharp
IEnumerable<INode> NodesSnapshot { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[INode](DotNetBrowser.Dom.INode.md)\>

### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Numeric"></a> Numeric

Gets the numeric value of the evaluation result.

```csharp
double? Numeric { get; }
```

#### Property Value

 [double](https://learn.microsoft.com/dotnet/api/system.double)?

### <a id="DotNetBrowser_Dom_XPath_IXPathResult_String"></a> String

Gets the string value of the evaluation result.

```csharp
string String { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Type"></a> Type

Gets the result type.

```csharp
XPathResultType Type { get; }
```

#### Property Value

 [XPathResultType](DotNetBrowser.Dom.XPath.XPathResultType.md)

