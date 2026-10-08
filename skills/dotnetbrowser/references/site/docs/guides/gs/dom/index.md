
# DOM

**Lead**
This guide describes how to access a DOM document, find elements, modify a DOM structure, simulate user input, and so on.


## Overview

Each web page loaded in a `IBrowser` has a main `IFrame`. The `IFrame` itself may have child frames. For example, when a web page has multiple `IFRAME` objects, use the `IFrame` class to access DOM and JavaScript.

## Accessing a document

Every `IFrame` has a DOM `IDocument`. To access the `IDocument`, use the `IFrame.Document` property:


**C#**
```csharp
IDocument document = frame.Document;
```

**VB**
```vb
Dim document As IDocument = frame.Document
```



## Finding elements

You can find HTML elements inside an element by different conditions. The code sample below demonstrates how to find all `DIV` elements inside the document element:


**C#**
```csharp
IElement documentElement = document.DocumentElement;
IEnumerable<IElement> elements = documentElement?.GetElementsByTagName("div"); 
```

**VB**
```vb
Dim documentElement As IElement = document.DocumentElement
Dim elements As IEnumerable(Of IElement) = documentElement?.GetElementsByTagName("div")
```



If you need to find only the first HTML element, use the following approach:


**C#**
```csharp
documentElement.GetElementByTagName("div");
```

**VB**
```vb
documentElement.GetElementByTagName("div")
```



Here are the examples of searching for HTML elements by different conditions:


**C#**
```csharp
documentElement.GetElementById("<id>");
documentElement.GetElementsByName("<attr-name>");
documentElement.GetElementsByTagName("<tag-name>");
documentElement.GetElementsByClassName("<attr-class>");
```

**VB**
```vb
documentElement.GetElementById("<id>")
documentElement.GetElementsByName("<attr-name>")
documentElement.GetElementsByTagName("<tag-name>")
documentElement.GetElementsByClassName("<attr-class>")
```



### XPath

DotNetBrowser DOM API allows evaluating XPath expressions using `INode.Evaluate(string expression)`. You can evaluate an XPath expression in the scope of a specified `INode` using the following code sample:


**C#**
```csharp
IXPathResult result = node.Evaluate("count(//div)");
```

**VB**
```vb
Dim result As IXPathResult = node.Evaluate("count(//div)")
```



The evaluation result is stored in the `IXPathResult` object. Make sure that the result contains the expected value type, for example, `Number`, `Boolean`, `String`, `Node`, and extract the value itself:


**C#**
```csharp
if (result.Type == XPathResultType.Number) {
    double? number = result.Numeric;
}
```

**VB**
```vb
If result.Type = XPathResultType.Number Then
    Dim number? As Double = result.Numeric
End If
```



### Query selector

To find the elements that match a specified selector, for example, `#root`, use the following code:


**C#**
```csharp
IEnumerable<IElement> elements = element.GetElementsByCssSelector("#root");
```

**VB**
```vb
Dim elements As IEnumerable(Of IElement) = element.GetElementsByCssSelector("#root")
```



### Focused element
To find the currently focused element on the web page, use the `IDocument.FocusedElement` property:


**C#**
```csharp
IElement focusedElement = document.FocusedElement;
```

**VB**
```vb
Dim focusedElement As IElement = document.FocusedElement
```



### Node at point

To find the `INode` at a specific point, for example, 100x150, on the web page, use the following approach:


**C#**
```csharp
PointInspection inspection = frame.Inspect(new Point(100, 150));
INode node = inspection.Node;
```

**VB**
```vb
Dim inspection As PointInspection = frame.Inspect(New Point(100, 150))
Dim node As INode = inspection.Node
```



## Working with elements
### Element bounds

You can get bounds of the `IElement` with the position relative to the top-left of the viewport of the current `IDocument` as follows:


**C#**
```csharp
Rectangle rect = element.BoundingClientRect;
```

**VB**
```vb
Dim rect As Rectangle = element.BoundingClientRect
```



**Note**
This method returns an empty `Rectangle` when the element has a `hidden` attribute or the CSS style of the element contains `display: none;` statement.


### Element attributes

The `IElement` class provides methods that allow you to get, add, remove, or modify the HTML element attributes. The code sample below demonstrates how to get all the attributes of the element and print their names and values:


**C#**
```csharp
foreach (KeyValuePair<string, string> attr in element.Attributes)
{
    Console.WriteLine($"{attr.Key}: {attr.Value}");
}
```

**VB**
```vb
For Each attr As KeyValuePair(Of String, String) In element.Attributes
    Console.WriteLine($"{attr.Key}: {attr.Value}")
Next
```



The code sample below demonstrates how to add/modify an element attribute:


**C#**
```csharp
element.Attributes["attrName"] = "attrValue";
```

**VB**
```vb
element.Attributes("attrName") = "attrValue"
```



### Creating Elements

The DOM API allows modifying the document DOM structure. The following example demonstrates how to create and insert `<p>` element with some text:


