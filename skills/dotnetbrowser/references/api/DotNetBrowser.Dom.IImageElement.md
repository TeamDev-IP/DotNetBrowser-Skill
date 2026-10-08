# <a id="DotNetBrowser_Dom_IImageElement"></a> Interface IImageElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents DOM HTML image element <code>&lt;img&gt;</code>.

```csharp
public interface IImageElement : IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[IElement](DotNetBrowser.Dom.IElement.md), 
[INode](DotNetBrowser.Dom.INode.md), 
[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_IImageElement_Contents"></a> Contents

Gets the image displayed by the element.

```csharp
Bitmap Contents { get; }
```

#### Property Value

 [Bitmap](DotNetBrowser.Ui.Bitmap.md)

#### Remarks

The size of the bitmap depends on the size of the original image. It is not affected by the size specified for
the element.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IImageElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

