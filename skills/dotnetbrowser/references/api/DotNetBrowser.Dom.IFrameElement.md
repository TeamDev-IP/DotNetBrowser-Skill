# <a id="DotNetBrowser_Dom_IFrameElement"></a> Interface IFrameElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents an HTML <code>&lt;frame&gt;</code> or <code>&lt;iframe&gt;</code> element.

```csharp
public interface IFrameElement : IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[IElement](DotNetBrowser.Dom.IElement.md), 
[INode](DotNetBrowser.Dom.INode.md), 
[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_IFrameElement_ContentDocument"></a> ContentDocument

Gets the document of the current <code>&lt;frame&gt;</code> or <code>&lt;iframe&gt;</code> element.

```csharp
IDocument ContentDocument { get; }
```

#### Property Value

 [IDocument](DotNetBrowser.Dom.IDocument.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFrameElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

