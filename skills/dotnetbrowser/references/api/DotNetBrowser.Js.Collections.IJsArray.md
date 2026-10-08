# <a id="DotNetBrowser_Js_Collections_IJsArray"></a> Interface IJsArray

Namespace: [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)  
Assembly: DotNetBrowser.dll  

A JavaScript array.

```csharp
public interface IJsArray : IJsObject, IAutoDisposable
```

#### Implements

[IJsObject](DotNetBrowser.Js.IJsObject.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.JsonExtensions.md\#DotNetBrowser\_Js\_JsonExtensions\_ToJsonString\_DotNetBrowser\_Js\_IJsObject\_)

## Remarks

An array object can be passed between .NET and JavaScript as a method argument
or a return value.The object lifetime is bound to the lifetime of the frame this
object belongs to. When the owner frame is unloaded, all the bound JavaScript objects are
automatically disposed.

## Properties

### <a id="DotNetBrowser_Js_Collections_IJsArray_Count"></a> Count

Gets the number of elements contained in the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref>.

```csharp
ulong Count { get; }
```

#### Property Value

 [ulong](https://learn.microsoft.com/dotnet/api/system.uint64)

#### Remarks

The maximum size of an array in JavaScript equals to 2^32-1

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsArray_Item_System_UInt32_"></a> this\[uint\]

Gets or sets the array element at the specified <code class="paramref">index</code>.
If there is an existing element at the specified <code class="paramref">index</code>, it will be replaced.
If the <code class="paramref">index</code> exceeds the array size, the array will be extended and the elements
between the last inserted item and the <code class="paramref">index</code> will be set to <code>null</code>.

```csharp
object this[uint index] { get; set; }
```

#### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Remarks

If you pass a non-primitive .NET object to JavaScript, it will be converted into a
"proxy" JavaScript object. Method and property calls to this object will be
delegated to the .NET object.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_Js_Collections_IJsArray_ToReadOnlyList"></a> ToReadOnlyList\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyList%601" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyList<object> ToReadOnlyList()
```

#### Returns

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

A <xref href="System.Collections.Generic.IReadOnlyList%601" data-throw-if-not-resolved="false"></xref> that contains elements from the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref>.

#### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Js_Collections_IJsArray_ToReadOnlyList__1"></a> ToReadOnlyList<T\>\(\)

Copies the contents of the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> to a new <xref href="System.Collections.Generic.IReadOnlyList%601" data-throw-if-not-resolved="false"></xref>.

```csharp
IReadOnlyList<T> ToReadOnlyList<T>()
```

#### Returns

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<T\>

A <xref href="System.Collections.Generic.IReadOnlyList%601" data-throw-if-not-resolved="false"></xref> that contains elements from the <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref>.

#### Type Parameters

`T` 

#### Remarks

Proxy objects are mapped to the corresponding injected .NET objects.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.Collections.IJsArray" data-throw-if-not-resolved="false"></xref> has already been disposed.