**C#**
```csharp
// Create a new paragraph element.
IElement paragraph = document.CreateElement("p");
// Create a text node with the given text.
INode text = document.CreateTextNode("Text");
// Insert the text node into the paragraph element.
if (paragraph.Children.Append(text)) {
    // Insert the paragraph element into the required element.
    bool success = element.Children.Append(paragraph);
}
```

**VB**
```vb
' Create a new paragraph element.
Dim paragraph As IElement = document.CreateElement("p")
' Create a text node with the given text.
Dim text As INode = document.CreateTextNode("Text")
' Insert the text node into the paragraph element.
If paragraph.Children.Append(text) Then
    ' Insert the paragraph element into the required element.
    Dim success As Boolean = element.Children.Append(paragraph)
End If
```



## DOM events

Each `INode` implements the `IEventTarget` interface that provides methods for registering DOM events. You can register DOM listener to receive DOM events such as `click`, `mousedown`, `mouseup`, `keydown`, `load`, `error`, and others.

The following code sample demonstrates how to register a `click` event listener for an HTML document element:


**C#**
```csharp
document.DocumentElement.Events.Click += (sender, e) => {
    // Mouse click event has been received.
};
```

**VB**
```vb
AddHandler document.DocumentElement.Events.Click, Sub(sender, e)
    ' Mouse click event has been received.
End Sub
```



DotNetBrowser also allows you to listen to the custom DOM event types. The following code sample demonstrates how to listen to `MyEvent` DOM Events:


**C#**
```csharp
// Create a custom DOM event type.
EventType eventType = new EventType("MyEvent");
element.Events[eventType] += (sender, e) => {
    // Custom event has been received.
};
```

**VB**
```vb
' Create a custom DOM event type.
Dim eventType As New EventType("MyEvent")
AddHandler element.Events(eventType).EventReceived, Sub(sender, e)
    ' Custom event has been received.
End Sub
```



## Automation

DotNetBrowser DOM API provides everything you need to automate the web form filling. This section describes how to update the text in the text fields, select a checkbox or a radio button, select one or multiple options in a drop-down list, simulate a click, and so on.

To work with web form controls, use the `IFormControlElement` interface. This interface allows you to check whether the control is enabled and to modify its value. All the form controls such as `INPUT`, `SELECT`, `TEXTAREA`, and others inherit this interface.

### Input

To work with `INPUT` elements, use the `IInputElement` interface. It provides all the required methods to check the input type and set its value.

#### Text, email, and password

To replace the default value of a text, email, or password field with a new value, use the `IInputElement.Value` property.

For example, your web form contains the `<input>` elements with the following types:

```html
<input type="text" id="firstname" placeholder="First Name">
<input type="email" id="email" placeholder="Email Address">
<input type="password" id="password" placeholder="Password">
```

You can set their value using the following approach:


**C#**
```csharp
((IInputElement)documentElement.GetElementById("firstname")).Value = "John";
((IInputElement)documentElement.GetElementById("email")).Value = "me@company.com";
((IInputElement)documentElement.GetElementById("password")).Value = "Jkdl12!";
```

**VB**
```vb
DirectCast(documentElement.GetElementById("firstname"), IInputElement).Value = "John"
DirectCast(documentElement.GetElementById("email"), IInputElement).Value = "me@company.com"
DirectCast(documentElement.GetElementById("password"), IInputElement).Value = "Jkdl12!"
```



#### Check box, radio button

To select a radio button or a check box, use the `IInputElement.Checked` property. For example, your web form contains the `<input>` elements with the following types:

```html
<input type="checkbox" id="checkbox" value="Remember me">
<input type="radio" id="radio" checked>
```

You can select/unselect them using the following approach:


**C#**
```csharp
((IInputElement)documentElement.GetElementById("checkbox")).Checked = true;

((IInputElement)documentElement.GetElementById("radio")).Checked = false;
```

**VB**
```vb
DirectCast(documentElement.GetElementById("checkbox"), IInputElement).Checked = True

DirectCast(documentElement.GetElementById("radio"), IInputElement).Checked = False
```



#### File

The `<input>` elements with `type=file` let the user choose one or more files from their device storage. DotNetBrowser allows to programmatically select a file and update the value of the `<input type=file>` elements.

For example, your web form contains an `<input>` element like:

```html
<input type="file" id="avatar" accept="image/png, image/jpeg" multiple>
```

You can select the required file/files programmatically using the following approach:


**C#**
```csharp
((IInputElement)documentElement.GetElementById("avatar")).Files = new[]{
    "file1.png", 
    "file2.jpeg"};
```

**VB**
```vb
DirectCast(documentElement.GetElementById("avatar"), IInputElement).Files =
{
    "file1.png",
    "file2.jpeg"
}
```



### Text area

You have a `<textarea>` element as shown below:

```html
<textarea id="details"></textarea>
```

Use the following approach to set the text in:


**C#**
```csharp
((ITextAreaElement)documentElement.GetElementById("details")).Value = "Some text...";
```

**VB**
```vb
Dim textElement = DirectCast(documentElement.GetElementById("details"), ITextAreaElement)
textElement.Value = "Some text..."
```



