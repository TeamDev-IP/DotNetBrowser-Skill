# <a id="DotNetBrowser_Frames"></a> Namespace DotNetBrowser.Frames

### Namespaces

 [DotNetBrowser.Frames.Handlers](DotNetBrowser.Frames.Handlers.md)

### Classes

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

Provides the supported commands that can be executed in a <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

 [WebStorageException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageException)

Thrown by <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> properties and  methods to indicate that the requested operation failed. This
is a superclass of the exceptions that can be thrown during working with <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref>.

 [WebStorageOverflowException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageOverflowException)

Thrown by <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> indexer if the new value size exceeds the
available space in the storage.

 [WebStorageSecurityException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageSecurityException)

Thrown by <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> methods if the access to the web storage is forbidden for the
current document.

### Interfaces

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

Represents a frame in the browser.
Each web page loaded in the browser has a main(top-level) frame. The frame itself may have child
frames. When a web page is unloaded, its frame and all child frames are closed automatically.

 [IWebStorage](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IWebStorage)

<p>An HTML WebStorage.</p>
<p>
    Provides access to the session storage or local storage for a particular document on the loaded
    web page. Allows you to add, modify, or delete the stored items.
</p>

## <a id="DotNetBrowser_Frames_EditorCommand"></a> Class EditorCommand

Namespace: [DotNetBrowser.Frames](DotNetBrowser.Frames.md)  
Assembly: DotNetBrowser.dll  

Provides the supported commands that can be executed in a <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class EditorCommand
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Frames_EditorCommand_BackColor_System_String_"></a> BackColor\(string\)

Returns a command that allows setting the background color for selected text in a WYSIWYG editor.

```csharp
public static EditorCommand BackColor(string color)
```

##### Parameters

