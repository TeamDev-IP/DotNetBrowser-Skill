# <a id="DotNetBrowser_Dom_INodeCollection"></a> Interface INodeCollection

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents a collection of the DOM nodes.

```csharp
public interface INodeCollection : IEnumerable<INode>, IEnumerable
```

#### Implements

[IEnumerable<INode\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1), 
[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.ienumerable)

## Methods

### <a id="DotNetBrowser_Dom_INodeCollection_Append_DotNetBrowser_Dom_INode_"></a> Append\(INode\)

Appends a node as the last item of the collection. The new node could be an existing node in the document,
or a new node. If the node is existing node, it will be moved to new location
in the document.

```csharp
bool Append(INode node)
```

#### Parameters

`node` [INode](DotNetBrowser.Dom.INode.md)

the node to append.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the node was successfully appended, <code>false</code> otherwise.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">node</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INodeCollection_AsReadOnly"></a> AsReadOnly\(\)

Returns the snapshot of the items in the collection as a read-only list.

```csharp
IReadOnlyList<INode> AsReadOnly()
```

#### Returns

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[INode](DotNetBrowser.Dom.INode.md)\>

the snapshot of the items in the collection as a read-only list.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INodeCollection_Insert_DotNetBrowser_Dom_INode_DotNetBrowser_Dom_INode_"></a> Insert\(INode, INode\)

Inserts a new <code class="paramref">node</code> before an existing <code class="paramref">beforeNode</code>.

```csharp
bool Insert(INode node, INode beforeNode)
```

#### Parameters

`node` [INode](DotNetBrowser.Dom.INode.md)

The node to insert.

`beforeNode` [INode](DotNetBrowser.Dom.INode.md)

The node before which the node will be inserted.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if node was successfully inserted, <code>false</code> otherwise.

#### Remarks

The <code class="paramref">node</code> could be an existing
node in the document, or you can create and insert a new node. If the node is an existing node,
it will be moved to new location in the document.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">node</code> or <code class="paramref">beforeNode</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INodeCollection_Remove_DotNetBrowser_Dom_INode_"></a> Remove\(INode\)

Removes a node from the collection.

```csharp
bool Remove(INode node)
```

#### Parameters

`node` [INode](DotNetBrowser.Dom.INode.md)

The node to remove.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the node was successfully removed from the collection.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">node</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_INodeCollection_Replace_DotNetBrowser_Dom_INode_DotNetBrowser_Dom_INode_"></a> Replace\(INode, INode\)

Replaces an existing child node with a new node. The new node could be an existing node in the document,
or you can create a new node. If the <code class="paramref">newNode</code> is an existing node, it will be moved to new
location in the document.

```csharp
bool Replace(INode newNode, INode oldNode)
```

#### Parameters

`newNode` [INode](DotNetBrowser.Dom.INode.md)

the new node for replacement.

`oldNode` [INode](DotNetBrowser.Dom.INode.md)

the existing node, which will be replaced by <code class="paramref">newNode</code>.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the <code class="paramref">oldNode</code> was successfully replaced with the <code class="paramref">newNode</code>.

#### Remarks

The old node could be used for inserting/appending it into the document later.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">newNode</code> or the <code class="paramref">oldNode</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

