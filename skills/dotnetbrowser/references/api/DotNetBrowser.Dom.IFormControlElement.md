# <a id="DotNetBrowser_Dom_IFormControlElement"></a> Interface IFormControlElement

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Represents the form control element.

```csharp
public interface IFormControlElement : IElement, INode, IEventTarget, ISearchContext, IAutoDisposable
```

#### Implements

[IElement](DotNetBrowser.Dom.IElement.md), 
[INode](DotNetBrowser.Dom.INode.md), 
[IEventTarget](DotNetBrowser.Dom.Events.IEventTarget.md), 
[ISearchContext](DotNetBrowser.Dom.ISearchContext.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Dom_IFormControlElement_Form"></a> Form

Gets the <code>&lt;form&gt;</code> element containing this control.

```csharp
IFormElement Form { get; }
```

#### Property Value

 [IFormElement](DotNetBrowser.Dom.IFormElement.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormControlElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IFormControlElement_IsEnabled"></a> IsEnabled

Indicates whether form control is enabled or disabled.

```csharp
bool IsEnabled { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormControlElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_IFormControlElement_Value"></a> Value

Gets or sets the form control value.

```csharp
string Value { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.IFormControlElement" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null.