`color` [string](https://learn.microsoft.com/dotnet/api/system.string)

the color to set.

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">color</code> is null, empty or contain only white
space.

#### <a id="DotNetBrowser_Frames_EditorCommand_Bold"></a> Bold\(\)

Returns a command that allows making the selected text bold in a WYSIWYG editor.

```csharp
public static EditorCommand Bold()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_Copy"></a> Copy\(\)

Returns a command that allows copying the selected text in the frame.

```csharp
public static EditorCommand Copy()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_Cut"></a> Cut\(\)

Returns a command that allows cutting the selected text in a text field, text area or WYSIWYG editor.

```csharp
public static EditorCommand Cut()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_Delete"></a> Delete\(\)

Returns a command that allows deleting the selected text in a text field, text area or WYSIWYG editor.

```csharp
public static EditorCommand Delete()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_DeleteBackward"></a> DeleteBackward\(\)

Returns a command that allows deleting character before the caret position in a text field,
text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteBackward()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_DeleteForward"></a> DeleteForward\(\)

Returns a command that allows deleting character after the caret position in a text field,
text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteForward()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_DeleteToBeginningOfLine"></a> DeleteToBeginningOfLine\(\)

Returns a command that allows deleting character from the caret position to the beginning of
line in a text field, text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteToBeginningOfLine()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_DeleteWordBackward"></a> DeleteWordBackward\(\)

Returns a command that allows deleting a word before the caret position in a text field,
text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteWordBackward()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_DeleteWordForward"></a> DeleteWordForward\(\)

Returns a command that allows deleting a word after the caret position in a text field,
text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteWordForward()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_FindText_System_String_"></a> FindText\(string\)

Returns a command that allows searching for the given <code class="paramref">text</code> occurrence from the
current caret position in the frame. If match found, this command will select it and scroll
down to make it visible, if needed.

```csharp
public static EditorCommand FindText(string text)
```

##### Parameters

`text` [string](https://learn.microsoft.com/dotnet/api/system.string)

the text to search.

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">text</code> is null, empty or contain only white
space.

#### <a id="DotNetBrowser_Frames_EditorCommand_FontName_System_String_"></a> FontName\(string\)

Returns a command that allows setting the given <code class="paramref">fontName</code> for the selected text in a WYSIWYG
editor.

```csharp
public static EditorCommand FontName(string fontName)
```

##### Parameters

`fontName` [string](https://learn.microsoft.com/dotnet/api/system.string)

the font name to set.

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">fontName</code> is null, empty or contain only white
space.

#### <a id="DotNetBrowser_Frames_EditorCommand_FontSize_System_Int32_"></a> FontSize\(int\)

Returns a command that allows setting the given <code class="paramref">fontSize</code> for the selected text in a WYSIWYG
editor.

```csharp
public static EditorCommand FontSize(int fontSize)
```

##### Parameters

`fontSize` [int](https://learn.microsoft.com/dotnet/api/system.int32)

the font size to set.

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">fontSize</code> is less or equal to zero.

#### <a id="DotNetBrowser_Frames_EditorCommand_ForeColor_System_String_"></a> ForeColor\(string\)

Returns a command that allows setting the given foreground <code class="paramref">color</code> for the selected
text in a WYSIWYG editor.

```csharp
public static EditorCommand ForeColor(string color)
```

##### Parameters

`color` [string](https://learn.microsoft.com/dotnet/api/system.string)

the color to set.

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">color</code> is null, empty or contain only white
space.

#### <a id="DotNetBrowser_Frames_EditorCommand_IgnoreSpelling"></a> IgnoreSpelling\(\)

Returns a command that allows disabling the spelling mistakes highlighting in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand IgnoreSpelling()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_InsertHtml_System_String_"></a> InsertHtml\(string\)

Returns a command that allows inserting the given <code class="paramref">html</code> content in a WYSIWYG editor.

```csharp
public static EditorCommand InsertHtml(string html)
```

##### Parameters

`html` [string](https://learn.microsoft.com/dotnet/api/system.string)

the html content to insert.

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">html</code> is null, empty or contain only white
space.

#### <a id="DotNetBrowser_Frames_EditorCommand_InsertImage_System_String_"></a> InsertImage\(string\)

Returns a command that allows inserting an image with the given <code class="paramref">source</code> in a WYSIWYG editor.
If the <code class="paramref">source</code> points to an invalid location, then image won't be inserted.

```csharp
public static EditorCommand InsertImage(string source)
```

##### Parameters

`source` [string](https://learn.microsoft.com/dotnet/api/system.string)

the value of the 'src' attribute of the IMG tag

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">source</code> is null, empty or contain only white
space.

#### <a id="DotNetBrowser_Frames_EditorCommand_InsertNewLine"></a> InsertNewLine\(\)

Returns a command that allows inserting a new line in a WYSIWYG editor.

```csharp
public static EditorCommand InsertNewLine()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_InsertParagraph"></a> InsertParagraph\(\)

Inserts new paragraph in a WYSIWYG editor.

```csharp
public static EditorCommand InsertParagraph()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_InsertTab"></a> InsertTab\(\)

Returns a command that allows inserting a tab character in a WYSIWYG editor.

```csharp
public static EditorCommand InsertTab()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_InsertText_System_String_"></a> InsertText\(string\)

Returns a command that allows inserting the given <code class="paramref">text</code> content in a WYSIWYG editor or a text
field.

```csharp
public static EditorCommand InsertText(string text)
```

##### Parameters

`text` [string](https://learn.microsoft.com/dotnet/api/system.string)

the text to insert.

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">text</code> is null, empty or contain only white
space.

#### <a id="DotNetBrowser_Frames_EditorCommand_Italic"></a> Italic\(\)

Returns a command that allows making the selected text italic in a WYSIWYG editor.

```csharp
public static EditorCommand Italic()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MovePageDown"></a> MovePageDown\(\)

Returns a command that allows moving the caret position at one page down in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MovePageDown()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MovePageUp"></a> MovePageUp\(\)

Returns a command that allows moving the caret position at one page up in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MovePageUp()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MoveToBeginningOfLine"></a> MoveToBeginningOfLine\(\)

Returns a command that allows moving a word to the beginning of line in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveToBeginningOfLine()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MoveToBeginningOfLineAndModifySelection"></a> MoveToBeginningOfLineAndModifySelection\(\)

Returns a command that allows moving a word to the beginning of line and modifying selection
in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveToBeginningOfLineAndModifySelection()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MoveToEndOfLine"></a> MoveToEndOfLine\(\)

Returns a command that allows moving a word to the end of line in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveToEndOfLine()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MoveToEndOfLineAndModifySelection"></a> MoveToEndOfLineAndModifySelection\(\)

Returns a command that allows moving a word to the end of line and modifying selection in a
text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveToEndOfLineAndModifySelection()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MoveWordLeft"></a> MoveWordLeft\(\)

Returns a command that allows moving a word left in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveWordLeft()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MoveWordLeftAndModifySelection"></a> MoveWordLeftAndModifySelection\(\)

Returns a command that allows moving a word left and modifying selection in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveWordLeftAndModifySelection()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MoveWordRight"></a> MoveWordRight\(\)

Returns a command that allows moving a word right in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveWordRight()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_MoveWordRightAndModifySelection"></a> MoveWordRightAndModifySelection\(\)

Returns a command that allows moving a word right and modifying selection in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveWordRightAndModifySelection()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_Paste"></a> Paste\(\)

Returns a command that allows pasting content of the clipboard in a text field, text area or
a WYSIWYG editor.

```csharp
public static EditorCommand Paste()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_Redo"></a> Redo\(\)

Returns a command that allows reversing the last <xref href="DotNetBrowser.Frames.EditorCommand.Undo" data-throw-if-not-resolved="false"></xref> action.

```csharp
public static EditorCommand Redo()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_ScrollLineDown"></a> ScrollLineDown\(\)

Returns a command that allows scrolling one line down.

```csharp
public static EditorCommand ScrollLineDown()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_ScrollLineUp"></a> ScrollLineUp\(\)

Returns a command that allows scrolling one line up.

```csharp
public static EditorCommand ScrollLineUp()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_ScrollPageBackward"></a> ScrollPageBackward\(\)

Returns a command that allows scrolling a page backward.

```csharp
public static EditorCommand ScrollPageBackward()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_ScrollPageForward"></a> ScrollPageForward\(\)

Returns a command that allows scrolling a page forward.

```csharp
public static EditorCommand ScrollPageForward()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_ScrollToBeginningOfDocument"></a> ScrollToBeginningOfDocument\(\)

Returns a command that allows scrolling content to the beginning of the document in the frame.

```csharp
public static EditorCommand ScrollToBeginningOfDocument()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_ScrollToEndOfDocument"></a> ScrollToEndOfDocument\(\)

Returns a command that allows scrolling content to the end of the document in the frame.

```csharp
public static EditorCommand ScrollToEndOfDocument()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_SelectAll"></a> SelectAll\(\)

Returns a command that allows selecting all text in the frame or the currently focused text
field, text area or a WYSIWYG editor.

```csharp
public static EditorCommand SelectAll()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_SelectLine"></a> SelectLine\(\)

Returns a command that allows selecting a line at the caret position in a text area or a
WYSIWYG editor.

```csharp
public static EditorCommand SelectLine()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_SelectParagraph"></a> SelectParagraph\(\)

Returns a command that allows selecting the whole paragraph at the caret position in a text
area or a WYSIWYG editor.

```csharp
public static EditorCommand SelectParagraph()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_SelectSentence"></a> SelectSentence\(\)

Returns a command that allows selecting the whole sentence at the caret position in a text
area or a WYSIWYG editor.

```csharp
public static EditorCommand SelectSentence()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_SelectWord"></a> SelectWord\(\)

Returns a command that allows selecting the word at the caret position in a text field, text
area or a WYSIWYG editor.

```csharp
public static EditorCommand SelectWord()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_ToggleBold"></a> ToggleBold\(\)

Returns a command that allows toggling bold style for the selected text in a WYSIWYG editor.

```csharp
public static EditorCommand ToggleBold()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_ToggleItalic"></a> ToggleItalic\(\)

Returns a command that allows toggling italic style for the selected text in a WYSIWYG editor.

```csharp
public static EditorCommand ToggleItalic()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_ToggleUnderline"></a> ToggleUnderline\(\)

Returns a command that allows toggling underline style for the selected text in a WYSIWYG editor.

```csharp
public static EditorCommand ToggleUnderline()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_Underline"></a> Underline\(\)

Returns a command that allows underlying the selected text in a WYSIWYG editor.

```csharp
public static EditorCommand Underline()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_Undo"></a> Undo\(\)

Returns a command that allows reversing the last action.

```csharp
public static EditorCommand Undo()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### <a id="DotNetBrowser_Frames_EditorCommand_Unselect"></a> Unselect\(\)

Returns a command that allows clearing the current selection in a frame.

```csharp
public static EditorCommand Unselect()
```

##### Returns

 [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

## <a id="DotNetBrowser_Frames_WebStorageException"></a> Class WebStorageException

Namespace: [DotNetBrowser.Frames](DotNetBrowser.Frames.md)  
Assembly: DotNetBrowser.dll  

Thrown by <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> properties and  methods to indicate that the requested operation failed. This
is a superclass of the exceptions that can be thrown during working with <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref>.

```csharp
public class WebStorageException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[WebStorageException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageException)

##### Derived

[WebStorageOverflowException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageOverflowException), 
[WebStorageSecurityException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageSecurityException)

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
[Exception.SerializeObjectState](https://learn.microsoft.com/dotnet/api/system.exception.serializeobjectstate), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Frames_WebStorageException__ctor_System_String_"></a> WebStorageException\(string\)

```csharp
public WebStorageException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Frames_WebStorageOverflowException"></a> Class WebStorageOverflowException

Namespace: [DotNetBrowser.Frames](DotNetBrowser.Frames.md)  
Assembly: DotNetBrowser.dll  

Thrown by <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> indexer if the new value size exceeds the
available space in the storage.

```csharp
public class WebStorageOverflowException : WebStorageException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[WebStorageException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageException) ← 
[WebStorageOverflowException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageOverflowException)

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
[Exception.SerializeObjectState](https://learn.microsoft.com/dotnet/api/system.exception.serializeobjectstate), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Frames_WebStorageOverflowException__ctor_System_String_"></a> WebStorageOverflowException\(string\)

```csharp
public WebStorageOverflowException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Frames_WebStorageSecurityException"></a> Class WebStorageSecurityException

Namespace: [DotNetBrowser.Frames](DotNetBrowser.Frames.md)  
Assembly: DotNetBrowser.dll  

Thrown by <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> methods if the access to the web storage is forbidden for the
current document.

```csharp
public class WebStorageSecurityException : WebStorageException, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[WebStorageException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageException) ← 
[WebStorageSecurityException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageSecurityException)

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
[Exception.SerializeObjectState](https://learn.microsoft.com/dotnet/api/system.exception.serializeobjectstate), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Constructors

#### <a id="DotNetBrowser_Frames_WebStorageSecurityException__ctor_System_String_"></a> WebStorageSecurityException\(string\)

```csharp
public WebStorageSecurityException(string message)
```

##### Parameters

`message` [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Frames_IFrame"></a> Interface IFrame

Namespace: [DotNetBrowser.Frames](DotNetBrowser.Frames.md)  
Assembly: DotNetBrowser.dll  

Represents a frame in the browser.
Each web page loaded in the browser has a main(top-level) frame. The frame itself may have child
frames. When a web page is unloaded, its frame and all child frames are closed automatically.

```csharp
public interface IFrame : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Extension Methods

[JsonExtensions.ParseJsonString<T\>\(IFrame, string\)](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions_ParseJsonString__1_DotNetBrowser_Frames_IFrame_System_String_), 
[JsonExtensions.ParseJsonString\(IFrame, string\)](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions_ParseJsonString_DotNetBrowser_Frames_IFrame_System_String_)

### Properties

#### <a id="DotNetBrowser_Frames_IFrame_Browser"></a> Browser

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance associated with this frame.

```csharp
IBrowser Browser { get; }
```

##### Property Value

 [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

#### <a id="DotNetBrowser_Frames_IFrame_Children"></a> Children

The collection of the child frames.

```csharp
IEnumerable<IFrame> Children { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)\>

#### <a id="DotNetBrowser_Frames_IFrame_Document"></a> Document

The <xref href="DotNetBrowser.Dom.IDocument" data-throw-if-not-resolved="false"></xref> that can be used to work with DOM of the frame. Can be null if the frame doesn't have
a document.

```csharp
IDocument Document { get; }
```

##### Property Value

 [IDocument](DotNetBrowser.Dom.md#DotNetBrowser_Dom_IDocument)

#### <a id="DotNetBrowser_Frames_IFrame_Html"></a> Html

The HTML content of the frame. Can be an empty string
if the frame doesn't have a content or its content is empty.

```csharp
string Html { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Frames_IFrame_IsMain"></a> IsMain

Indicates whether the frame is a main (top-level) frame in the browser.

```csharp
bool IsMain { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_Frames_IFrame_LocalStorage"></a> LocalStorage

The <code>localStorage</code> instance of this frame.

```csharp
IWebStorage LocalStorage { get; }
```

##### Property Value

 [IWebStorage](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IWebStorage)

#### <a id="DotNetBrowser_Frames_IFrame_Name"></a> Name

The name of the frame. Can be an empty string if the frame doesn't have a name.

```csharp
string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Frames_IFrame_Parent"></a> Parent

The parent frame.

```csharp
IFrame Parent { get; }
```

##### Property Value

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

#### <a id="DotNetBrowser_Frames_IFrame_SelectedHtml"></a> SelectedHtml

The HTML representation of the selected content in the frame. Can be an empty string if there's no selection.

```csharp
string SelectedHtml { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Frames_IFrame_SelectedText"></a> SelectedText

The text representation of the selected content in the frame. Can be an empty string if there's no selection.

```csharp
string SelectedText { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Frames_IFrame_SessionStorage"></a> SessionStorage

The <code>sessionStorage</code> instance of this frame.

```csharp
IWebStorage SessionStorage { get; }
```

##### Property Value

 [IWebStorage](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IWebStorage)

#### <a id="DotNetBrowser_Frames_IFrame_Text"></a> Text

Gets the content of the frame and its sub-frames as plain text or an empty string if the
frame does not have content or its content is empty.

```csharp
string Text { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Remarks

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

### Methods

#### <a id="DotNetBrowser_Frames_IFrame_CreateJsArray__1_System_Collections_Generic_IEnumerable___0__"></a> CreateJsArray<T\>\(IEnumerable<T\>\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> and copies the contents of the <xref href="System.Collections.Generic.IEnumerable%601" data-throw-if-not-resolved="false"></xref> to it.

```csharp
IJsArray CreateJsArray<T>(IEnumerable<T> enumerable)
```

##### Parameters

`enumerable` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<T\>

The enumerable to copy values from.

##### Returns

 [IJsArray](DotNetBrowser.Js.Collections.md#DotNetBrowser_Js_Collections_IJsArray)

An <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> that contains values
from the <xref href="System.Collections.Generic.IEnumerable%601" data-throw-if-not-resolved="false"></xref>.

##### Type Parameters

`T` 

##### Remarks

The values are converted to their JavaScript representations during copying.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IFrame_CreateJsArrayBuffer_System_Byte___"></a> CreateJsArrayBuffer\(byte\[\]\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> and copies the contents of the byte array to it.

```csharp
IJsArrayBuffer CreateJsArrayBuffer(byte[] data)
```

##### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The byte array to copy data from.

##### Returns

 [IJsArrayBuffer](DotNetBrowser.Js.Collections.md#DotNetBrowser_Js_Collections_IJsArrayBuffer)

An <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> that contains values
from the byte array.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IFrame_CreateJsMap__2_System_Collections_Generic_IDictionary___0___1__"></a> CreateJsMap<TKey, TValue\>\(IDictionary<TKey, TValue\>\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> and copies the contents of the <xref href="System.Collections.Generic.IDictionary%602" data-throw-if-not-resolved="false"></xref> to it.

```csharp
IJsMap CreateJsMap<TKey, TValue>(IDictionary<TKey, TValue> dictionary)
```

##### Parameters

`dictionary` [IDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.idictionary\-2)<TKey, TValue\>

The dictionary to copy elements from.

##### Returns

 [IJsMap](DotNetBrowser.Js.Collections.md#DotNetBrowser_Js_Collections_IJsMap)

An <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> that contains values
from the provided dictionary.

##### Type Parameters

`TKey` 

`TValue` 

##### Remarks

The values are converted to their JavaScript representations during copying.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IFrame_CreateJsMap__2_System_Collections_Generic_IReadOnlyDictionary___0___1__"></a> CreateJsMap<TKey, TValue\>\(IReadOnlyDictionary<TKey, TValue\>\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> and copies the contents of the <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref>
to it.

```csharp
IJsMap CreateJsMap<TKey, TValue>(IReadOnlyDictionary<TKey, TValue> dictionary)
```

##### Parameters

`dictionary` [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<TKey, TValue\>

The dictionary to copy elements from.

##### Returns

 [IJsMap](DotNetBrowser.Js.Collections.md#DotNetBrowser_Js_Collections_IJsMap)

An <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> that contains values
from the provided dictionary.

##### Type Parameters

`TKey` 

`TValue` 

##### Remarks

The values are converted to their JavaScript representations during copying.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IFrame_CreateJsSet__1_System_Collections_Generic_IEnumerable___0__"></a> CreateJsSet<T\>\(IEnumerable<T\>\)

Creates a new <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> and copies the contents of the <xref href="System.Collections.Generic.IEnumerable%601" data-throw-if-not-resolved="false"></xref> to it.

```csharp
IJsSet CreateJsSet<T>(IEnumerable<T> collection)
```

##### Parameters

`collection` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<T\>

The collection to copy elements from.

##### Returns

 [IJsSet](DotNetBrowser.Js.Collections.md#DotNetBrowser_Js_Collections_IJsSet)

An <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> that contains values
from the provided collection.

##### Type Parameters

`T` 

##### Remarks

The values are converted to their JavaScript representations during copying.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IFrame_Execute_DotNetBrowser_Frames_EditorCommand_"></a> Execute\(EditorCommand\)

Executes the given <code class="paramref">command</code> in the frame.
Before executing the command, it's recommended to check whether it can be executed or not
using the <xref href="DotNetBrowser.Frames.IFrame.IsCommandEnabled(DotNetBrowser.Frames.EditorCommand)" data-throw-if-not-resolved="false"></xref> method.

```csharp
bool Execute(EditorCommand command)
```

##### Parameters

`command` [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The command to execute. Cannot be null.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the command has been executed successfully.

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">command</code> is null.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IFrame_ExecuteJavaScript__1_System_String_System_Boolean_"></a> ExecuteJavaScript<T\>\(string, bool\)

Asynchronously executes JavaScript code using the current context and
converts the execution result to the specified .NET type.

```csharp
Task<T> ExecuteJavaScript<T>(string javaScript, bool userGesture = false)
```

##### Parameters

`javaScript` [string](https://learn.microsoft.com/dotnet/api/system.string)

The JavaScript code.

`userGesture` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

Indicates whether JavaScript is initiated by a user gesture.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<T\>

The task that can be used to wait for completion and obtain the result of the JavaScript execution.

##### Type Parameters

`T` 

.NET type of the result

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">javaScript</code> is null, empty, or contains only blank
characters.

#### <a id="DotNetBrowser_Frames_IFrame_ExecuteJavaScript_System_String_System_Boolean_"></a> ExecuteJavaScript\(string, bool\)

Asynchronously executes JavaScript code using the current context.

```csharp
Task<object> ExecuteJavaScript(string javaScript, bool userGesture = false)
```

##### Parameters

`javaScript` [string](https://learn.microsoft.com/dotnet/api/system.string)

The JavaScript code to execute.

`userGesture` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

Indicates whether JavaScript is initiated by a user gesture.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The task that can be used to wait for completion and obtain the result of the JavaScript execution.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">javaScript</code> is null, empty, or contains only blank
characters.

#### <a id="DotNetBrowser_Frames_IFrame_Inspect_DotNetBrowser_Geometry_Point_"></a> Inspect\(Point\)

Inspects the given <code class="paramref">location</code> in the frame and returns the result of inspection.

```csharp
PointInspection Inspect(Point location)
```

##### Parameters

`location` [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

A point in the frame's view. Cannot be null.

##### Returns

 [PointInspection](DotNetBrowser.Dom.md#DotNetBrowser_Dom_PointInspection)

The result of inspection that contains the details about the DOM node at the given location.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">location</code> is null.

#### <a id="DotNetBrowser_Frames_IFrame_Inspect_System_Int32_System_Int32_"></a> Inspect\(int, int\)

Inspects the given location in the frame and returns the result of inspection.

```csharp
PointInspection Inspect(int x, int y)
```

##### Parameters

`x` [int](https://learn.microsoft.com/dotnet/api/system.int32)

a horizontal coordinate on the web page

`y` [int](https://learn.microsoft.com/dotnet/api/system.int32)

a vertical coordinate on the web page

##### Returns

 [PointInspection](DotNetBrowser.Dom.md#DotNetBrowser_Dom_PointInspection)

The result of inspection that contains the details about the DOM node at the given location.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IFrame_IsCommandEnabled_DotNetBrowser_Frames_EditorCommand_"></a> IsCommandEnabled\(EditorCommand\)

Indicates if the command with the given <code class="paramref">command</code> can be executed in the frame.
Some commands can be executed only under certain conditions.
For example, the <xref href="DotNetBrowser.Frames.EditorCommand.InsertText(System.String)" data-throw-if-not-resolved="false"></xref> command can be executed only if there's a focused text
field in the frame.

```csharp
bool IsCommandEnabled(EditorCommand command)
```

##### Parameters

`command` [EditorCommand](DotNetBrowser.Frames.md#DotNetBrowser_Frames_EditorCommand)

The command to check.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the command is enabled and can be executed.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">command</code> is null.

#### <a id="DotNetBrowser_Frames_IFrame_LoadUrl_System_String_"></a> LoadUrl\(string\)

Navigates the frame to a resource identified by the given <code class="paramref">url</code>.

```csharp
Task<NavigationResult> LoadUrl(string url)
```

##### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to load. Cannot be null, empty or contain only white space.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous loading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the loading operation has been completed, stopped or failed.
The task throws a <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the loading operation hasn't been completed within a default timeout (100 seconds).

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

thrown when <code class="paramref">url</code>is null, empty or contain only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IFrame_LoadUrl_System_String_System_TimeSpan_"></a> LoadUrl\(string, TimeSpan\)

Navigates the frame to a resource identified by the given <code class="paramref">url</code>.

```csharp
Task<NavigationResult> LoadUrl(string url, TimeSpan timeout)
```

##### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to load. Cannot be null, empty or contain only white space.

`timeout` [TimeSpan](https://learn.microsoft.com/dotnet/api/system.timespan)

The timeout.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[NavigationResult](DotNetBrowser.Navigation.md#DotNetBrowser_Navigation_NavigationResult)\>

A task that represents the asynchronous loading operation.
The <xref href="DotNetBrowser.Navigation.NavigationResult" data-throw-if-not-resolved="false"></xref> indicates if the loading operation has been completed, stopped or failed.
The task throws a  <xref href="System.TimeoutException" data-throw-if-not-resolved="false"></xref>
if the loading operation hasn't been completed within the specified
<code class="paramref">timeout</code>.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

thrown when <code class="paramref">url</code>is null, empty or contain only white space.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IFrame_Print"></a> Print\(\)

Requests printing of the currently loaded web page in this frame.

```csharp
void Print()
```

##### Remarks

<p>
    The printing should be allowed in the <xref href="DotNetBrowser.Browser.IBrowser.RequestPrintHandler" data-throw-if-not-resolved="false"></xref>, in other case, it will be
    canceled.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

The print operation failed. This can happen when the frame itself does not exist anymore.

#### <a id="DotNetBrowser_Frames_IFrame_ViewSource"></a> ViewSource\(\)

Opens a popup with the frame's source like the browser does when showing page source.

```csharp
void ViewSource()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> object has already been disposed.

## <a id="DotNetBrowser_Frames_IWebStorage"></a> Interface IWebStorage

Namespace: [DotNetBrowser.Frames](DotNetBrowser.Frames.md)  
Assembly: DotNetBrowser.dll  

<p>An HTML WebStorage.</p>
<p>
    Provides access to the session storage or local storage for a particular document on the loaded
    web page. Allows you to add, modify, or delete the stored items.
</p>

```csharp
public interface IWebStorage : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Frames_IWebStorage_Count"></a> Count

Gets the number of the key/value pairs in the storage.

```csharp
int Count { get; }
```

##### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageException)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.

#### <a id="DotNetBrowser_Frames_IWebStorage_Keys"></a> Keys

Gets a list of the web storage keys.

```csharp
IReadOnlyList<string> Keys { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Frames_IWebStorage_Item_System_String_"></a> this\[string\]

Gets or sets the value associated with the given <code class="paramref">key</code>. The setter adds the item with the
specified <code class="paramref">key</code> and
<code class="paramref">value</code> to the storage, or updates it if the item with the given <code class="paramref">key</code> already
exists.

```csharp
string this[string key] { get; set; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageException)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.

### Methods

#### <a id="DotNetBrowser_Frames_IWebStorage_Clear"></a> Clear\(\)

Removes all the items from the storage.

```csharp
void Clear()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageException)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.

#### <a id="DotNetBrowser_Frames_IWebStorage_Contains_System_String_"></a> Contains\(string\)

Checks if the specified key is present in the storage.

```csharp
bool Contains(string key)
```

##### Parameters

`key` [string](https://learn.microsoft.com/dotnet/api/system.string)

the key name to check. Can be empty or blank.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the storage contains an item with the specified <code class="paramref">key</code>,
otherwise <code>false</code>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageException)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.

#### <a id="DotNetBrowser_Frames_IWebStorage_Remove_System_String_"></a> Remove\(string\)

Removes the item with the specified <code class="paramref">key</code> from the storage. Does nothing if there is no
item with the specified <code class="paramref">key</code> in the storage.

```csharp
void Remove(string key)
```

##### Parameters

`key` [string](https://learn.microsoft.com/dotnet/api/system.string)

the key name of the item to remove. Can be empty or blank.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [WebStorageException](DotNetBrowser.Frames.md#DotNetBrowser_Frames_WebStorageException)

The <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> operation has failed.
