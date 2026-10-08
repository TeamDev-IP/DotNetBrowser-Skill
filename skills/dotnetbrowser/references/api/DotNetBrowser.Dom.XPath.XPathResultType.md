# <a id="DotNetBrowser_Dom_XPath_XPathResultType"></a> Enum XPathResultType

Namespace: [DotNetBrowser.Dom.XPath](DotNetBrowser.Dom.XPath.md)  
Assembly: DotNetBrowser.dll  

Represents the XPath result types.

```csharp
public enum XPathResultType
```

## Fields

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



