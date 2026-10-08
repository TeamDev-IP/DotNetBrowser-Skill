# <a id="DotNetBrowser_Dom_DocumentPosition"></a> Enum DocumentPosition

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Enumeration of the document position that represent the relationship
between two nodes within the Document.

```csharp
[Flags]
public enum DocumentPosition
```

## Fields

`ContainedBy = 16` 

The other node contains the reference node.



`Contains = 8` 

The reference node contains the other node.



`Disconnected = 1` 

The nodes are disconnected.



`Following = 4` 

The position of the other node follows the position of the reference node.



`ImplementationSpecific = 32` 

The node positions depend on the DOM implementation and cannot be compared.



`Preceding = 2` 

The position of the other node precedes the position of the reference node.



