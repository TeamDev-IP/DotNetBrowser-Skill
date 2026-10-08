# <a id="DotNetBrowser_Dom_INode"></a> Interface INode

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

```csharp
public interface INode : IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_INode_Children"></a> Children

Gets the collection of the child nodes. Modifying this collection will lead to the DOM tree modification.

```csharp
INodeCollection Children { get; }
```

#### Property Value

 [INodeCollection](DotNetBrowser.Dom.INodeCollection.md)

### <a id="DotNetBrowser_Dom_INode_Document"></a> Document

Gets the document instance containing this node.

```csharp
IDocument Document { get; }
```

#### Property Value

 [IDocument](DotNetBrowser.Dom.IDocument.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INode_Frame"></a> Frame

Gets the frame containing this node.

```csharp
IFrame Frame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

### <a id="DotNetBrowser_Dom_INode_NextSibling"></a> NextSibling

Gets the next sibling node in the document tree.

```csharp
INode NextSibling { get; }
```

#### Property Value

 [INode](DotNetBrowser.Dom.INode.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INode_NodeName"></a> NodeName

Gets the name of this node, depending on its <xref href="DotNetBrowser.Dom.NodeType" data-throw-if-not-resolved="false"></xref>.

```csharp
string NodeName { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INode_NodeValue"></a> NodeValue

Gets the value of this node, depending on its <xref href="DotNetBrowser.Dom.NodeType" data-throw-if-not-resolved="false"></xref>.

```csharp
string NodeValue { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INode_Parent"></a> Parent

Gets the parent node.

```csharp
INode Parent { get; }
```

#### Property Value

 [INode](DotNetBrowser.Dom.INode.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INode_PreviousSibling"></a> PreviousSibling

Gets the previous sibling node in the document tree.

```csharp
INode PreviousSibling { get; }
```

#### Property Value

 [INode](DotNetBrowser.Dom.INode.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INode_TextContent"></a> TextContent

Gets or sets the text content of the node and its descendants.

```csharp
string TextContent { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    Setting this property on a node removes all of its children and replaces them with a single text node with the
    given value.
</p>
<p>
    The property value depends on the type of the node, whhich can be checked via the <xref href="DotNetBrowser.Dom.INode.Type" data-throw-if-not-resolved="false"></xref>
    property.
</p>
<p>
    The property value is an empty string if the element is a document, a document type, or a notation.
</p>
<p>
    If the node is a CDATA section, a comment, a processing instruction, or a text node, this method returns
    the text inside this node (the <xref href="DotNetBrowser.Dom.INode.NodeValue" data-throw-if-not-resolved="false"></xref>).
</p>
<p>
    For other node types, this method returns the concatenation of the TextContent attribute value
    of every child node, excluding comments and processing instruction nodes. This is an empty string if the
    node has no children.
</p>
<p>
    Differences from InnerText:

<ul>
        <li>
            The TextContent property gets the content of all elements, including &lt;script&gt; and &lt;style
            > elements, and the mostly equivalent <code>InnerText</code> property does not.
        </li>
        <li>
            <code>InnerText</code> is also aware of style and will not return the text of hidden elements, whereas
            TextContent
            will.
        </li>
        <li>As <code>InnerText</code> is aware of CSS styling, it will trigger a reflow, whereas TextContent will not.</li>
    </ul>
</p>

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INode_Type"></a> Type

Gets the type of this node.

```csharp
NodeType Type { get; }
```

#### Property Value

 [NodeType](DotNetBrowser.Dom.NodeType.md)

### <a id="DotNetBrowser_Dom_INode_XPath"></a> XPath

Gets an XPath for the current Node.

```csharp
string XPath { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Dom_INode_Click"></a> Click\(\)

Simulates click on the current Node.

```csharp
void Click()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INode_CompareDocumentPosition_DotNetBrowser_Dom_INode_"></a> CompareDocumentPosition\(INode\)

Compares position of the current node against another node in a DOM tree.

```csharp
DocumentPosition CompareDocumentPosition(INode otherNode)
```

#### Parameters

`otherNode` [INode](DotNetBrowser.Dom.INode.md)

The node to be compared to the current node

#### Returns

 [DocumentPosition](DotNetBrowser.Dom.DocumentPosition.md)

The document position of the node specified by the <code class="paramref">otherNode</code> parameter
relates to the position of the current node.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INode_Evaluate_System_String_DotNetBrowser_Dom_XPath_XPathResultType_"></a> Evaluate\(string, XPathResultType\)

Evaluates an XPath expression.

```csharp
IXPathResult Evaluate(string expression, XPathResultType type = XPathResultType.Any)
```

#### Parameters

`expression` [string](https://learn.microsoft.com/dotnet/api/system.string)

a string representing the XPath to be evaluated. Cannot be null or empty string.

`type` [XPathResultType](DotNetBrowser.Dom.XPath.XPathResultType.md)

type of result XPathResult to return. See <xref href="DotNetBrowser.Dom.XPath.XPathResultType" data-throw-if-not-resolved="false"></xref>

#### Returns

 [IXPathResult](DotNetBrowser.Dom.XPath.IXPathResult.md)

The <xref href="DotNetBrowser.Dom.XPath.IXPathResult" data-throw-if-not-resolved="false"></xref> object of the type specified in the <code class="paramref">type</code> parameter. The return
value will
be always a valid <xref href="DotNetBrowser.Dom.XPath.IXPathResult" data-throw-if-not-resolved="false"></xref> object.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">expression</code> is null, empty, or contains blank characters only.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [XPathException](DotNetBrowser.Dom.XPath.XPathException.md)

The XPath evaluation error occurs.

