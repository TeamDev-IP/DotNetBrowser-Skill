# <a id="DotNetBrowser_Dom_ISearchContext"></a> Interface ISearchContext

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

The base interface for search that is implemented by the DOM objects that provide
search mechanisms.

```csharp
public interface ISearchContext : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Methods

### <a id="DotNetBrowser_Dom_ISearchContext_GetElementByClassName_System_String_"></a> GetElementByClassName\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given
<code class="paramref">className</code>.

```csharp
IElement GetElementByClassName(string className)
```

#### Parameters

`className` [string](https://learn.microsoft.com/dotnet/api/system.string)

The class attribute of the HTML element.

#### Returns

 [IElement](DotNetBrowser.Dom.IElement.md)

The first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given <code class="paramref">className</code> or <code>null</code> if no elements were found.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">className</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_ISearchContext_GetElementByCssSelector_System_String_"></a> GetElementByCssSelector\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given CSS selector.

```csharp
IElement GetElementByCssSelector(string cssSelector)
```

#### Parameters

`cssSelector` [string](https://learn.microsoft.com/dotnet/api/system.string)

The CSS selector.

#### Returns

 [IElement](DotNetBrowser.Dom.IElement.md)

The first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given CSS selector or <code>null</code> if no elements were found.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">cssSelector</code> is null, empty or contains only blank
characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_ISearchContext_GetElementById_System_String_"></a> GetElementById\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given <code class="paramref">id</code>.

```csharp
IElement GetElementById(string id)
```

#### Parameters

`id` [string](https://learn.microsoft.com/dotnet/api/system.string)

a string that represents the id attribute of the HTML element.

#### Returns

 [IElement](DotNetBrowser.Dom.IElement.md)

The first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given <code class="paramref">id</code> or <code>null</code> if no elements were found.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">id</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_ISearchContext_GetElementByName_System_String_"></a> GetElementByName\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given <code class="paramref">name</code>.

```csharp
IElement GetElementByName(string name)
```

#### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The <code>name</code> attribute of the HTML element.

#### Returns

 [IElement](DotNetBrowser.Dom.IElement.md)

The first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given <code class="paramref">name</code> or  <code>null</code> if no elements were found.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">name</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_ISearchContext_GetElementByTagName_System_String_"></a> GetElementByTagName\(string\)

Finds the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object in the current search context by the given tag name.

```csharp
IElement GetElementByTagName(string tagName)
```

#### Parameters

`tagName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The tag name of the HTML element.

#### Returns

 [IElement](DotNetBrowser.Dom.IElement.md)

the first <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> object found in the current search context
by the given tag name or <code>null</code> if no elements were found.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">tagName</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_ISearchContext_GetElementsByClassName_System_String_"></a> GetElementsByClassName\(string\)

Finds all <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects in the current search context by the given <code class="paramref">className</code>.

```csharp
IEnumerable<IElement> GetElementsByClassName(string className)
```

#### Parameters

`className` [string](https://learn.microsoft.com/dotnet/api/system.string)

The <code>class</code> attribute of the HTML element.

#### Returns

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IElement](DotNetBrowser.Dom.IElement.md)\>

A collection of the <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects found in the current search context
by the given <code class="paramref">className</code> or an empty collection if no elements were found.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">className</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_ISearchContext_GetElementsByCssSelector_System_String_"></a> GetElementsByCssSelector\(string\)

Finds all <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects in the current search context by the given
<code class="paramref">cssSelector</code>.

```csharp
IEnumerable<IElement> GetElementsByCssSelector(string cssSelector)
```

#### Parameters

`cssSelector` [string](https://learn.microsoft.com/dotnet/api/system.string)

The CSS selector.

#### Returns

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IElement](DotNetBrowser.Dom.IElement.md)\>

A collection of the <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects found in the current search context
by the given <code class="paramref">cssSelector</code> or an empty collection if no elements were found.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">cssSelector</code> is null, empty or contains only blank
characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_ISearchContext_GetElementsByName_System_String_"></a> GetElementsByName\(string\)

Finds all <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects in the current search context by the given <code>name</code>.

```csharp
IEnumerable<IElement> GetElementsByName(string name)
```

#### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The <code>name</code> attribute of the HTML element.

#### Returns

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IElement](DotNetBrowser.Dom.IElement.md)\>

a collection of the <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects found in the current search context
by the given <code>name</code> or an empty collection if no elements were found.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">name</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Dom_ISearchContext_GetElementsByTagName_System_String_"></a> GetElementsByTagName\(string\)

Finds all <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects in the current search context by the given tag name.

```csharp
IEnumerable<IElement> GetElementsByTagName(string tagName)
```

#### Parameters

`tagName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The tag name of the HTML element.

#### Returns

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IElement](DotNetBrowser.Dom.IElement.md)\>

The collection of the <xref href="DotNetBrowser.Dom.IElement" data-throw-if-not-resolved="false"></xref> objects found in the current search context
by the given tag name or an empty collection if no elements were found.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">tagName</code> is null, empty or contains only blank characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Dom.ISearchContext" data-throw-if-not-resolved="false"></xref> has already been disposed.

