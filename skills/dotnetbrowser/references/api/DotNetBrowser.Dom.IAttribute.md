# <a id="DotNetBrowser_Dom_IAttribute"></a> Interface IAttribute

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

```csharp
public interface IAttribute : INode, IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[INode](DotNetBrowser.Dom.INode.md), 
[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_IAttribute_Owner"></a> Owner

Gets an owner element of the attribute.

```csharp
IElement Owner { get; }
```

#### Property Value

 [IElement](DotNetBrowser.Dom.IElement.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IAttribute" data-throw-if-not-resolved="false"></xref> has already been disposed.

