# <a id="DotNetBrowser_Frames_IFrame"></a> Interface IFrame

Namespace: [DotNetBrowser.Frames](DotNetBrowser.Frames.md)  
Assembly: DotNetBrowser.dll  

Represents a frame in the browser.
Each web page loaded in the browser has a main(top-level) frame. The frame itself may have child
frames. When a web page is unloaded, its frame and all child frames are closed automatically.

```csharp
public interface IFrame : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Extension Methods

[JsonExtensions.ParseJsonString<T\>\(IFrame, string\)](DotNetBrowser.Js.JsonExtensions.md\#DotNetBrowser\_Js\_JsonExtensions\_ParseJsonString\_\_1\_DotNetBrowser\_Frames\_IFrame\_System\_String\_), 
[JsonExtensions.ParseJsonString\(IFrame, string\)](DotNetBrowser.Js.JsonExtensions.md\#DotNetBrowser\_Js\_JsonExtensions\_ParseJsonString\_DotNetBrowser\_Frames\_IFrame\_System\_String\_)

## Properties

### <a id="DotNetBrowser_Frames_IFrame_Browser"></a> Browser

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this frame.

```csharp
IBrowser Browser { get; }
```

#### Property Value

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

### <a id="DotNetBrowser_Frames_IFrame_Children"></a> Children

The collection of the child frames.

```csharp
IEnumerable<IFrame> Children { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IFrame](DotNetBrowser.Frames.IFrame.md)\>

### <a id="DotNetBrowser_Frames_IFrame_Document"></a> Document

The <xref href="DotNetBrowser.Dom.IDocument" data-throw-if-not-resolved="false"></xref> that can be used to work with DOM of the frame. Can be null if the frame doesn't have
a document.

```csharp
IDocument Document { get; }
```

#### Property Value

 [IDocument](DotNetBrowser.Dom.IDocument.md)

### <a id="DotNetBrowser_Frames_IFrame_Html"></a> Html

The HTML content of the frame. Can be an empty string
if the frame doesn't have a content or its content is empty.

