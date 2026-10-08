# <a id="DotNetBrowser_Dom_IDocument"></a> Interface IDocument

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents DOM HTML document of the web page.

```csharp
public interface IDocument : INode, IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[INode](DotNetBrowser.Dom.INode.md), 
[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_IDocument_BaseUri"></a> BaseUri

Gets the <code>&lt;base&gt;</code> element's href attribute if one
is present.

```csharp
string BaseUri { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Dom_IDocument_DocumentElement"></a> DocumentElement

Gets the document HTML element that usually represents HTML tag.

```csharp
IElement DocumentElement { get; }
```

#### Property Value

 [IElement](DotNetBrowser.Dom.IElement.md)

### <a id="DotNetBrowser_Dom_IDocument_FocusedElement"></a> FocusedElement

Gets the currently focused element in the document.

```csharp
IElement FocusedElement { get; }
```

#### Property Value

 [IElement](DotNetBrowser.Dom.IElement.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IDocument" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

## Methods

### <a id="DotNetBrowser_Dom_IDocument_CreateElement_System_String_"></a> CreateElement\(string\)

Creates and returns a new DOM element with the specified tag name.

```csharp
IElement CreateElement(string tagName)
```

#### Parameters

`tagName` [string](https://learn.microsoft.com/dotnet/api/system.string)

the tag name (e.g. "A", "P", "DIV") of the new DOM element.

#### Returns

 [IElement](DotNetBrowser.Dom.IElement.md)

the new <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> or null if the <code class="paramref">tagName</code> is incorrect.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">tagName</code> is null, empty, or contains only blank characters.

### <a id="DotNetBrowser_Dom_IDocument_CreateEvent_DotNetBrowser_Dom_Events_EventType_DotNetBrowser_Dom_Events_EventParameters_"></a> CreateEvent\(EventType, EventParameters\)

Creates a DOM event instance of the specified type.

```csharp
IEvent CreateEvent(EventType eventType, EventParameters parameters)
```

#### Parameters

`eventType` [EventType](DotNetBrowser.Dom.Events.EventType.md)

the DOM event type.

`parameters` [EventParameters](DotNetBrowser.Dom.Events.EventParameters.md)

the parameters of the DOM event

#### Returns

 [IEvent](DotNetBrowser.Dom.Events.IEvent.md)

DOM Event object

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

when eventType or parameters values are null.

### <a id="DotNetBrowser_Dom_IDocument_CreateKeyDownEvent_DotNetBrowser_Dom_Events_KeyEventParameters_"></a> CreateKeyDownEvent\(KeyEventParameters\)

    Creates and returns a new <code>keyDown</code> <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object with the given 

<pre><code class="lang-csharp">parameters</code></pre>

.

```csharp
IKeyEvent CreateKeyDownEvent(KeyEventParameters parameters)
```

#### Parameters

`parameters` [KeyEventParameters](DotNetBrowser.Dom.Events.KeyEventParameters.md)

a <xref href="DotNetBrowser.Dom.Events.KeyEventParameters" data-throw-if-not-resolved="false"></xref>object representing key event properties.
Cannot be null.

#### Returns

 [IKeyEvent](DotNetBrowser.Dom.Events.IKeyEvent.md)

the new <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when parameters value is null.

### <a id="DotNetBrowser_Dom_IDocument_CreateKeyPressEvent_DotNetBrowser_Dom_Events_KeyEventParameters_"></a> CreateKeyPressEvent\(KeyEventParameters\)

    Creates and returns a new <code>keyPress</code> <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object with the given 

<pre><code class="lang-csharp">parameters</code></pre>

.

```csharp
IKeyEvent CreateKeyPressEvent(KeyEventParameters parameters)
```

#### Parameters

`parameters` [KeyEventParameters](DotNetBrowser.Dom.Events.KeyEventParameters.md)

a <xref href="DotNetBrowser.Dom.Events.KeyEventParameters" data-throw-if-not-resolved="false"></xref>object representing key event properties.
Cannot be null.

#### Returns

 [IKeyEvent](DotNetBrowser.Dom.Events.IKeyEvent.md)

the new <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when parameters value is null.

### <a id="DotNetBrowser_Dom_IDocument_CreateKeyUpEvent_DotNetBrowser_Dom_Events_KeyEventParameters_"></a> CreateKeyUpEvent\(KeyEventParameters\)

    Creates and returns a new <code>keyUp</code> <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object with the given 

<pre><code class="lang-csharp">parameters</code></pre>

.

```csharp
IKeyEvent CreateKeyUpEvent(KeyEventParameters parameters)
```

#### Parameters

`parameters` [KeyEventParameters](DotNetBrowser.Dom.Events.KeyEventParameters.md)

a <xref href="DotNetBrowser.Dom.Events.KeyEventParameters" data-throw-if-not-resolved="false"></xref>object representing key event properties.
Cannot be null.

#### Returns

 [IKeyEvent](DotNetBrowser.Dom.Events.IKeyEvent.md)

the new <xref href="DotNetBrowser.Dom.Events.IKeyEvent" data-throw-if-not-resolved="false"></xref> object.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when parameters value is null.

### <a id="DotNetBrowser_Dom_IDocument_CreateMouseEvent_DotNetBrowser_Dom_Events_EventType_DotNetBrowser_Dom_Events_MouseEventParameters_"></a> CreateMouseEvent\(EventType, MouseEventParameters\)

    Creates and returns a new <xref href="DotNetBrowser.Dom.Events.IMouseEvent" data-throw-if-not-resolved="false"></xref> object with the given 

<pre><code class="lang-csharp">eventType</code></pre>

    and 

    <pre><code class="lang-csharp">parameters</code></pre>

    .

```csharp
IMouseEvent CreateMouseEvent(EventType eventType, MouseEventParameters parameters)
```

#### Parameters

`eventType` [EventType](DotNetBrowser.Dom.Events.EventType.md)

an <xref href="DotNetBrowser.Dom.Events.EventType" data-throw-if-not-resolved="false"></xref>object representing a type of a valid DOM event
supported by engine. Cannot be null.

`parameters` [MouseEventParameters](DotNetBrowser.Dom.Events.MouseEventParameters.md)

a <xref href="DotNetBrowser.Dom.Events.MouseEventParameters" data-throw-if-not-resolved="false"></xref> object representing mouse event properties
(e.g. bubbles, cancellable). Cannot be null.

#### Returns

 [IMouseEvent](DotNetBrowser.Dom.Events.IMouseEvent.md)

the new <xref href="DotNetBrowser.Dom.Events.IMouseEvent" data-throw-if-not-resolved="false"></xref> object.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

when eventType or parameters values are null.

### <a id="DotNetBrowser_Dom_IDocument_CreateTextNode_System_String_"></a> CreateTextNode\(string\)

Returns a new Text DOM node with <xref href="DotNetBrowser.Dom.NodeType.TextNode" data-throw-if-not-resolved="false"></xref> type.

```csharp
INode CreateTextNode(string text = null)
```

#### Parameters

`text` [string](https://learn.microsoft.com/dotnet/api/system.string)

the string, which will be used to initialize node value.

#### Returns

 [INode](DotNetBrowser.Dom.INode.md)

the new Text DOM node with <xref href="DotNetBrowser.Dom.NodeType.TextNode" data-throw-if-not-resolved="false"></xref> type.

