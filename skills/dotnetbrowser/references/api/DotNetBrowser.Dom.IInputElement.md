# <a id="DotNetBrowser_Dom_IInputElement"></a> Interface IInputElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents the DOM element with <code>&lt;input&gt;</code> tag.

```csharp
public interface IInputElement : IFormControlElement, IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[IFormControlElement](DotNetBrowser.Dom.IFormControlElement.md), 
[IElement](DotNetBrowser.Dom.IElement.md), 
[INode](DotNetBrowser.Dom.INode.md), 
[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_IInputElement_Checked"></a> Checked

Gets or sets the checked attribute of the input DOM element with the type
<code>'checkbox'</code> or <code>'radio'</code>.

```csharp
bool Checked { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IInputElement_File"></a> File

Gets or sets an absolute or relative path to a file if the current input DOM element
has the type attribute with the 'file' value.

```csharp
string File { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty, or contains only blank characters.

### <a id="DotNetBrowser_Dom_IInputElement_Files"></a> Files

Gets or sets the collection of absolute or relative paths to files if the current input DOM element
has the type attribute with the 'file' value.

```csharp
IEnumerable<string> Files { get; set; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null, empty, or contains only blank characters.

### <a id="DotNetBrowser_Dom_IInputElement_IsCheckBox"></a> IsCheckBox

Indicates whether the DOM element's type attribute has the 'checkbox' value.

```csharp
bool IsCheckBox { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IInputElement_IsEmailField"></a> IsEmailField

Indicates whether the DOM element's type attribute has the 'email' value.

```csharp
bool IsEmailField { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IInputElement_IsFile"></a> IsFile

Indicates whether the DOM element's type attribute has the 'file' value.

```csharp
bool IsFile { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IInputElement_IsMultipleFile"></a> IsMultipleFile

Indicates whether the DOM element has both the type attribute with the
'file' value, and the  multiple attribute, for example: <code>&lt;input type="file" multiple&gt;</code>

```csharp
bool IsMultipleFile { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IInputElement_IsPasswordField"></a> IsPasswordField

Indicates whether the DOM element's type attribute has the 'password' value.

```csharp
bool IsPasswordField { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IInputElement_IsRadioButton"></a> IsRadioButton

Indicates whether the DOM element's type attribute has the 'radio' value.

```csharp
bool IsRadioButton { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IInputElement_IsText"></a> IsText

Indicates if this input element is a text field and
the type attribute value of the input HTML element is 'number'.

```csharp
bool IsText { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IInputElement_IsTextField"></a> IsTextField

Indicates if the DOM element's type attribute has the <code>'text'</code> value.

```csharp
bool IsTextField { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IInputElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

