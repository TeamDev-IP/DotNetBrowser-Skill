# <a id="DotNetBrowser_Dom_IOptionElement"></a> Interface IOptionElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents the DOM HTML <code>&lt;option&gt;</code> element.

```csharp
public interface IOptionElement : IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[IElement](DotNetBrowser.Dom.IElement.md), 
[INode](DotNetBrowser.Dom.INode.md), 
[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_IOptionElement_Selected"></a> Selected

Gets or sets the state of the option element.

```csharp
bool Selected { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IOptionElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

