# <a id="DotNetBrowser_Js_IJsObjectPropertyCollection"></a> Interface IJsObjectPropertyCollection

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

The JavaScript object properties.

```csharp
public interface IJsObjectPropertyCollection : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Names"></a> Names

Gets a collection containing the names of the properties of this object, including properties
from prototype objects.

```csharp
IEnumerable<string> Names { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### Remarks

The returned enumerable will enumerate the names in the same way as they would be enumerated by a
for-in statement over this object in JavaScript.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_OwnPropertyNames"></a> OwnPropertyNames

Gets the names of the properties of this object, excluding properties from prototype objects.

```csharp
IEnumerable<string> OwnPropertyNames { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_PropertySymbols"></a> PropertySymbols

Gets the <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> instances with properties' names of this object, excluding properties from
prototype objects.

```csharp
IEnumerable<IJsSymbol> PropertySymbols { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IJsSymbol](DotNetBrowser.Js.IJsSymbol.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Item_System_String_"></a> this\[string\]

Gets or sets a property with the specified name in the current JavaScript object.
The <code class="paramref">name</code> parameter represents JavaScript object's property name.

```csharp
object this[string name] { get; set; }
```

#### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">name</code> is null, empty, or contains only blank characters.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is an IJsObject with
a different JavaScript context.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Item_System_UInt32_"></a> this\[uint\]

Gets or sets a property with the specified index in the current JavaScript object.
The <code class="paramref">index</code> parameter represents JavaScript object's property index.

```csharp
object this[uint index] { get; set; }
```

#### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is an IJsObject with
a different JavaScript context.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Item_DotNetBrowser_Js_IJsSymbol_"></a> this\[IJsSymbol\]

Gets or sets a property with the specified name in the current JavaScript object.
The <code class="paramref">name</code> parameter represents a JavaScript Symbol with a name of the object's property.

```csharp
object this[IJsSymbol name] { get; set; }
```

#### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">name</code> is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is an IJsObject with
a different JavaScript context.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

## Methods

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Contains_System_String_"></a> Contains\(string\)

Checks whether the JavaScript object has a property or function with the specified <code class="paramref">name</code>.

```csharp
bool Contains(string name)
```

#### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The name of the property or function.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the object has a property or function with the specified <code class="paramref">name</code>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Contains_System_UInt32_"></a> Contains\(uint\)

Checks whether the JavaScript object has a property with the specified <code class="paramref">index</code>.

```csharp
bool Contains(uint index)
```

#### Parameters

`index` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

The index of the property.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the object has a property with the given <code class="paramref">index</code>.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Contains_DotNetBrowser_Js_IJsSymbol_"></a> Contains\(IJsSymbol\)

Checks whether the JavaScript object has a property or function with a name specified in the
<xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> input parameter.

```csharp
bool Contains(IJsSymbol name)
```

#### Parameters

`name` [IJsSymbol](DotNetBrowser.Js.IJsSymbol.md)

The <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> instance with the property or function name.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the object has a property or function with a name specified in the <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref>
input parameter.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Remove_System_String_"></a> Remove\(string\)

Removes a property with the specified <code class="paramref">name</code> from the JavaScript object.
Once you remove the property, it will not be available in the current JavaScript object anymore.

```csharp
bool Remove(string name)
```

#### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The name of the property or function.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the property was successfully removed.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Remove_System_UInt32_"></a> Remove\(uint\)

Removes a property with the specified <code class="paramref">index</code> in the JavaScript object.
Once you remove the property, it will not be available in the current JavaScript object anymore.

```csharp
bool Remove(uint index)
```

#### Parameters

`index` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

The index of the property or function.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the property was successfully removed.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Remove_DotNetBrowser_Js_IJsSymbol_"></a> Remove\(IJsSymbol\)

Removes a property with a name specified in the input <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> instance from the JavaScript object.
Once you remove the property, it will not be available in the current JavaScript object anymore.

```csharp
bool Remove(IJsSymbol name)
```

#### Parameters

`name` [IJsSymbol](DotNetBrowser.Js.IJsSymbol.md)

The <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> instance with a name of the property or function.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the property was successfully removed.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