### Select & option

There is a `SELECT` control as follows:

```html
<select id="fruits" multiple>
    <option>Apple</option>
    <option>Orange</option>
    <option>Pineapple</option>
    <option>Banana</option>
</select>
```

You can use the following approach to select a certain item:


**C#**
```csharp
var document = browser.MainFrame.Document;
var optionElements = ((ISelectElement)document.GetElementById("fruits"))
    .Options
    .ToList();

foreach (IOptionElement optionElement in optionElements)
{
    // Check if the necessary item was found.
    if (optionElement.InnerText.Contains("Orange"))
    {
        // Select the necessary item.
        optionElement.Selected = true;
    }
}
```

**VB**
```vb
Dim document = browser.MainFrame.Document
Dim optionElements = DirectCast(document.GetElementById("fruits"), ISelectElement)
    .Options
    .ToList()

For Each optionElement As IOptionElement In optionElements
    ' Check if the necessary item was found.
    If optionElement.InnerText.Contains("Orange") Then
        ' Select the necessary item.
        optionElement.Selected = True
    End If
Next
```



Using this approach, you can select only one required option.

### Simulating click

To simulate a mouse click on an element, use the following method:


**C#**
```csharp
element.Click();
```

**VB**
```vb
element.Click()
```



When `Click()` is used with the supported elements, such as an `<input>`, it fires the element's `click` event. This event bubbles up to the elements higher in the document tree and fires their `click` events.

### Dispatching events

You can dispatch an `IEvent` at the specified `IEventTarget` using the `IEventTarget.DispatchEvent(IEvent)` method.

The code sample below demonstrates how to dispatch a standard `click` event at the specified element:


**C#**
```csharp
// Client and screen location.
Point location = new Point(10, 10);
// Create MouseEvent with the required options.
MouseEventParameters eventParameters = new MouseEventParameters
{
    Button = 0,
    ClientLocation = location,
    ScreenLocation = location,
    UiEventModifierParameters = new UiEventModifierParameters()
    {
        EventParameters = new EventParameters.Builder()
        {
            Bubbles = true,
            Cancelable = true
        }.Build()
    }
};
IMouseEvent mouseClickEvent = document.CreateMouseEvent(EventType.Click,
    eventParameters);

// Generate a click event on the target element.
element.DispatchEvent(mouseClickEvent);
```

**VB**
```vb
' Client and screen location.
Dim location As New Point(10, 10)
' Create MouseEvent with the required options.
Dim eventParameters As New MouseEventParameters With {
    .Button = 0,
    .ClientLocation = location,
    .ScreenLocation = location,
    .UiEventModifierParameters = New UiEventModifierParameters() With 
    {
        .EventParameters = New EventParameters.Builder() With 
        {
            .Bubbles = True, 
            .Cancelable = True
        }.Build()
    }
}
Dim mouseClickEvent As IMouseEvent = document.CreateMouseEvent(EventType.Click, 
    eventParameters)

' Generate a click event on the target element.
element.DispatchEvent(mouseClickEvent)
```



Using this approach, you can create and dispatch various DOM events. Such events are commonly called **synthetic events** as opposed to the events fired by the `IBrowser` itself.

### Dispatching the "change" event

In DotNetBrowser, DOM events are not automatically dispatched upon updating a value, while some websites may require them. In this case, you need to dispatch these events explicitly to make the website recognize the updates properly. The actual usage of `DispatchEvent` depends on the JavaScript frameworks you are interacting with.

The most common case is dispatching the `change` event after updating the input field to trigger the `onchange` event listener in JavaScript. For example:


**C#**
```csharp
IDocument document = Browser.MainFrame.Document;
IInputElement email = document.GetElementById("email") as IInputElement;
email.Value = "me@example.com";
email.DispatchEvent(document.CreateEvent(EventType.Change, 
    new EventParameters.Builder().Build()));
```

**VB**
```vb
Dim document As IDocument = Browser.MainFrame.Document
Dim email = TryCast(document.GetElementById("email"), IInputElement)
email.Value = "me@example.com"
email.DispatchEvent(document.CreateEvent(EventType.Change,
    (New EventParameters.Builder()).Build()))
```




## Injecting a custom CSS

You can specify custom CSS rules to be applied to every page loaded in the `IBrowser` instance.

You can configure custom CSS by setting the `IBrowser.InjectCssHandler` property. The CSS rules will be applied to the next page loaded in the Browser.


**C#**
```csharp
string hideOverflowCss = "HTML, BODY {overflow:hidden;}";
browser.InjectCssHandler = 
    new Handler<InjectCssParameters, InjectCssResponse>(p =>
    {
        return InjectCssResponse.Inject(hideOverflowCss);
    });
```

**VB**
```vb
Dim hideOverflowCss = "HTML, BODY {overflow:hidden;}"
browser.InjectCssHandler = 
    New Handler(Of InjectCssParameters, InjectCssResponse)(Function(p)
        Return InjectCssResponse.Inject(hideOverflowCss)
    End Function)
```


