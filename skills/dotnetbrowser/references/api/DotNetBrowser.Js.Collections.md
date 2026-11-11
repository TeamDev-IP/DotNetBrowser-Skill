# <a id="DotNetBrowser_Js_Collections"></a> Namespace DotNetBrowser.Js.Collections

### Interfaces

 [IJsArray](DotNetBrowser.Js.Collections.md#DotNetBrowser_Js_Collections_IJsArray)

A JavaScript array.

 [IJsArrayBuffer](DotNetBrowser.Js.Collections.md#DotNetBrowser_Js_Collections_IJsArrayBuffer)

A JavaScript array buffer.

 [IJsMap](DotNetBrowser.Js.Collections.md#DotNetBrowser_Js_Collections_IJsMap)

A JavaScript map.

 [IJsSet](DotNetBrowser.Js.Collections.md#DotNetBrowser_Js_Collections_IJsSet)

A JavaScript set.

## <a id="DotNetBrowser_Js_Collections_IJsArray"></a> Interface IJsArray

Namespace: [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)  
Assembly: DotNetBrowser.dll  

A JavaScript array.

```csharp
public interface IJsArray : IJsObject, IAutoDisposable
```

##### Implements

[IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions_ToJsonString_DotNetBrowser_Js_IJsObject_)

### Remarks

An array object can be passed between .NET and JavaScript as a method argument
or a return value.The object lifetime is bound to the lifetime of the frame this
object belongs to. When the owner frame is unloaded, all the bound JavaScript objects are
automatically disposed.

### Properties

#### <a id="DotNetBrowser_Js_Collections_IJsArray_Count"></a> Count

Gets the number of elements contained in the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref>.

```csharp
ulong Count { get; }
```

##### Property Value

 [ulong](https://learn.microsoft.com/dotnet/api/system.uint64)

##### Remarks

The maximum size of an array in JavaScript equals to 2^32-1

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsArray_Item_System_UInt32_"></a> this\[uint\]

Gets or sets the array element at the specified <code class="paramref">index</code>.
If there is an existing element at the specified <code class="paramref">index</code>, it will be replaced.
If the <code class="paramref">index</code> exceeds the array size, the array will be extended and the elements
between the last inserted item and the <code class="paramref">index</code> will be set to <code>null</code>.

```csharp
object this[uint index] { get; set; }
```

##### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Remarks

If you pass a non-primitive .NET object to JavaScript, it will be converted into a
"proxy" JavaScript object. Method and property calls to this object will be
delegated to the .NET object.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Js_Collections_IJsArray_ToReadOnlyList"></a> ToReadOnlyList\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyList%601" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyList<object> ToReadOnlyList()
```

##### Returns

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

A <xref href="System.Collections.Generic.IReadOnlyList%601" data-throw-if-not-resolved="false"></xref> that contains elements from the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref>.

##### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsArray_ToReadOnlyList__1"></a> ToReadOnlyList<T\>\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyList%601" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyList<T> ToReadOnlyList<T>()
```

##### Returns

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<T\>

A <xref href="System.Collections.Generic.IReadOnlyList%601" data-throw-if-not-resolved="false"></xref> that contains elements from the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref>.

##### Type Parameters

`T` 

##### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Js_Collections_IJsArrayBuffer"></a> Interface IJsArrayBuffer

Namespace: [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)  
Assembly: DotNetBrowser.dll  

A JavaScript array buffer.

```csharp
public interface IJsArrayBuffer
```

### Remarks

An array buffer object can be passed between .NET and JavaScript as a method argument
or a return value.The object lifetime is bound to the lifetime of the frame this
object belongs to.When the owner frame is unloaded, all the JavaScript objects are
automatically disposed.

### Properties

#### <a id="DotNetBrowser_Js_Collections_IJsArrayBuffer_Count"></a> Count

Gets the number of elements contained in the <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref>.

```csharp
long Count { get; }
```

##### Property Value

 [long](https://learn.microsoft.com/dotnet/api/system.int64)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Js_Collections_IJsArrayBuffer_ToByteArray"></a> ToByteArray\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> to a new byte array.

```csharp
byte[] ToByteArray()
```

##### Returns

 [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

An array containing copy of the data in <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArrayBuffer" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Js_Collections_IJsMap"></a> Interface IJsMap

Namespace: [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)  
Assembly: DotNetBrowser.dll  

A JavaScript map.

```csharp
public interface IJsMap : IJsObject, IAutoDisposable
```

##### Implements

[IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions_ToJsonString_DotNetBrowser_Js_IJsObject_)

### Remarks

A map object can be passed between .NET and JavaScript as a method argument or a return value.
The object lifetime is bound to the lifetime of the frame this object belongs to.When the owner
frame is unloaded, all the bound JavaScript objects are automatically disposed.

### Properties

#### <a id="DotNetBrowser_Js_Collections_IJsMap_Count"></a> Count

Gets the number of key-value mappings in this <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

```csharp
uint Count { get; }
```

##### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsMap_Item_System_Object_"></a> this\[object\]

Gets or sets the element with the specified <code class="paramref">key</code>.
If this map contains a value associated with the <code class="paramref">key</code>, it will be replaced.

```csharp
object this[object key] { get; set; }
```

##### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Js_Collections_IJsMap_Clear"></a> Clear\(\)

Removes all items from this <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>. Does nothing if the map is empty.

```csharp
void Clear()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsMap_ContainsKey_System_Object_"></a> ContainsKey\(object\)

Determines whether the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> contains an element with
the specified <code class="paramref">key</code>.

```csharp
bool ContainsKey(object key)
```

##### Parameters

`key` [object](https://learn.microsoft.com/dotnet/api/system.object)

The key to locate in the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> contains an element with the key; otherwise, <code>false</code>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsMap_Remove_System_Object_"></a> Remove\(object\)

Removes the element with the specified key from the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

```csharp
bool Remove(object key)
```

##### Parameters

`key` [object](https://learn.microsoft.com/dotnet/api/system.object)

The key of the element to remove.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the element is successfully removed; otherwise, <code>false</code>.
This method also returns <code>false</code> if key was not found in the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsMap_ToReadOnlyDictionary__2"></a> ToReadOnlyDictionary<TKey, TVal\>\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyDictionary<TKey, TVal> ToReadOnlyDictionary<TKey, TVal>()
```

##### Returns

 [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<TKey, TVal\>

A <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref> that contains key-value pairs
from the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

##### Type Parameters

`TKey` 

`TVal` 

##### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The elements in this <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> cannot be converted to the specified type.

#### <a id="DotNetBrowser_Js_Collections_IJsMap_ToReadOnlyDictionary"></a> ToReadOnlyDictionary\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyDictionary<object, object> ToReadOnlyDictionary()
```

##### Returns

 [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

A <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref> that contains key-value pairs
from the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

##### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Js_Collections_IJsSet"></a> Interface IJsSet

Namespace: [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)  
Assembly: DotNetBrowser.dll  

A JavaScript set.

```csharp
public interface IJsSet : IJsObject, IAutoDisposable
```

##### Implements

[IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions_ToJsonString_DotNetBrowser_Js_IJsObject_)

### Remarks

A set object can be passed between .NET and JavaScript as a method argument
or a return value. The object lifetime is bound to the lifetime of the frame this
object belongs to. When the owner frame is unloaded, all the JavaScript objects are
automatically disposed.

### Properties

#### <a id="DotNetBrowser_Js_Collections_IJsSet_Count"></a> Count

Gets the number of elements contained in the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

```csharp
ulong Count { get; }
```

##### Property Value

 [ulong](https://learn.microsoft.com/dotnet/api/system.uint64)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

### Methods

#### <a id="DotNetBrowser_Js_Collections_IJsSet_Add_System_Object_"></a> Add\(object\)

Adds an item to the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

```csharp
void Add(object item)
```

##### Parameters

`item` [object](https://learn.microsoft.com/dotnet/api/system.object)

The item to the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">item</code> is a <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> from a different web page or frame.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsSet_Clear"></a> Clear\(\)

Removes all items from this <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>. Does nothing if the set is empty.

```csharp
void Clear()
```

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsSet_Contains_System_Object_"></a> Contains\(object\)

Determines whether the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> contains a specific value.

```csharp
bool Contains(object item)
```

##### Parameters

`item` [object](https://learn.microsoft.com/dotnet/api/system.object)

The object to locate in the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if item is found in the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>; otherwise, <code>false</code>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsSet_Remove_System_Object_"></a> Remove\(object\)

Removes the specified <code class="paramref">item</code> from this set.

```csharp
bool Remove(object item)
```

##### Parameters

`item` [object](https://learn.microsoft.com/dotnet/api/system.object)

The item to be removed from this set.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if item was successfully removed from the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>; otherwise, <code>false</code>.
This method also returns <code>false</code> if item is not found in the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Js_Collections_IJsSet_ToReadOnlyCollection__1"></a> ToReadOnlyCollection<T\>\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyCollection%601" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyCollection<T> ToReadOnlyCollection<T>()
```

##### Returns

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<T\>

A <xref href="System.Collections.Generic.IReadOnlyCollection%601" data-throw-if-not-resolved="false"></xref> that contains values
from the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

##### Type Parameters

`T` 

##### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The elements in this <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> cannot be converted to the specified type.

#### <a id="DotNetBrowser_Js_Collections_IJsSet_ToReadOnlyCollection"></a> ToReadOnlyCollection\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyCollection%601" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyCollection<object> ToReadOnlyCollection()
```

##### Returns

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

A <xref href="System.Collections.Generic.IReadOnlyCollection%601" data-throw-if-not-resolved="false"></xref> that contains values
from the <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref>.

##### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The elements in this <xref href="DotNetBrowser.Js.Collections.IJsSet" data-throw-if-not-resolved="false"></xref> cannot be converted to the specified type.
