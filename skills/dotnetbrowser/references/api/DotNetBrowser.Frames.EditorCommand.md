# <a id="DotNetBrowser_Frames_EditorCommand"></a> Class EditorCommand

Namespace: [DotNetBrowser.Frames](DotNetBrowser.Frames.md)  
Assembly: DotNetBrowser.dll  

Provides the supported commands that can be executed in a <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class EditorCommand
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Frames_EditorCommand_BackColor_System_String_"></a> BackColor\(string\)

Returns a command that allows setting the background color for selected text in a WYSIWYG editor.

```csharp
public static EditorCommand BackColor(string color)
```

#### Parameters

`color` [string](https://learn.microsoft.com/dotnet/api/system.string)

the color to set.

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">color</code> is null, empty or contain only white
space.

### <a id="DotNetBrowser_Frames_EditorCommand_Bold"></a> Bold\(\)

Returns a command that allows making the selected text bold in a WYSIWYG editor.

```csharp
public static EditorCommand Bold()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_Copy"></a> Copy\(\)

Returns a command that allows copying the selected text in the frame.

```csharp
public static EditorCommand Copy()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_Cut"></a> Cut\(\)

Returns a command that allows cutting the selected text in a text field, text area or WYSIWYG editor.

```csharp
public static EditorCommand Cut()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_Delete"></a> Delete\(\)

Returns a command that allows deleting the selected text in a text field, text area or WYSIWYG editor.

```csharp
public static EditorCommand Delete()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_DeleteBackward"></a> DeleteBackward\(\)

Returns a command that allows deleting character before the caret position in a text field,
text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteBackward()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_DeleteForward"></a> DeleteForward\(\)

Returns a command that allows deleting character after the caret position in a text field,
text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteForward()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_DeleteToBeginningOfLine"></a> DeleteToBeginningOfLine\(\)

Returns a command that allows deleting character from the caret position to the beginning of
line in a text field, text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteToBeginningOfLine()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_DeleteWordBackward"></a> DeleteWordBackward\(\)

Returns a command that allows deleting a word before the caret position in a text field,
text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteWordBackward()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_DeleteWordForward"></a> DeleteWordForward\(\)

Returns a command that allows deleting a word after the caret position in a text field,
text area or WYSIWYG editor.

```csharp
public static EditorCommand DeleteWordForward()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_FindText_System_String_"></a> FindText\(string\)

Returns a command that allows searching for the given <code class="paramref">text</code> occurrence from the
current caret position in the frame. If match found, this command will select it and scroll
down to make it visible, if needed.

```csharp
public static EditorCommand FindText(string text)
```

#### Parameters

`text` [string](https://learn.microsoft.com/dotnet/api/system.string)

the text to search.

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">text</code> is null, empty or contain only white
space.

### <a id="DotNetBrowser_Frames_EditorCommand_FontName_System_String_"></a> FontName\(string\)

Returns a command that allows setting the given <code class="paramref">fontName</code> for the selected text in a WYSIWYG
editor.

```csharp
public static EditorCommand FontName(string fontName)
```

#### Parameters

`fontName` [string](https://learn.microsoft.com/dotnet/api/system.string)

the font name to set.

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">fontName</code> is null, empty or contain only white
space.

### <a id="DotNetBrowser_Frames_EditorCommand_FontSize_System_Int32_"></a> FontSize\(int\)

Returns a command that allows setting the given <code class="paramref">fontSize</code> for the selected text in a WYSIWYG
editor.

```csharp
public static EditorCommand FontSize(int fontSize)
```

#### Parameters

`fontSize` [int](https://learn.microsoft.com/dotnet/api/system.int32)

the font size to set.

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">fontSize</code> is less or equal to zero.

### <a id="DotNetBrowser_Frames_EditorCommand_ForeColor_System_String_"></a> ForeColor\(string\)

Returns a command that allows setting the given foreground <code class="paramref">color</code> for the selected
text in a WYSIWYG editor.

```csharp
public static EditorCommand ForeColor(string color)
```

#### Parameters

`color` [string](https://learn.microsoft.com/dotnet/api/system.string)

the color to set.

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">color</code> is null, empty or contain only white
space.

### <a id="DotNetBrowser_Frames_EditorCommand_IgnoreSpelling"></a> IgnoreSpelling\(\)

Returns a command that allows disabling the spelling mistakes highlighting in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand IgnoreSpelling()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_InsertHtml_System_String_"></a> InsertHtml\(string\)

Returns a command that allows inserting the given <code class="paramref">html</code> content in a WYSIWYG editor.

```csharp
public static EditorCommand InsertHtml(string html)
```

#### Parameters

`html` [string](https://learn.microsoft.com/dotnet/api/system.string)

the html content to insert.

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">html</code> is null, empty or contain only white
space.

### <a id="DotNetBrowser_Frames_EditorCommand_InsertImage_System_String_"></a> InsertImage\(string\)

Returns a command that allows inserting an image with the given <code class="paramref">source</code> in a WYSIWYG editor.
If the <code class="paramref">source</code> points to an invalid location, then image won't be inserted.

```csharp
public static EditorCommand InsertImage(string source)
```

#### Parameters

`source` [string](https://learn.microsoft.com/dotnet/api/system.string)

the value of the 'src' attribute of the IMG tag

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">source</code> is null, empty or contain only white
space.

### <a id="DotNetBrowser_Frames_EditorCommand_InsertNewLine"></a> InsertNewLine\(\)

Returns a command that allows inserting a new line in a WYSIWYG editor.

```csharp
public static EditorCommand InsertNewLine()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_InsertParagraph"></a> InsertParagraph\(\)

Inserts new paragraph in a WYSIWYG editor.

```csharp
public static EditorCommand InsertParagraph()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_InsertTab"></a> InsertTab\(\)

Returns a command that allows inserting a tab character in a WYSIWYG editor.

```csharp
public static EditorCommand InsertTab()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_InsertText_System_String_"></a> InsertText\(string\)

Returns a command that allows inserting the given <code class="paramref">text</code> content in a WYSIWYG editor or a text
field.

```csharp
public static EditorCommand InsertText(string text)
```

#### Parameters

`text` [string](https://learn.microsoft.com/dotnet/api/system.string)

the text to insert.

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Thrown when the <code class="paramref">text</code> is null, empty or contain only white
space.

### <a id="DotNetBrowser_Frames_EditorCommand_Italic"></a> Italic\(\)

Returns a command that allows making the selected text italic in a WYSIWYG editor.

```csharp
public static EditorCommand Italic()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MovePageDown"></a> MovePageDown\(\)

Returns a command that allows moving the caret position at one page down in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MovePageDown()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MovePageUp"></a> MovePageUp\(\)

Returns a command that allows moving the caret position at one page up in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MovePageUp()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MoveToBeginningOfLine"></a> MoveToBeginningOfLine\(\)

Returns a command that allows moving a word to the beginning of line in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveToBeginningOfLine()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MoveToBeginningOfLineAndModifySelection"></a> MoveToBeginningOfLineAndModifySelection\(\)

Returns a command that allows moving a word to the beginning of line and modifying selection
in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveToBeginningOfLineAndModifySelection()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MoveToEndOfLine"></a> MoveToEndOfLine\(\)

Returns a command that allows moving a word to the end of line in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveToEndOfLine()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MoveToEndOfLineAndModifySelection"></a> MoveToEndOfLineAndModifySelection\(\)

Returns a command that allows moving a word to the end of line and modifying selection in a
text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveToEndOfLineAndModifySelection()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MoveWordLeft"></a> MoveWordLeft\(\)

Returns a command that allows moving a word left in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveWordLeft()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MoveWordLeftAndModifySelection"></a> MoveWordLeftAndModifySelection\(\)

Returns a command that allows moving a word left and modifying selection in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveWordLeftAndModifySelection()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MoveWordRight"></a> MoveWordRight\(\)

Returns a command that allows moving a word right in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveWordRight()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_MoveWordRightAndModifySelection"></a> MoveWordRightAndModifySelection\(\)

Returns a command that allows moving a word right and modifying selection in a text area or a WYSIWYG editor.

```csharp
public static EditorCommand MoveWordRightAndModifySelection()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_Paste"></a> Paste\(\)

Returns a command that allows pasting content of the clipboard in a text field, text area or
a WYSIWYG editor.

```csharp
public static EditorCommand Paste()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_Redo"></a> Redo\(\)

Returns a command that allows reversing the last <xref href="DotNetBrowser.Frames.EditorCommand.Undo" data-throw-if-not-resolved="false"></xref> action.

```csharp
public static EditorCommand Redo()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_ScrollLineDown"></a> ScrollLineDown\(\)

Returns a command that allows scrolling one line down.

```csharp
public static EditorCommand ScrollLineDown()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_ScrollLineUp"></a> ScrollLineUp\(\)

Returns a command that allows scrolling one line up.

```csharp
public static EditorCommand ScrollLineUp()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_ScrollPageBackward"></a> ScrollPageBackward\(\)

Returns a command that allows scrolling a page backward.

```csharp
public static EditorCommand ScrollPageBackward()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_ScrollPageForward"></a> ScrollPageForward\(\)

Returns a command that allows scrolling a page forward.

```csharp
public static EditorCommand ScrollPageForward()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_ScrollToBeginningOfDocument"></a> ScrollToBeginningOfDocument\(\)

Returns a command that allows scrolling content to the beginning of the document in the frame.

```csharp
public static EditorCommand ScrollToBeginningOfDocument()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_ScrollToEndOfDocument"></a> ScrollToEndOfDocument\(\)

Returns a command that allows scrolling content to the end of the document in the frame.

```csharp
public static EditorCommand ScrollToEndOfDocument()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_SelectAll"></a> SelectAll\(\)

Returns a command that allows selecting all text in the frame or the currently focused text
field, text area or a WYSIWYG editor.

```csharp
public static EditorCommand SelectAll()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_SelectLine"></a> SelectLine\(\)

Returns a command that allows selecting a line at the caret position in a text area or a
WYSIWYG editor.

```csharp
public static EditorCommand SelectLine()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_SelectParagraph"></a> SelectParagraph\(\)

Returns a command that allows selecting the whole paragraph at the caret position in a text
area or a WYSIWYG editor.

```csharp
public static EditorCommand SelectParagraph()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_SelectSentence"></a> SelectSentence\(\)

Returns a command that allows selecting the whole sentence at the caret position in a text
area or a WYSIWYG editor.

```csharp
public static EditorCommand SelectSentence()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_SelectWord"></a> SelectWord\(\)

Returns a command that allows selecting the word at the caret position in a text field, text
area or a WYSIWYG editor.

```csharp
public static EditorCommand SelectWord()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_ToggleBold"></a> ToggleBold\(\)

Returns a command that allows toggling bold style for the selected text in a WYSIWYG editor.

```csharp
public static EditorCommand ToggleBold()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_ToggleItalic"></a> ToggleItalic\(\)

Returns a command that allows toggling italic style for the selected text in a WYSIWYG editor.

```csharp
public static EditorCommand ToggleItalic()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_ToggleUnderline"></a> ToggleUnderline\(\)

Returns a command that allows toggling underline style for the selected text in a WYSIWYG editor.

```csharp
public static EditorCommand ToggleUnderline()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_Underline"></a> Underline\(\)

Returns a command that allows underlying the selected text in a WYSIWYG editor.

```csharp
public static EditorCommand Underline()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_Undo"></a> Undo\(\)

Returns a command that allows reversing the last action.

```csharp
public static EditorCommand Undo()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Frames_EditorCommand_Unselect"></a> Unselect\(\)

Returns a command that allows clearing the current selection in a frame.

```csharp
public static EditorCommand Unselect()
```

#### Returns

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

The <xref href="DotNetBrowser.Frames.EditorCommand" data-throw-if-not-resolved="false"></xref> instance.

