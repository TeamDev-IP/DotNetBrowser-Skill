# <a id="DotNetBrowser_Dom_NodeType"></a> Enum NodeType

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents the node types that can be used to distinguish different kind of nodes
(such as an HTML element, text, attribute) from each other.

```csharp
public enum NodeType
```

## Fields

`AttributeNode = 2` 

An attribute of the HTML element.



`CDataSectionNode = 4` 

A <code>[CDATA]</code> section.



`CommentNode = 6` 

A content between the <code>&lt;!--</code> and <code>--&gt;</code> statements.



`DocumentFragmentNode = 9` 

A segment of the document structure.



`DocumentNode = 7` 

A document node.



`DocumentTypeNode = 8` 

A document type node. For example, <code>&lt;!DOCTYPE html&gt;</code> for HTML5 documents.



`ElementNode = 1` 

An element node, such as `<p>` or `<div>`.



`ProcessingInstructionsNode = 5` 

A <code>ProcessingInstruction</code> of an XML document such as <code>&lt;?xml-stylesheet ... ?&gt;</code>
declaration.



`TextNode = 3` 

The actual text of the HTML element or the attribute.



