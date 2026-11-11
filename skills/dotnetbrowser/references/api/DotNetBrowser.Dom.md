# <a id="DotNetBrowser_Dom"></a> Namespace DotNetBrowser.Dom

### Namespaces

 [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)

 [DotNetBrowser.Dom.XPath](DotNetBrowser.Dom.XPath.md)

### Classes

 [DomException](DotNetBrowser.Dom.md#DotNetBrowser_Dom_DomException)

Thrown when an operation on the DOM element fails.

 [PointInspection](DotNetBrowser.Dom.md#DotNetBrowser_Dom_PointInspection)

Provides information about a DOM node at the specified point inside the loaded document.

### Interfaces

 [IAttribute](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IAttribute)

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

 [IAttributes](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IAttributes)

A dictionary that contains <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> attributes. Modifying this dictionary
will lead to modifying the element attributes.

 [IDocument](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IDocument)

Represents DOM HTML document of the web page.

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

 [IFormControlElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IFormControlElement)

Represents the form control element.

 [IFormElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IFormElement)

Represents DOM HTML Form element.

 [IFrameElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IFrameElement)

Represents an HTML <code>&lt;frame&gt;</code> or <code>&lt;iframe&gt;</code> element.

 [IImageElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IImageElement)

Represents DOM HTML image element <code>&lt;img&gt;</code>.

 [IInputElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IInputElement)

Represents the DOM element with <code>&lt;input&gt;</code> tag.

 [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

 [INodeCollection](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INodeCollection)

Represents a collection of the DOM nodes.

 [IOptionElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IOptionElement)

Represents the DOM HTML <code>&lt;option&gt;</code> element.

 [ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext)

The base interface for search that is implemented by the DOM objects that provide
search mechanisms.

 [ISelectElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISelectElement)

Represents DOM HTML <code>&lt;select&gt;</code> element.

 [ITextAreaElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ITextAreaElement)

Represents DOM HTML <code>&lt;textarea&gt;</code> element.

### Enums

 [AlignTo](DotNetBrowser.Dom.md#DotNetBrowser_Dom_AlignTo)

Represents the values that can be used to describe how the element
will be aligned to the visible area of the scrollable ancestor.

 [DocumentPosition](DotNetBrowser.Dom.md#DotNetBrowser_Dom_DocumentPosition)

Enumeration of the document position that represent the relationship
between two nodes within the Document.

 [NodeType](DotNetBrowser.Dom.md#DotNetBrowser_Dom_NodeType)

Represents the node types that can be used to distinguish different kind of nodes
(such as an HTML element, text, attribute) from each other.

## <a id="DotNetBrowser_Dom_DomException"></a> Class DomException

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Thrown when an operation on the DOM element fails.

```csharp
public sealed class DomException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[DomException](DotNetBrowser.Dom.md#DotNetBrowser_Dom_DomException)

##### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

##### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Dom_DomException__ctor_System_String_"></a> DomException\(string\)

Initializes a new <xref href="DotNetBrowser.Dom.DomException" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public DomException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

The message that describes the error.

## <a id="DotNetBrowser_Dom_PointInspection"></a> Class PointInspection

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Provides information about a DOM node at the specified point inside the loaded document.

```csharp
public sealed class PointInspection
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PointInspection](DotNetBrowser.Dom.md#DotNetBrowser_Dom_PointInspection)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Dom_PointInspection_AbsoluteImageUrl"></a> AbsoluteImageUrl

Gets the absolute URL of the image located at the point.

```csharp
public string AbsoluteImageUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Dom_PointInspection_AbsoluteLinkUrl"></a> AbsoluteLinkUrl

Gets the absolute URL of the link DOM element at the specified point.
Returns an empty string if there is no link at the point.

```csharp
public string AbsoluteLinkUrl { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Dom_PointInspection_LocalPoint"></a> LocalPoint

Gets the coordinates of the point relative to the node.

```csharp
public Point LocalPoint { get; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

#### <a id="DotNetBrowser_Dom_PointInspection_Node"></a> Node

Gets the node at the specified point.

```csharp
public INode Node { get; }
```

##### Property Value

 [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

#### <a id="DotNetBrowser_Dom_PointInspection_UrlNode"></a> UrlNode

Gets the link node when a link is located at the point.

```csharp
public INode UrlNode { get; }
```

##### Property Value

 [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

## <a id="DotNetBrowser_Dom_IAttribute"></a> Interface IAttribute

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

```csharp
public interface IAttribute : INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_IAttribute_Owner"></a> Owner

Gets an owner element of the attribute.

```csharp
IElement Owner { get; }
```

##### Property Value

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IAttribute" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_IAttributes"></a> Interface IAttributes

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

A dictionary that contains <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> attributes. Modifying this dictionary
will lead to modifying the element attributes.

```csharp
public interface IAttributes : IAutoDisposable, IDictionary<string, string>, ICollection<KeyValuePair<string, string>>, IEnumerable<KeyValuePair<string, string>>, IEnumerable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable), 
[IDictionary<string, string\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.idictionary\-2), 
[ICollection<KeyValuePair<string, string\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.icollection\-1), 
[IEnumerable<KeyValuePair<string, string\>\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1), 
[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.ienumerable)

### Methods

#### <a id="DotNetBrowser_Dom_IAttributes_AsReadOnly"></a> AsReadOnly\(\)

Gets a read-only dictionary that contains a snapshot of the attributes of the current element.

```csharp
IReadOnlyDictionary<string, string> AsReadOnly()
```

##### Returns

 [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<[string](https://learn.microsoft.com/dotnet/api/system.string), [string](https://learn.microsoft.com/dotnet/api/system.string)\>

The dictionary that contains a snapshot of the attributes of the current element.
The returned dictionary will be empty if the element doesn't have any attributes.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IAttributes" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_IDocument"></a> Interface IDocument

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents DOM HTML document of the web page.

```csharp
public interface IDocument : INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_IDocument_BaseUri"></a> BaseUri

Gets the <code>&lt;base&gt;</code> element's href attribute if one
is present.

```csharp
string BaseUri { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Dom_IDocument_DocumentElement"></a> DocumentElement

Gets the document HTML element that usually represents HTML tag.

```csharp
IElement DocumentElement { get; }
```

##### Property Value

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

#### <a id="DotNetBrowser_Dom_IDocument_FocusedElement"></a> FocusedElement

Gets the currently focused element in the document.

```csharp
IElement FocusedElement { get; }
```

##### Property Value

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IDocument" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

### Methods

#### <a id="DotNetBrowser_Dom_IDocument_CreateElement_System_String_"></a> CreateElement\(string\)

Creates and returns a new DOM element with the specified tag name.

```csharp
IElement CreateElement(string tagName)
```

##### Parameters

`tagName` [string](https://learn.microsoft.com/dotnet/api/system.string)

the tag name (e.g. "A", "P", "DIV") of the new DOM element.

##### Returns

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

the new <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> or null if the <code class="paramref">tagName</code> is incorrect.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">tagName</code> is null, empty, or contains only blank characters.

#### <a id="DotNetBrowser_Dom_IDocument_CreateEvent_DotNetBrowser_Dom_Events_EventType_DotNetBrowser_Dom_Events_EventParameters_"></a> CreateEvent\(EventType, EventParameters\)

Creates a DOM event instance of the specified type.

```csharp
IEvent CreateEvent(EventType eventType, EventParameters parameters)
```

##### Parameters

`eventType` [EventType](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_EventType)

the DOM event type.

`parameters` [EventParameters](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_EventParameters)

the parameters of the DOM event

##### Returns

 [IEvent](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEvent)

DOM Event object

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

when eventType or parameters values are null.

#### <a id="DotNetBrowser_Dom_IDocument_CreateKeyDownEvent_DotNetBrowser_Dom_Events_KeyEventParameters_"></a> CreateKeyDownEvent\(KeyEventParameters\)

    Creates and returns a new <code>keyDown</code> <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object with the given 

<pre><code class="lang-csharp">parameters</code></pre>

.

```csharp
IKeyEvent CreateKeyDownEvent(KeyEventParameters parameters)
```

##### Parameters

`parameters` [KeyEventParameters](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_KeyEventParameters)

a <xref href="DotNetBrowser.Dom.Events.KeyEventParameters" data-throw-if-not-resolved="false"></xref>object representing key event properties.
Cannot be null.

##### Returns

 [IKeyEvent](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IKeyEvent)

the new <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when parameters value is null.

#### <a id="DotNetBrowser_Dom_IDocument_CreateKeyPressEvent_DotNetBrowser_Dom_Events_KeyEventParameters_"></a> CreateKeyPressEvent\(KeyEventParameters\)

    Creates and returns a new <code>keyPress</code> <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object with the given 

<pre><code class="lang-csharp">parameters</code></pre>

.

```csharp
IKeyEvent CreateKeyPressEvent(KeyEventParameters parameters)
```

##### Parameters

`parameters` [KeyEventParameters](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_KeyEventParameters)

a <xref href="DotNetBrowser.Dom.Events.KeyEventParameters" data-throw-if-not-resolved="false"></xref>object representing key event properties.
Cannot be null.

##### Returns

 [IKeyEvent](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IKeyEvent)

the new <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when parameters value is null.

#### <a id="DotNetBrowser_Dom_IDocument_CreateKeyUpEvent_DotNetBrowser_Dom_Events_KeyEventParameters_"></a> CreateKeyUpEvent\(KeyEventParameters\)

    Creates and returns a new <code>keyUp</code> <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object with the given 

<pre><code class="lang-csharp">parameters</code></pre>

.

```csharp
IKeyEvent CreateKeyUpEvent(KeyEventParameters parameters)
```

##### Parameters

`parameters` [KeyEventParameters](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_KeyEventParameters)

a <xref href="DotNetBrowser.Dom.Events.KeyEventParameters" data-throw-if-not-resolved="false"></xref>object representing key event properties.
Cannot be null.

##### Returns

 [IKeyEvent](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IKeyEvent)

the new <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when parameters value is null.

#### <a id="DotNetBrowser_Dom_IDocument_CreateMouseEvent_DotNetBrowser_Dom_Events_EventType_DotNetBrowser_Dom_Events_MouseEventParameters_"></a> CreateMouseEvent\(EventType, MouseEventParameters\)

    Creates and returns a new <xref href="DotNetBrowser.Dom.Events.IMouseEvent" data-throw-if-not-resolved="false"></xref> object with the given 

<pre><code class="lang-csharp">eventType</code></pre>

    and 

    <pre><code class="lang-csharp">parameters</code></pre>

    .

```csharp
IMouseEvent CreateMouseEvent(EventType eventType, MouseEventParameters parameters)
```

##### Parameters

`eventType` [EventType](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_EventType)

an <xref href="DotNetBrowser.Dom.Events.EventType" data-throw-if-not-resolved="false"></xref>object representing a type of a valid DOM event
supported by engine. Cannot be null.

`parameters` [MouseEventParameters](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_MouseEventParameters)

a <xref href="DotNetBrowser.Dom.Events.MouseEventParameters" data-throw-if-not-resolved="false"></xref> object representing mouse event properties
(e.g. bubbles, cancellable). Cannot be null.

##### Returns

 [IMouseEvent](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IMouseEvent)

the new <xref href="DotNetBrowser.Dom.Events.IMouseEvent" data-throw-if-not-resolved="false"></xref> object.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when eventType or parameters values are null.

#### <a id="DotNetBrowser_Dom_IDocument_CreateTextNode_System_String_"></a> CreateTextNode\(string\)

Returns a new Text DOM node with <xref href="DotNetBrowser.Dom.NodeType.TextNode" data-throw-if-not-resolved="false"></xref> type.

```csharp
INode CreateTextNode(string text = null)
```

##### Parameters

`text` [string](https://learn.microsoft.com/dotnet/api/system.string)

the string, which will be used to initialize node value.

##### Returns

 [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

the new Text DOM node with <xref href="DotNetBrowser.Dom.NodeType.TextNode" data-throw-if-not-resolved="false"></xref> type.

## <a id="DotNetBrowser_Dom_IElement"></a> Interface IElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

```csharp
public interface IElement : INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_IElement_AttributeNodes"></a> AttributeNodes

Gets a list that contains attribute nodes of the element. Each list entry
represents an attribute node.

```csharp
IReadOnlyList<IAttribute> AttributeNodes { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[IAttribute](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IAttribute)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IElement_Attributes"></a> Attributes

Gets a dictionary that contains attributes of the current element. Modifying this dictionary
will lead to modifying the element attributes.

```csharp
IAttributes Attributes { get; }
```

##### Property Value

 [IAttributes](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IAttributes)

#### <a id="DotNetBrowser_Dom_IElement_BoundingClientRect"></a> BoundingClientRect

Gets the bounds of the element and its position relative to the top-left of
the viewport of the current document.

```csharp
Rectangle BoundingClientRect { get; }
```

##### Property Value

 [Rectangle](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Rectangle)

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IElement_BoundingClientRectInViewport"></a> BoundingClientRectInViewport

Gets the bounds of the element and its position relative to the top-left of the viewport of the main document.

```csharp
Rectangle BoundingClientRectInViewport { get; }
```

##### Property Value

 [Rectangle](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Rectangle)

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IElement_InnerHtml"></a> InnerHtml

Gets or sets the inner HTML of the current element.

```csharp
string InnerHtml { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [DomException](DotNetBrowser.Dom.md#DotNetBrowser_Dom_DomException)

The value was not set.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IElement_InnerText"></a> InnerText

Gets or sets the inner text of the current element.

```csharp
string InnerText { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [DomException](DotNetBrowser.Dom.md#DotNetBrowser_Dom_DomException)

The value was not set.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IElement_OuterHtml"></a> OuterHtml

Gets or sets the outer HTML of the current element.

```csharp
string OuterHtml { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

<p>
    While the element will be replaced in the document, the variable whose <code>OuterHtml</code> property
    was set will still hold a reference to the original element.
    See <a href="https://developer.mozilla.org/en-US/docs/Web/API/Element/outerHTML">https://developer.mozilla.org/en-US/docs/Web/API/Element/outerHTML</a>
    MDN web docs.
</p>

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The value is set to null.

 [DomException](DotNetBrowser.Dom.md#DotNetBrowser_Dom_DomException)

The value was not set.

### Methods

#### <a id="DotNetBrowser_Dom_IElement_Blur"></a> Blur\(\)

Removes focus from the current element.

```csharp
void Blur()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IElement_Focus"></a> Focus\(\)

Gives focus to the current element (if it can be focused).

```csharp
void Focus()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IElement_ScrollIntoView_DotNetBrowser_Dom_AlignTo_"></a> ScrollIntoView\(AlignTo\)

Scrolls the element's parent container such that the element on which this method is called
is visible to the user.

```csharp
void ScrollIntoView(AlignTo alignTo)
```

##### Parameters

`alignTo` [AlignTo](DotNetBrowser.Dom.md#DotNetBrowser_Dom_AlignTo)

Describes how the element will be aligned to the visible area of the
scrollable ancestor

##### Remarks

<p>
    Note that the element may not be scrolled completely to the top or bottom depending on
    the layout of other elements.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_IFormControlElement"></a> Interface IFormControlElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents the form control element.

```csharp
public interface IFormControlElement : IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement), 
[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_IFormControlElement_Form"></a> Form

Gets the <code>&lt;form&gt;</code> element containing this control.

```csharp
IFormElement Form { get; }
```

##### Property Value

 [IFormElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IFormElement)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormControlElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IFormControlElement_IsEnabled"></a> IsEnabled

Indicates whether form control is enabled or disabled.

```csharp
bool IsEnabled { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormControlElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IFormControlElement_Value"></a> Value

Gets or sets the form control value.

```csharp
string Value { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormControlElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null.

## <a id="DotNetBrowser_Dom_IFormElement"></a> Interface IFormElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents DOM HTML Form element.

```csharp
public interface IFormElement : IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement), 
[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_IFormElement_Action"></a> Action

Gets the 'action' attribute value.

```csharp
string Action { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IFormElement_Controls"></a> Controls

Gets the collection of all control elements in the form.

```csharp
IEnumerable<IFormControlElement> Controls { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IFormControlElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IFormControlElement)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IFormElement_Method"></a> Method

Gets the 'method' attribute value.

```csharp
string Method { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IFormElement_Name"></a> Name

Gets the 'name' attribute value.

```csharp
string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Dom_IFormElement_Reset"></a> Reset\(\)

Restores the form elements' default values. It performs the same action as a reset button.

```csharp
void Reset()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IFormElement_Submit"></a> Submit\(\)

Submits the form. It performs the same action as a submit button.

```csharp
void Submit()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_IFrameElement"></a> Interface IFrameElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents an HTML <code>&lt;frame&gt;</code> or <code>&lt;iframe&gt;</code> element.

```csharp
public interface IFrameElement : IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement), 
[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_IFrameElement_ContentDocument"></a> ContentDocument

Gets the document of the current <code>&lt;frame&gt;</code> or <code>&lt;iframe&gt;</code> element.

```csharp
IDocument ContentDocument { get; }
```

##### Property Value

 [IDocument](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IDocument)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFrameElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_IImageElement"></a> Interface IImageElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents DOM HTML image element <code>&lt;img&gt;</code>.

```csharp
public interface IImageElement : IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement), 
[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_IImageElement_Contents"></a> Contents

Gets the image displayed by the element.

```csharp
Bitmap Contents { get; }
```

##### Property Value

 [Bitmap](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Bitmap)

##### Remarks

The size of the bitmap depends on the size of the original image. It is not affected by the size specified for
the element.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IImageElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_IInputElement"></a> Interface IInputElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents the DOM element with <code>&lt;input&gt;</code> tag.

```csharp
public interface IInputElement : IFormControlElement, IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[IFormControlElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IFormControlElement), 
[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement), 
[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_IInputElement_Checked"></a> Checked

Gets or sets the checked attribute of the input DOM element with the type
<code>'checkbox'</code> or <code>'radio'</code>.

```csharp
bool Checked { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IInputElement_File"></a> File

Gets or sets an absolute or relative path to a file if the current input DOM element
has the type attribute with the 'file' value.

```csharp
string File { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty, or contains only blank characters.

#### <a id="DotNetBrowser_Dom_IInputElement_Files"></a> Files

Gets or sets the collection of absolute or relative paths to files if the current input DOM element
has the type attribute with the 'file' value.

```csharp
IEnumerable<string> Files { get; set; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty, or contains only blank characters.

#### <a id="DotNetBrowser_Dom_IInputElement_IsCheckBox"></a> IsCheckBox

Indicates whether the DOM element's type attribute has the 'checkbox' value.

```csharp
bool IsCheckBox { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IInputElement_IsEmailField"></a> IsEmailField

Indicates whether the DOM element's type attribute has the 'email' value.

```csharp
bool IsEmailField { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IInputElement_IsFile"></a> IsFile

Indicates whether the DOM element's type attribute has the 'file' value.

```csharp
bool IsFile { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IInputElement_IsMultipleFile"></a> IsMultipleFile

Indicates whether the DOM element has both the type attribute with the
'file' value, and the  multiple attribute, for example: <code>&lt;input type="file" multiple&gt;</code>

```csharp
bool IsMultipleFile { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IInputElement_IsPasswordField"></a> IsPasswordField

Indicates whether the DOM element's type attribute has the 'password' value.

```csharp
bool IsPasswordField { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IInputElement_IsRadioButton"></a> IsRadioButton

Indicates whether the DOM element's type attribute has the 'radio' value.

```csharp
bool IsRadioButton { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IInputElement_IsText"></a> IsText

Indicates if this input element is a text field and
the type attribute value of the input HTML element is 'number'.

```csharp
bool IsText { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_IInputElement_IsTextField"></a> IsTextField

Indicates if the DOM element's type attribute has the <code>'text'</code> value.

```csharp
bool IsTextField { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_INode"></a> Interface INode

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

This interface is implemented by all <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> implementations
to support DOM event model.

```csharp
public interface INode : IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_INode_Children"></a> Children

Gets the collection of the child nodes. Modifying this collection will lead to the DOM tree modification.

```csharp
INodeCollection Children { get; }
```

##### Property Value

 [INodeCollection](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INodeCollection)

#### <a id="DotNetBrowser_Dom_INode_Document"></a> Document

Gets the document instance containing this node.

```csharp
IDocument Document { get; }
```

##### Property Value

 [IDocument](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IDocument)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INode_Frame"></a> Frame

Gets the frame containing this node.

```csharp
IFrame Frame { get; }
```

##### Property Value

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

#### <a id="DotNetBrowser_Dom_INode_NextSibling"></a> NextSibling

Gets the next sibling node in the document tree.

```csharp
INode NextSibling { get; }
```

##### Property Value

 [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INode_NodeName"></a> NodeName

Gets the name of this node, depending on its <xref href="DotNetBrowser.Dom.NodeType" data-throw-if-not-resolved="false"></xref>.

```csharp
string NodeName { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INode_NodeValue"></a> NodeValue

Gets the value of this node, depending on its <xref href="DotNetBrowser.Dom.NodeType" data-throw-if-not-resolved="false"></xref>.

```csharp
string NodeValue { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INode_Parent"></a> Parent

Gets the parent node.

```csharp
INode Parent { get; }
```

##### Property Value

 [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INode_PreviousSibling"></a> PreviousSibling

Gets the previous sibling node in the document tree.

```csharp
INode PreviousSibling { get; }
```

##### Property Value

 [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INode_TextContent"></a> TextContent

Gets or sets the text content of the node and its descendants.

```csharp
string TextContent { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

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

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INode_Type"></a> Type

Gets the type of this node.

```csharp
NodeType Type { get; }
```

##### Property Value

 [NodeType](DotNetBrowser.Dom.md#DotNetBrowser_Dom_NodeType)

#### <a id="DotNetBrowser_Dom_INode_XPath"></a> XPath

Gets an XPath for the current Node.

```csharp
string XPath { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### Methods

#### <a id="DotNetBrowser_Dom_INode_Click"></a> Click\(\)

Simulates click on the current Node.

```csharp
void Click()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INode_CompareDocumentPosition_DotNetBrowser_Dom_INode_"></a> CompareDocumentPosition\(INode\)

Compares position of the current node against another node in a DOM tree.

```csharp
DocumentPosition CompareDocumentPosition(INode otherNode)
```

##### Parameters

`otherNode` [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

The node to be compared to the current node

##### Returns

 [DocumentPosition](DotNetBrowser.Dom.md#DotNetBrowser_Dom_DocumentPosition)

The document position of the node specified by the <code class="paramref">otherNode</code> parameter
relates to the position of the current node.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INode_Evaluate_System_String_DotNetBrowser_Dom_XPath_XPathResultType_"></a> Evaluate\(string, XPathResultType\)

Evaluates an XPath expression.

```csharp
IXPathResult Evaluate(string expression, XPathResultType type = XPathResultType.Any)
```

##### Parameters

`expression` [string](https://learn.microsoft.com/dotnet/api/system.string)

a string representing the XPath to be evaluated. Cannot be null or empty string.

`type` [XPathResultType](DotNetBrowser.Dom.XPath.md#DotNetBrowser_Dom_XPath_XPathResultType)

type of result XPathResult to return. See <xref href="DotNetBrowser.Dom.XPath.XPathResultType" data-throw-if-not-resolved="false"></xref>

##### Returns

 [IXPathResult](DotNetBrowser.Dom.XPath.md#DotNetBrowser_Dom_XPath_IXPathResult)

The <xref href="DotNetBrowser.Dom.XPath.IXPathResult" data-throw-if-not-resolved="false"></xref> object of the type specified in the <code class="paramref">type</code> parameter. The return
value will
be always a valid <xref href="DotNetBrowser.Dom.XPath.IXPathResult" data-throw-if-not-resolved="false"></xref> object.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">expression</code> is null, empty, or contains blank characters only.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [XPathException](DotNetBrowser.Dom.XPath.md#DotNetBrowser_Dom_XPath_XPathException)

The XPath evaluation error occurs.

## <a id="DotNetBrowser_Dom_INodeCollection"></a> Interface INodeCollection

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents a collection of the DOM nodes.

```csharp
public interface INodeCollection : IEnumerable<INode>, IEnumerable
```

##### Implements

[IEnumerable<INode\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1), 
[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.ienumerable)

### Methods

#### <a id="DotNetBrowser_Dom_INodeCollection_Append_DotNetBrowser_Dom_INode_"></a> Append\(INode\)

Appends a node as the last item of the collection. The new node could be an existing node in the document,
or a new node. If the node is existing node, it will be moved to new location
in the document.

```csharp
bool Append(INode node)
```

##### Parameters

`node` [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

the node to append.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the node was successfully appended, <code>false</code> otherwise.

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">node</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INodeCollection_AsReadOnly"></a> AsReadOnly\(\)

Returns the snapshot of the items in the collection as a read-only list.

```csharp
IReadOnlyList<INode> AsReadOnly()
```

##### Returns

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)\>

the snapshot of the items in the collection as a read-only list.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INodeCollection_Insert_DotNetBrowser_Dom_INode_DotNetBrowser_Dom_INode_"></a> Insert\(INode, INode\)

Inserts a new <code class="paramref">node</code> before an existing <code class="paramref">beforeNode</code>.

```csharp
bool Insert(INode node, INode beforeNode)
```

##### Parameters

`node` [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

The node to insert.

`beforeNode` [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

The node before which the node will be inserted.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if node was successfully inserted, <code>false</code> otherwise.

##### Remarks

The <code class="paramref">node</code> could be an existing
node in the document, or you can create and insert a new node. If the node is an existing node,
it will be moved to new location in the document.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">node</code> or <code class="paramref">beforeNode</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INodeCollection_Remove_DotNetBrowser_Dom_INode_"></a> Remove\(INode\)

Removes a node from the collection.

```csharp
bool Remove(INode node)
```

##### Parameters

`node` [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

The node to remove.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the node was successfully removed from the collection.

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">node</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_INodeCollection_Replace_DotNetBrowser_Dom_INode_DotNetBrowser_Dom_INode_"></a> Replace\(INode, INode\)

Replaces an existing child node with a new node. The new node could be an existing node in the document,
or you can create a new node. If the <code class="paramref">newNode</code> is an existing node, it will be moved to new
location in the document.

```csharp
bool Replace(INode newNode, INode oldNode)
```

##### Parameters

`newNode` [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

the new node for replacement.

`oldNode` [INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode)

the existing node, which will be replaced by <code class="paramref">newNode</code>.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the <code class="paramref">oldNode</code> was successfully replaced with the <code class="paramref">newNode</code>.

##### Remarks

The old node could be used for inserting/appending it into the document later.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">newNode</code> or the <code class="paramref">oldNode</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.INode" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_IOptionElement"></a> Interface IOptionElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents the DOM HTML <code>&lt;option&gt;</code> element.

```csharp
public interface IOptionElement : IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement), 
[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_IOptionElement_Selected"></a> Selected

Gets or sets the state of the option element.

```csharp
bool Selected { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IOptionElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_ISearchContext"></a> Interface ISearchContext

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

The base interface for search that is implemented by the DOM objects that provide
search mechanisms.

```csharp
public interface ISearchContext : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Methods

#### <a id="DotNetBrowser_Dom_ISearchContext_GetElementByClassName_System_String_"></a> GetElementByClassName\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given
<code class="paramref">className</code>.

```csharp
IElement GetElementByClassName(string className)
```

##### Parameters

`className` [string](https://learn.microsoft.com/dotnet/api/system.string)

The class attribute of the HTML element.

##### Returns

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

The first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given <code class="paramref">className</code> or <code>null</code> if no elements were found.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">className</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_ISearchContext_GetElementByCssSelector_System_String_"></a> GetElementByCssSelector\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given CSS selector.

```csharp
IElement GetElementByCssSelector(string cssSelector)
```

##### Parameters

`cssSelector` [string](https://learn.microsoft.com/dotnet/api/system.string)

The CSS selector.

##### Returns

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

The first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given CSS selector or <code>null</code> if no elements were found.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">cssSelector</code> is null, empty or contains only blank
characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_ISearchContext_GetElementById_System_String_"></a> GetElementById\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given <code class="paramref">id</code>.

```csharp
IElement GetElementById(string id)
```

##### Parameters

`id` [string](https://learn.microsoft.com/dotnet/api/system.string)

a string that represents the id attribute of the HTML element.

##### Returns

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

The first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given <code class="paramref">id</code> or <code>null</code> if no elements were found.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">id</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_ISearchContext_GetElementByName_System_String_"></a> GetElementByName\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given <code class="paramref">name</code>.

```csharp
IElement GetElementByName(string name)
```

##### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The <code>name</code> attribute of the HTML element.

##### Returns

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

The first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given <code class="paramref">name</code> or  <code>null</code> if no elements were found.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">name</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_ISearchContext_GetElementByTagName_System_String_"></a> GetElementByTagName\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given tag name.

```csharp
IElement GetElementByTagName(string tagName)
```

##### Parameters

`tagName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The tag name of the HTML element.

##### Returns

 [IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)

the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given tag name or <code>null</code> if no elements were found.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">tagName</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_ISearchContext_GetElementsByClassName_System_String_"></a> GetElementsByClassName\(string\)

Finds all <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects in the current search context by the given <code class="paramref">className</code>.

```csharp
IEnumerable<IElement> GetElementsByClassName(string className)
```

##### Parameters

`className` [string](https://learn.microsoft.com/dotnet/api/system.string)

The <code>class</code> attribute of the HTML element.

##### Returns

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)\>

A collection of the <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects found in the current search context
by the given <code class="paramref">className</code> or an empty collection if no elements were found.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">className</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_ISearchContext_GetElementsByCssSelector_System_String_"></a> GetElementsByCssSelector\(string\)

Finds all <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects in the current search context by the given
<code class="paramref">cssSelector</code>.

```csharp
IEnumerable<IElement> GetElementsByCssSelector(string cssSelector)
```

##### Parameters

`cssSelector` [string](https://learn.microsoft.com/dotnet/api/system.string)

The CSS selector.

##### Returns

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)\>

A collection of the <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects found in the current search context
by the given <code class="paramref">cssSelector</code> or an empty collection if no elements were found.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">cssSelector</code> is null, empty or contains only blank
characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_ISearchContext_GetElementsByName_System_String_"></a> GetElementsByName\(string\)

Finds all <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects in the current search context by the given <code>name</code>.

```csharp
IEnumerable<IElement> GetElementsByName(string name)
```

##### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The <code>name</code> attribute of the HTML element.

##### Returns

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)\>

a collection of the <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects found in the current search context
by the given <code>name</code> or an empty collection if no elements were found.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">name</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_ISearchContext_GetElementsByTagName_System_String_"></a> GetElementsByTagName\(string\)

Finds all <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects in the current search context by the given tag name.

```csharp
IEnumerable<IElement> GetElementsByTagName(string tagName)
```

##### Parameters

`tagName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The tag name of the HTML element.

##### Returns

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement)\>

The collection of the <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects found in the current search context
by the given tag name or an empty collection if no elements were found.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">tagName</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_ISelectElement"></a> Interface ISelectElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents DOM HTML <code>&lt;select&gt;</code> element.

```csharp
public interface ISelectElement : IFormControlElement, IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[IFormControlElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IFormControlElement), 
[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement), 
[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Dom_ISelectElement_Multiple"></a> Multiple

Enables or disables selecting multiple options in the list.

```csharp
bool Multiple { get; set; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISelectElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Dom_ISelectElement_Options"></a> Options

Gets the collection of <code>&lt;option&gt;</code> elements contained by this <code>&lt;select&gt;</code> element.

```csharp
IEnumerable<IOptionElement> Options { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IOptionElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IOptionElement)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISelectElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Dom_ITextAreaElement"></a> Interface ITextAreaElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents DOM HTML <code>&lt;textarea&gt;</code> element.

```csharp
public interface ITextAreaElement : IFormControlElement, IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

##### Implements

[IFormControlElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IFormControlElement), 
[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement), 
[INode](DotNetBrowser.Dom.md#DotNetBrowser_Dom_INode), 
[IEventTarget](DotNetBrowser.Dom.Events.md#DotNetBrowser_Dom_Events_IEventTarget), 
[ISearchContext](DotNetBrowser.Dom.md#DotNetBrowser_Dom_ISearchContext), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

## <a id="DotNetBrowser_Dom_AlignTo"></a> Enum AlignTo

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents the values that can be used to describe how the element
will be aligned to the visible area of the scrollable ancestor.

```csharp
public enum AlignTo
```

### Fields

`Bottom = 1` 

The bottom of the element will be aligned to the bottom of the visible area of the scrollable ancestor.



`Top = 0` 

The top of the element will be aligned to the top of the visible area of the scrollable ancestor.



### See Also

[IElement](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement).[ScrollIntoView](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IElement_ScrollIntoView_DotNetBrowser_Dom_AlignTo_)\([AlignTo](DotNetBrowser.Dom.md#DotNetBrowser_Dom_AlignTo)\)

## <a id="DotNetBrowser_Dom_DocumentPosition"></a> Enum DocumentPosition

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Enumeration of the document position that represent the relationship
between two nodes within the Document.

```csharp
[Flags]
public enum DocumentPosition
```

### Fields

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

## <a id="DotNetBrowser_Dom_NodeType"></a> Enum NodeType

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents the node types that can be used to distinguish different kind of nodes
(such as an HTML element, text, attribute) from each other.

```csharp
public enum NodeType
```

### Fields

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