```csharp
string Html { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Frames_IFrame_IsMain"></a> IsMain

Indicates whether the frame is a main (top-level) frame in the browser.

```csharp
bool IsMain { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Frames_IFrame_LocalStorage"></a> LocalStorage

The <code>localStorage</code> instance of this frame.

```csharp
IWebStorage LocalStorage { get; }
```

#### Property Value

 [IWebStorage](DotNetBrowser.Frames.IWebStorage.md)

### <a id="DotNetBrowser_Frames_IFrame_Name"></a> Name

The name of the frame. Can be an empty string if the frame doesn't have a name.

```csharp
string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Frames_IFrame_Parent"></a> Parent

The parent frame.

```csharp
IFrame Parent { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

### <a id="DotNetBrowser_Frames_IFrame_SelectedHtml"></a> SelectedHtml

The HTML representation of the selected content in the frame. Can be an empty string if there's no selection.

```csharp
string SelectedHtml { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Frames_IFrame_SelectedText"></a> SelectedText

The text representation of the selected content in the frame. Can be an empty string if there's no selection.

```csharp
string SelectedText { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Frames_IFrame_SessionStorage"></a> SessionStorage

The <code>sessionStorage</code> instance of this frame.

```csharp
IWebStorage SessionStorage { get; }
```

#### Property Value

 [IWebStorage](DotNetBrowser.Frames.IWebStorage.md)

### <a id="DotNetBrowser_Frames_IFrame_Text"></a> Text

Gets the content of the frame and its sub-frames as plain text or an empty string if the
frame does not have content or its content is empty.

```csharp
string Text { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

Limitations:

<p>
    If the frame has sub-frames from another domain, their text will not be included into
    the return value.
</p>
<p>No specification is given for how text from one frame will be delimited from the next.</p>
<p>
    The return value may contain text that is not visible to the user, whether due to
    scrolling, <code>display:none</code>, unexpanded divs, etc.
</p>
<p>
    The ordering of the text does not reflect the ordering of the text on the page as seen
    by the user. Each element's text may appear in a totally different position in the result
    from its position on the page.
</p>
<p>
    Please note that this functionality is resource-intensive, consuming significant memory
    and CPU during a text capture.
</p>

## Methods

### <a id="DotNetBrowser_Frames_IFrame_CreateJsArray__1_System_Collections_Generic_IEnumerable___0__"></a> CreateJsArray<T\>\(IEnumerable<T\>\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> and copies the contents of the <xref href="System.Collections.Generic.IEnumerable%601" data-throw-if-not-resolved="false"></xref> to it.

```csharp
IJsArray CreateJsArray<T>(IEnumerable<T> enumerable)
```

#### Parameters

`enumerable` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<T\>

The enumerable to copy values from.

#### Returns

 [IJsArray](DotNetBrowser.Js.Collections.IJsArray.md)

An <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> that contains values
from the <xref href="System.Collections.Generic.IEnumerable%601" data-throw-if-not-resolved="false"></xref>.

#### Type Parameters

`T` 

#### Remarks

The values are converted to their JavaScript representations during copying.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IFrame_CreateJsArrayBuffer_System_Byte___"></a> CreateJsArrayBuffer\(byte\[\]\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> and copies the contents of the byte array to it.

```csharp
IJsArrayBuffer CreateJsArrayBuffer(byte[] data)
```

#### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The byte array to copy data from.

#### Returns

 [IJsArrayBuffer](DotNetBrowser.Js.Collections.IJsArrayBuffer.md)

An <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> that contains values
from the byte array.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IFrame_CreateJsMap__2_System_Collections_Generic_IDictionary___0___1__"></a> CreateJsMap<TKey, TValue\>\(IDictionary<TKey, TValue\>\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> and copies the contents of the <xref href="System.Collections.Generic.IDictionary%602" data-throw-if-not-resolved="false"></xref> to it.

```csharp
IJsMap CreateJsMap<TKey, TValue>(IDictionary<TKey, TValue> dictionary)
```

#### Parameters

`dictionary` [IDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.idictionary\-2)<TKey, TValue\>

The dictionary to copy elements from.

#### Returns

 [IJsMap](DotNetBrowser.Js.Collections.IJsMap.md)

An <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> that contains values
from the provided dictionary.

#### Type Parameters

`TKey` 

`TValue` 

#### Remarks

The values are converted to their JavaScript representations during copying.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IFrame_CreateJsMap__2_System_Collections_Generic_IReadOnlyDictionary___0___1__"></a> CreateJsMap<TKey, TValue\>\(IReadOnlyDictionary<TKey, TValue\>\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> and copies the contents of the <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref>
to it.

```csharp
IJsMap CreateJsMap<TKey, TValue>(IReadOnlyDictionary<TKey, TValue> dictionary)
```

#### Parameters

`dictionary` [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<TKey, TValue\>

The dictionary to copy elements from.

#### Returns

 [IJsMap](DotNetBrowser.Js.Collections.IJsMap.md)

An <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> that contains values
from the provided dictionary.

#### Type Parameters

`TKey` 

`TValue` 

#### Remarks

The values are converted to their JavaScript representations during copying.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IFrame_CreateJsSet__1_System_Collections_Generic_IEnumerable___0__"></a> CreateJsSet<T\>\(IEnumerable<T\>\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> and copies the contents of the <xref href="System.Collections.Generic.IEnumerable%601" data-throw-if-not-resolved="false"></xref> to it.

```csharp
IJsSet CreateJsSet<T>(IEnumerable<T> collection)
```

#### Parameters

`collection` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<T\>

The collection to copy elements from.

#### Returns

 [IJsSet](DotNetBrowser.Js.Collections.IJsSet.md)

An <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> that contains values
from the provided collection.

#### Type Parameters

`T` 

#### Remarks

The values are converted to their JavaScript representations during copying.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IFrame_Execute_DotNetBrowser_Frames_EditorCommand_"></a> Execute\(EditorCommand\)

Executes the given <code class="paramref">command</code> in the frame.
Before executing the command, it's recommended to check whether it can be executed or not
using the <xref href="DotNetBrowser.Frames.IFrame.IsCommandEnabled(DotNetBrowser.Frames.EditorCommand)" data-throw-if-not-resolved="false"></xref> method.

```csharp
bool Execute(EditorCommand command)
```

#### Parameters

`command` [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The command to execute. Cannot be null.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the command has been executed successfully.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">command</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IFrame_ExecuteJavaScript__1_System_String_System_Boolean_"></a> ExecuteJavaScript<T\>\(string, bool\)

Asynchronously executes JavaScript code using the current context and
converts the execution result to the specified .NET type.

```csharp
Task<T> ExecuteJavaScript<T>(string javaScript, bool userGesture = false)
```

#### Parameters

`javaScript` [string](https://learn.microsoft.com/dotnet/api/system.string)

The JavaScript code.

`userGesture` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

Indicates whether JavaScript is initiated by a user gesture.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<T\>

The task that can be used to wait for completion and obtain the result of the JavaScript execution.

#### Type Parameters

`T` 

.NET type of the result

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">javaScript</code> is null, empty, or contains only blank
characters.

### <a id="DotNetBrowser_Frames_IFrame_ExecuteJavaScript_System_String_System_Boolean_"></a> ExecuteJavaScript\(string, bool\)

Asynchronously executes JavaScript code using the current context.

```csharp
Task<object> ExecuteJavaScript(string javaScript, bool userGesture = false)
```

#### Parameters

`javaScript` [string](https://learn.microsoft.com/dotnet/api/system.string)

The JavaScript code to execute.

`userGesture` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

Indicates whether JavaScript is initiated by a user gesture.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The task that can be used to wait for completion and obtain the result of the JavaScript execution.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">javaScript</code> is null, empty, or contains only blank
characters.

### <a id="DotNetBrowser_Frames_IFrame_Inspect_DotNetBrowser_Geometry_Point_"></a> Inspect\(Point\)

Inspects the given <code class="paramref">location</code> in the frame and returns the result of inspection.

```csharp
PointInspection Inspect(Point location)
```

#### Parameters

`location` [Point](DotNetBrowser.Geometry.Point.md)

A point in the frame's view. Cannot be null.

#### Returns

 [PointInspection](DotNetBrowser.Dom.PointInspection.md)

The result of inspection that contains the details about the DOM node at the given location.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">location</code> is null.

### <a id="DotNetBrowser_Frames_IFrame_Inspect_System_Int32_System_Int32_"></a> Inspect\(int, int\)

Inspects the given location in the frame and returns the result of inspection.

```csharp
PointInspection Inspect(int x, int y)
```

#### Parameters

`x` [int](https://learn.microsoft.com/dotnet/api/system.int32)

a horizontal coordinate on the web page

`y` [int](https://learn.microsoft.com/dotnet/api/system.int32)

a vertical coordinate on the web page

#### Returns

 [PointInspection](DotNetBrowser.Dom.PointInspection.md)

The result of inspection that contains the details about the DOM node at the given location.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IFrame_IsCommandEnabled_DotNetBrowser_Frames_EditorCommand_"></a> IsCommandEnabled\(EditorCommand\)

Indicates if the command with the given <code class="paramref">command</code> can be executed in the frame.
Some commands can be executed only under certain conditions.
For example, the <xref href="DotNetBrowser.Frames.EditorCommand.InsertText(System.String)" data-throw-if-not-resolved="false"></xref> command can be executed only if there's a focused text
field in the frame.

```csharp
bool IsCommandEnabled(EditorCommand command)
```

#### Parameters

`command` [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The command to check.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the command is enabled and can be executed.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">command</code> is null.

### <a id="DotNetBrowser_Frames_IFrame_LoadUrl_System_String_"></a> LoadUrl\(string\)

Navigates the frame to a resource identified by the given <code class="paramref">url</code>.

```csharp
Task<NavigationResult> LoadUrl(string url)
```

#### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to load. Cannot be null, empty or contain only white space.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.NavigationResult.md)\>

A task that represents the asynchronous loading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the loading operation has been completed, stopped or failed.
The task throws a <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the loading operation hasn't been completed within a default timeout (100 seconds).

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

thrown when <code class="paramref">url</code>is null, empty or contain only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IFrame_LoadUrl_System_String_System_TimeSpan_"></a> LoadUrl\(string, TimeSpan\)

Navigates the frame to a resource identified by the given <code class="paramref">url</code>.

```csharp
Task<NavigationResult> LoadUrl(string url, TimeSpan timeout)
```

#### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to load. Cannot be null, empty or contain only white space.

`timeout` [TimeSpan](https://learn.microsoft.com/dotnet/api/system.timespan)

The timeout.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.NavigationResult.md)\>

A task that represents the asynchronous loading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the loading operation has been completed, stopped or failed.
The task throws a  <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the loading operation hasn't been completed within the specified
<code class="paramref">timeout</code>.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

thrown when <code class="paramref">url</code>is null, empty or contain only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Frames_IFrame_Print"></a> Print\(\)

Requests printing of the currently loaded web page in this frame.

```csharp
void Print()
```

#### Remarks

<p>
    The printing should be allowed in the <xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref>, in other case, it will be
    canceled.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

The print operation failed. This can happen when the frame itself does not exist anymore.

### <a id="DotNetBrowser_Frames_IFrame_ViewSource"></a> ViewSource\(\)

Opens a popup with the frame's source like the browser does when showing page source.

```csharp
void ViewSource()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

