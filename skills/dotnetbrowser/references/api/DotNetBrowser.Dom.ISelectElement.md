# <a id="DotNetBrowser_Dom_ISelectElement"></a> Interface ISelectElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents DOM HTML <code>&lt;select&gt;</code> element.

```csharp
public interface ISelectElement : IFormControlElement, IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[IFormControlElement](DotNetBrowser.Dom.IFormControlElement.md), 
[IElement](DotNetBrowser.Dom.IElement.md), 
[INode](DotNetBrowser.Dom.INode.md), 
[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_ISelectElement_Multiple"></a> Multiple

Enables or disables selecting multiple options in the list.

```csharp
bool Multiple { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISelectElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_ISelectElement_Options"></a> Options

Gets the collection of <code>&lt;option&gt;</code> elements contained by this <code>&lt;select&gt;</code> element.

```csharp
IEnumerable<IOptionElement> Options { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IOptionElement](DotNetBrowser.Dom.IOptionElement.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISelectElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

