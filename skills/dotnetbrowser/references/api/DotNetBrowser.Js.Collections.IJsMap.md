# <a id="DotNetBrowser_Js_Collections_IJsMap"></a> Interface IJsMap

Namespace: [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)  
Assembly: DotNetBrowser.dll  

A JavaScript map.

```csharp
public interface IJsMap : IJsObject, IAutoDisposable
```

#### Implements

[IJsObject](DotNetBrowser.Js.IJsObject.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.JsonExtensions.md\#DotNetBrowser\_Js\_JsonExtensions\_ToJsonString\_DotNetBrowser\_Js\_IJsObject\_)

## Remarks

A map object can be passed between .NET and JavaScript as a method argument or a return value.
The object lifetime is bound to the lifetime of the frame this object belongs to.When the owner
frame is unloaded, all the bound JavaScript objects are automatically disposed.

## Properties

### <a id="DotNetBrowser_Js_Collections_IJsMap_Count"></a> Count

Gets the number of key-value mappings in this <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

```csharp
uint Count { get; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsMap_Item_System_Object_"></a> this\[object\]

Gets or sets the element with the specified <code class="paramref">key</code>.
If this map contains a value associated with the <code class="paramref">key</code>, it will be replaced.

```csharp
object this[object key] { get; set; }
```

#### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_Js_Collections_IJsMap_Clear"></a> Clear\(\)

Removes all items from this <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>. Does nothing if the map is empty.

```csharp
void Clear()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsMap_ContainsKey_System_Object_"></a> ContainsKey\(object\)

Determines whether the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> contains an element with
the specified <code class="paramref">key</code>.

```csharp
bool ContainsKey(object key)
```

#### Parameters

`key` [object](https://learn.microsoft.com/dotnet/api/system.object)

The key to locate in the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> contains an element with the key; otherwise, <code>false</code>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsMap_Remove_System_Object_"></a> Remove\(object\)

Removes the element with the specified key from the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

```csharp
bool Remove(object key)
```

#### Parameters

`key` [object](https://learn.microsoft.com/dotnet/api/system.object)

The key of the element to remove.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the element is successfully removed; otherwise, <code>false</code>.
This method also returns <code>false</code> if key was not found in the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsMap_ToReadOnlyDictionary__2"></a> ToReadOnlyDictionary<TKey, TVal\>\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyDictionary<TKey, TVal> ToReadOnlyDictionary<TKey, TVal>()
```

#### Returns

 [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<TKey, TVal\>

A <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref> that contains key-value pairs
from the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

#### Type Parameters

`TKey` 

`TVal` 

#### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The elements in this <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> cannot be converted to the specified type.

### <a id="DotNetBrowser_Js_Collections_IJsMap_ToReadOnlyDictionary"></a> ToReadOnlyDictionary\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyDictionary<object, object> ToReadOnlyDictionary()
```

#### Returns

 [IReadOnlyDictionary](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlydictionary\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

A <xref href="System.Collections.Generic.IReadOnlyDictionary%602" data-throw-if-not-resolved="false"></xref> that contains key-value pairs
from the <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref>.

#### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsMap" data-throw-if-not-resolved="false"></xref> has already been disposed.

