# <a id="DotNetBrowser_Dom_XPath"></a> Namespace DotNetBrowser.Dom.XPath

### Classes

 [XPathException](DotNetBrowser.Dom.XPath.md#DotNetBrowser_Dom_XPath_XPathException)

This exception is thrown if XPath evaluation error occurs.

### Interfaces

 [IXPathResult](DotNetBrowser.Dom.XPath.md#DotNetBrowser_Dom_XPath_IXPathResult)

Represents the result of the XPath expression evaluation.

### Enums

 [XPathResultType](DotNetBrowser.Dom.XPath.md#DotNetBrowser_Dom_XPath_XPathResultType)

Represents the XPath result types.

## <a id="DotNetBrowser_Dom_XPath_XPathException"></a> Class XPathException

Namespace: [DotNetBrowser.Dom.XPath](DotNetBrowser.Dom.XPath.md)  
Assembly: DotNetBrowser.dll  

This exception is thrown if XPath evaluation error occurs.

```csharp
public sealed class XPathException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[XPathException](DotNetBrowser.Dom.XPath.md#DotNetBrowser_Dom_XPath_XPathException)

##### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

##### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Dom_XPath_XPathException__ctor_System_String_"></a> XPathException\(string\)

Initializes a new instance of the <xref href="DotNetBrowser.Dom.XPath.XPathException" data-throw-if-not-resolved="false"></xref> class with a specified error message.

```csharp
public XPathException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

The error message.

## <a id="DotNetBrowser_Dom_XPath_IXPathResult"></a> Interface IXPathResult

Namespace: [DotNetBrowser.Dom.XPath](DotNetBrowser.Dom.XPath.md)  
Assembly: DotNetBrowser.dll  

Represents the result of the XPath expression evaluation.

```csharp
public interface IXPathResult
```

### Properties

#### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Bool"></a> Bool

Gets the boolean value of the evaluation result.

```csharp
bool? Bool { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)?

#### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Iterator"></a> Iterator

Gets the iterator which allows requesting the
items from the Chromium engine during the iterating.

```csharp
IEnumerable<INode> Iterator { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)\>

#### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Node"></a> Node

Gets the DOM node returned as the result of evaluation.

```csharp
INode Node { get; }
```

##### Property Value

 [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

#### <a id="DotNetBrowser_Dom_XPath_IXPathResult_NodesSnapshot"></a> NodesSnapshot

Gets the snapshot collection of the DOM nodes.
If evaluation result type is not ordered or
unordered node iterator then returns null.

```csharp
IEnumerable<INode> NodesSnapshot { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)\>

#### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Numeric"></a> Numeric

Gets the numeric value of the evaluation result.

```csharp
double? Numeric { get; }
```

##### Property Value

 [double](https://learn.microsoft.com/dotnet/api/system.double)?

#### <a id="DotNetBrowser_Dom_XPath_IXPathResult_String"></a> String

Gets the string value of the evaluation result.

```csharp
string String { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Dom_XPath_IXPathResult_Type"></a> Type

Gets the result type.

```csharp
XPathResultType Type { get; }
```

##### Property Value

 [XPathResultType](DotNetBrowser.Dom.XPath.md#DotNetBrowser_Dom_XPath_XPathResultType)

## <a id="DotNetBrowser_Dom_XPath_XPathResultType"></a> Enum XPathResultType

Namespace: [DotNetBrowser.Dom.XPath](DotNetBrowser.Dom.XPath.md)  
Assembly: DotNetBrowser.dll  

Represents the XPath result types.

```csharp
public enum XPathResultType
```

### Fields

`Any = 1` 

The result type is not set. In this case the type is a natural type of the evaluation result.



`AnyUnorderedNode = 9` 

The result represents a single node matching the XPath expression.
The node is not necessarily the first node in the document that matches the expression.



`Boolean = 4` 

The result contains a single boolean value.



`FirstOrderedNode = 10` 

The result represents the first node in the document matching the XPath expression.



`Number = 2` 

The result contains a single number.



`OrderedNodeIterator = 6` 

The result represents a set of all nodes matching the XPath expression.
The nodes in the result are in the same order that they appear in the document.



`OrderedNodeSnapshot = 8` 

The result represents the snapshots of all nodes matching the XPath expression.
The nodes in the result are in the same order that they appear in the document.



`String = 3` 

The result contains a single string.



`UnorderedNodeIterator = 5` 

The result represents a set of all nodes matching the XPath expression.
The order of nodes in the result is not defined.



`UnorderedNodeSnapshot = 7` 

The result represents the snapshots of all nodes matching the XPath expression.
The order of the nodes in the result is not defined.
