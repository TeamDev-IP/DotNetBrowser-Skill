# <a id="DotNetBrowser_Js_Collections_IJsSet"></a> Interface IJsSet

Namespace: [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)  
Assembly: DotNetBrowser.dll  

A JavaScript set.

```csharp
public interface IJsSet : IJsObject, IAutoDisposable
```

#### Implements

[IJsObject](DotNetBrowser.Js.IJsObject.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.JsonExtensions.md\#DotNetBrowser\_Js\_JsonExtensions\_ToJsonString\_DotNetBrowser\_Js\_IJsObject\_)

## Remarks

A set object can be passed between .NET and JavaScript as a method argument
or a return value. The object lifetime is bound to the lifetime of the frame this
object belongs to. When the owner frame is unloaded, all the JavaScript objects are
automatically disposed.

## Properties

### <a id="DotNetBrowser_Js_Collections_IJsSet_Count"></a> Count

Gets the number of elements contained in the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

```csharp
ulong Count { get; }
```

#### Property Value

 [ulong](https://learn.microsoft.com/dotnet/api/system.uint64)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_Js_Collections_IJsSet_Add_System_Object_"></a> Add\(object\)

Adds an item to the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

```csharp
void Add(object item)
```

#### Parameters

`item` [object](https://learn.microsoft.com/dotnet/api/system.object)

The item to the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">item</code> is a <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> from a different web page or frame.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsSet_Clear"></a> Clear\(\)

Removes all items from this <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>. Does nothing if the set is empty.

```csharp
void Clear()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsSet_Contains_System_Object_"></a> Contains\(object\)

Determines whether the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> contains a specific value.

```csharp
bool Contains(object item)
```

#### Parameters

`item` [object](https://learn.microsoft.com/dotnet/api/system.object)

The object to locate in the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if item is found in the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>; otherwise, <code>false</code>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsSet_Remove_System_Object_"></a> Remove\(object\)

Removes the specified <code class="paramref">item</code> from this set.

```csharp
bool Remove(object item)
```

#### Parameters

`item` [object](https://learn.microsoft.com/dotnet/api/system.object)

The item to be removed from this set.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if item was successfully removed from the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>; otherwise, <code>false</code>.
This method also returns <code>false</code> if item is not found in the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsSet_ToReadOnlyCollection__1"></a> ToReadOnlyCollection<T\>\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyCollection%601" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyCollection<T> ToReadOnlyCollection<T>()
```

#### Returns

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<T\>

A <xref href="System.Collections.Generic.IReadOnlyCollection%601" data-throw-if-not-resolved="false"></xref> that contains values
from the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

#### Type Parameters

`T` 

#### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The elements in this <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> cannot be converted to the specified type.

### <a id="DotNetBrowser_Js_Collections_IJsSet_ToReadOnlyCollection"></a> ToReadOnlyCollection\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyCollection%601" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyCollection<object> ToReadOnlyCollection()
```

#### Returns

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

A <xref href="System.Collections.Generic.IReadOnlyCollection%601" data-throw-if-not-resolved="false"></xref> that contains values
from the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

#### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The elements in this <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> cannot be converted to the specified type.

