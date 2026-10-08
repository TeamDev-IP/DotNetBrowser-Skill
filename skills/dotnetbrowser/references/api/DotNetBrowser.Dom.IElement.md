# <a id="DotNetBrowser_Dom_IElement"></a> Interface IElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

```csharp
public interface IElement : INode, IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[INode](DotNetBrowser.Dom.INode.md), 
[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_IElement_AttributeNodes"></a> AttributeNodes

Gets a list that contains attribute nodes of the element. Each list entry
represents an attribute node.

```csharp
IReadOnlyList<IAttribute> AttributeNodes { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[IAttribute](DotNetBrowser.Dom.IAttribute.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IElement_Attributes"></a> Attributes

Gets a dictionary that contains attributes of the current element. Modifying this dictionary
will lead to modifying the element attributes.

```csharp
IAttributes Attributes { get; }
```

#### Property Value

 [IAttributes](DotNetBrowser.Dom.IAttributes.md)

### <a id="DotNetBrowser_Dom_IElement_BoundingClientRect"></a> BoundingClientRect

Gets the bounds of the element and its position relative to the top-left of
the viewport of the current document.

```csharp
Rectangle BoundingClientRect { get; }
```

#### Property Value

 [Rectangle](DotNetBrowser.Geometry.Rectangle.md)

#### Remarks

<p>
    The amount of scrolling that has been done of the viewport area (or any other
    scrollable element) is taken into account when computing the bounding rectangle.
    This means that the rectangle's boundary edges (top, left, bottom, and right)
    change their values every time the scrolling position changes (because their
    values are relative to the viewport and not absolute). If you need the bounding
    rectangle relative to the top-left corner of the document, just add the current
    scrolling position to the top and left properties (these can be obtained using
    <code>window.scrollX</code> and <code>window.scrollY</code>) to get a bounding rectangle
    which is independent from the current scrolling position.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IElement_BoundingClientRectInViewport"></a> BoundingClientRectInViewport

Gets the bounds of the element and its position relative to the top-left of the viewport of the main document.

```csharp
Rectangle BoundingClientRectInViewport { get; }
```

#### Property Value

 [Rectangle](DotNetBrowser.Geometry.Rectangle.md)

#### Remarks

<p>This property can return an empty <xref href="DotNetBrowser.Geometry.Rectangle" data-throw-if-not-resolved="false"></xref> in the following cases:</p>
<ul><li>The element is not attached to the DOM tree.</li><li>The element is not visible and has the <code>hidden</code> attribute.</li><li>The CSS style of the element contains <code>display: none;</code> statement.</li></ul>
<p>
    If the element is attached to the DOM tree and is visible, but it is out of the viewport,
    this property still returns its bounds.
</p>
<p>
    To get the bounding rectangle of the element relative to the viewport of the current
    document, use the <xref href="DotNetBrowser.Dom.IElement.BoundingClientRect" data-throw-if-not-resolved="false"></xref> property.
</p>
<p>The origin and size of the returned rectangle are in the device-independent pixels.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IElement_InnerHtml"></a> InnerHtml

Gets or sets the inner HTML of the current element.

```csharp
string InnerHtml { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [DomException](DotNetBrowser.Dom.DomException.md)

The value was not set.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IElement_InnerText"></a> InnerText

Gets or sets the inner text of the current element.

```csharp
string InnerText { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [DomException](DotNetBrowser.Dom.DomException.md)

The value was not set.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IElement_OuterHtml"></a> OuterHtml

Gets or sets the outer HTML of the current element.

```csharp
string OuterHtml { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
    While the element will be replaced in the document, the variable whose <code>OuterHtml</code> property
    was set will still hold a reference to the original element.
    See <a href="https://developer.mozilla.org/en-US/docs/Web/API/Element/outerHTML">https://developer.mozilla.org/en-US/docs/Web/API/Element/outerHTML</a>
    MDN web docs.
</p>

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The value is set to null.

 [DomException](DotNetBrowser.Dom.DomException.md)

The value was not set.

## Methods

### <a id="DotNetBrowser_Dom_IElement_Blur"></a> Blur\(\)

Removes focus from the current element.

```csharp
void Blur()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IElement_Focus"></a> Focus\(\)

Gives focus to the current element (if it can be focused).

```csharp
void Focus()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IElement_ScrollIntoView_DotNetBrowser_Dom_AlignTo_"></a> ScrollIntoView\(AlignTo\)

Scrolls the element's parent container such that the element on which this method is called
is visible to the user.

```csharp
void ScrollIntoView(AlignTo alignTo)
```

#### Parameters

`alignTo` [AlignTo](DotNetBrowser.Dom.AlignTo.md)

Describes how the element will be aligned to the visible area of the
scrollable ancestor

#### Remarks

<p>
    Note that the element may not be scrolled completely to the top or bottom depending on
    the layout of other elements.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

