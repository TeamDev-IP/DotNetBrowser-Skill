# <a id="DotNetBrowser_Js"></a> Namespace DotNetBrowser.Js

### Namespaces

 [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)

### Classes

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

Thrown when an exception is raised in JavaScript.

 [JsonExtensions](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions)

Contains methods for working with JSON strings

 [PropertyUpdateException](DotNetBrowser.Js.md#DotNetBrowser_Js_PropertyUpdateException)

Thrown when a property update fails.

### Interfaces

 [IJsFunction](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsFunction)

A JavaScript function that can be passed between .NET and JavaScript as a method
argument or a return value. The function lifetime is bound to the lifetime of the frame this
function belongs to. When the owner frame is unloaded, all the JavaScript objects are
automatically disposed. An attempt to access a disposed JavaScript object will result
in <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>

 [IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject)

Represents a JavaScript object. Provides access to the object's properties and functions.
The JavaScript object is alive until its JavaScript execution context exist. Once execution context
is disposed, all JavaScript objects available in the scope of this context will be automatically disposed.
If you try to access already disposed object, you will get an <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>.

 [IJsObjectPropertyCollection](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObjectPropertyCollection)

The JavaScript object properties.

 [IJsPromise](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsPromise)

The JavaScript Promise.

 [IJsSymbol](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsSymbol)

Represent a JavaScript "Symbol".
<remarks>
    JavaScript symbols are unique and immutable primitive values that may be used as the key of an object property.
    Symbols are often used to add unique property keys to an object that won't collide with keys any other code
    might add to the object, and which are hidden from any mechanisms other code might use to access the object.
</remarks>

## <a id="DotNetBrowser_Js_JsException"></a> Class JsException

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

Thrown when an exception is raised in JavaScript.

```csharp
public sealed class JsException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

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
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Js_JsonExtensions"></a> Class JsonExtensions

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

Contains methods for working with JSON strings

```csharp
public static class JsonExtensions
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[JsonExtensions](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Js_JsonExtensions_ParseJsonString__1_DotNetBrowser_Frames_IFrame_System_String_"></a> ParseJsonString<T\>\(IFrame, string\)

Creates an object that represents the result of parsing the given string in JSON format.

```csharp
public static T ParseJsonString<T>(this IFrame frame, string jsonString)
```

##### Parameters

`frame` [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

The frame to use for conversion.

`jsonString` [string](https://learn.microsoft.com/dotnet/api/system.string)

A string in JSON format.

##### Returns

 T

The result of parsing. Can be <code>null</code> if the result of parsing is <code>null</code>.
For example, when the given JSON string is "null", then the method returns <code>null</code>

##### Type Parameters

`T` 

The expected result type. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The given JSON string object cannot be parsed.

#### <a id="DotNetBrowser_Js_JsonExtensions_ParseJsonString_DotNetBrowser_Frames_IFrame_System_String_"></a> ParseJsonString\(IFrame, string\)

Creates an object that represents the result of parsing the given string in JSON format.

```csharp
public static object ParseJsonString(this IFrame frame, string jsonString)
```

##### Parameters

`frame` [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

The frame to use for conversion.

`jsonString` [string](https://learn.microsoft.com/dotnet/api/system.string)

A string in JSON format.

##### Returns

 [object](https://learn.microsoft.com/dotnet/api/system.object)

The result of parsing. Can be <code>null</code> if the result of parsing is <code>null</code>.
For example, when the given JSON string is "null", then the method returns <code>null</code>

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The given JSON string object cannot be parsed.

#### <a id="DotNetBrowser_Js_JsonExtensions_ToJsonString_DotNetBrowser_Js_IJsObject_"></a> ToJsonString\(IJsObject\)

Converts the given JavaScript object into a JSON string.

```csharp
public static string ToJsonString(this IJsObject jsObject)
```

##### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject)

The JavaScript object to convert.

##### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

A JSON representation of the given JavaScript object.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The given JavaScript object cannot be converted to a JSON string.
For example, a circular reference was found in the given JavaScript object.

## <a id="DotNetBrowser_Js_PropertyUpdateException"></a> Class PropertyUpdateException

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.Core.dll  

Thrown when a property update fails.

```csharp
public class PropertyUpdateException : Exception, ISerializable
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[PropertyUpdateException](DotNetBrowser.Js.md#DotNetBrowser_Js_PropertyUpdateException)

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

## <a id="DotNetBrowser_Js_IJsFunction"></a> Interface IJsFunction

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

A JavaScript function that can be passed between .NET and JavaScript as a method
argument or a return value. The function lifetime is bound to the lifetime of the frame this
function belongs to. When the owner frame is unloaded, all the JavaScript objects are
automatically disposed. An attempt to access a disposed JavaScript object will result
in <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>

```csharp
public interface IJsFunction : IJsObject, IAutoDisposable
```

##### Implements

[IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions_ToJsonString_DotNetBrowser_Js_IJsObject_)

### Remarks

<p> This API is available since DotNetBrowser 2.1.</p>

### Methods

#### <a id="DotNetBrowser_Js_IJsFunction_Invoke__1_DotNetBrowser_Js_IJsObject_System_Object___"></a> Invoke<T\>\(IJsObject, params object\[\]\)

Executes the function on the given <code class="paramref">jsObject</code> with the <code class="paramref">args</code>.
This method blocks current thread execution until the function finishes
its execution. If the function raises an exception, then a <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> with an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

```csharp
T Invoke<T>(IJsObject jsObject, params object[] args)
```

##### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject)

The JavaScript object to invoke this function on. Pass <code>null</code> to invoke
the function as a global function.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

##### Returns

 T

The result of the JavaScript function execution.

##### Type Parameters

`T` 

The expected type of the result of the JavaScript function execution

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsFunction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsFunction_Invoke_DotNetBrowser_Js_IJsObject_System_Object___"></a> Invoke\(IJsObject, params object\[\]\)

Executes the function on the given <code class="paramref">jsObject</code> with the <code class="paramref">args</code>.
This method blocks current thread execution until the function finishes
its execution. If the function raises an exception, then <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> with an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

```csharp
object Invoke(IJsObject jsObject, params object[] args)
```

##### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject)

The JavaScript object to invoke this function on. Pass <code>null</code> to invoke
the function as a global function.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

##### Returns

 [object](https://learn.microsoft.com/dotnet/api/system.object)

The result of the JavaScript function execution.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsFunction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsFunction_InvokeAsync_DotNetBrowser_Js_IJsObject_System_Object___"></a> InvokeAsync\(IJsObject, params object\[\]\)

Asynchronously executes the function on the given <code class="paramref">jsObject</code> with the <code class="paramref">args</code>
without blocking the current thread.

```csharp
Task<object> InvokeAsync(IJsObject jsObject, params object[] args)
```

##### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject)

The JavaScript object to invoke this function on. Pass <code>null</code> to invoke
the function as a global function.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The task that can be used to wait for completion and obtain the result of the JavaScript function execution.

##### Remarks

If the function raises an exception, the task will complete with <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> containing an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsFunction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsFunction_InvokeAsync__1_DotNetBrowser_Js_IJsObject_System_Object___"></a> InvokeAsync<T\>\(IJsObject, params object\[\]\)

Asynchronously executes the function on the given <code class="paramref">jsObject</code> with the <code class="paramref">args</code>
without blocking the current thread.

```csharp
Task<T> InvokeAsync<T>(IJsObject jsObject, params object[] args)
```

##### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject)

The JavaScript object to invoke this function on. Pass <code>null</code> to invoke
the function as a global function.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<T\>

The task that can be used to wait for completion and obtain the result of the JavaScript function execution.

##### Type Parameters

`T` 

The expected type of the result of the JavaScript function execution.

##### Remarks

If the function raises an exception, the task will complete with <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> containing an error
message that describes the reason of the exception. Same error message will be  printed in JavaScript Console.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsFunction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

## <a id="DotNetBrowser_Js_IJsObject"></a> Interface IJsObject

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

Represents a JavaScript object. Provides access to the object's properties and functions.
The JavaScript object is alive until its JavaScript execution context exist. Once execution context
is disposed, all JavaScript objects available in the scope of this context will be automatically disposed.
If you try to access already disposed object, you will get an <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>.

```csharp
public interface IJsObject : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions_ToJsonString_DotNetBrowser_Js_IJsObject_)

### Properties

#### <a id="DotNetBrowser_Js_IJsObject_Frame"></a> Frame

Gets the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> instance this JavaScript object is bound to.

```csharp
IFrame Frame { get; }
```

##### Property Value

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

#### <a id="DotNetBrowser_Js_IJsObject_Properties"></a> Properties

Gets the object properties as a live collection.
Modifying this collection will lead to updating the object properties.

```csharp
IJsObjectPropertyCollection Properties { get; }
```

##### Property Value

 [IJsObjectPropertyCollection](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObjectPropertyCollection)

### Methods

#### <a id="DotNetBrowser_Js_IJsObject_Invoke__1_System_String_System_Object___"></a> Invoke<T\>\(string, params object\[\]\)

Executes the function with the given <code class="paramref">methodName</code> and the <code class="paramref">args</code> in the
JavaScript object. This method blocks current thread execution until the function finishes
its execution. If the function raises an exception, then a <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> with an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

```csharp
T Invoke<T>(string methodName, params object[] args)
```

##### Parameters

`methodName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The function name.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

the list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

##### Returns

 T

The result of the JavaScript function execution.

##### Type Parameters

`T` 

The expected type of the result of the JavaScript function execution

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObject_Invoke_System_String_System_Object___"></a> Invoke\(string, params object\[\]\)

Executes the function with the given <code class="paramref">methodName</code> and the <code class="paramref">args</code>  in the
JavaScript object. This method blocks current thread execution until the function finishes
its execution. If the function raises an exception, then <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> with an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

```csharp
object Invoke(string methodName, params object[] args)
```

##### Parameters

`methodName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The function name.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

the list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

##### Returns

 [object](https://learn.microsoft.com/dotnet/api/system.object)

The result of the JavaScript function execution.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObject_InvokeAsync_System_String_System_Object___"></a> InvokeAsync\(string, params object\[\]\)

Asynchronously executes the function with the given <code class="paramref">methodName</code> and the <code class="paramref">args</code>
in the JavaScript object without blocking the current thread.

```csharp
Task<object> InvokeAsync(string methodName, params object[] args)
```

##### Parameters

`methodName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The function name.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The task that can be used to wait for completion and obtain the result of the JavaScript function execution.

##### Remarks

If the function raises an exception, the task will complete with <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> containing an error
message that describes the reason of the exception. Same error message will be printed in JavaScript Console.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObject_InvokeAsync__1_System_String_System_Object___"></a> InvokeAsync<T\>\(string, params object\[\]\)

Asynchronously executes the function with the given <code class="paramref">methodName</code> and the <code class="paramref">args</code>
in the JavaScript object without blocking the current thread.

```csharp
Task<T> InvokeAsync<T>(string methodName, params object[] args)
```

##### Parameters

`methodName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The function name.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

##### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<T\>

The task that can be used to wait for completion and obtain the result of the JavaScript function execution.

##### Type Parameters

`T` 

The expected type of the result of the JavaScript function execution.

##### Remarks

If the function raises an exception, the task will complete with <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> containing an error
message that describes the reason of the exception. Same error message will be printed in JavaScript Console.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

## <a id="DotNetBrowser_Js_IJsObjectPropertyCollection"></a> Interface IJsObjectPropertyCollection

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

The JavaScript object properties.

```csharp
public interface IJsObjectPropertyCollection : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Names"></a> Names

Gets a collection containing the names of the properties of this object, including properties
from prototype objects.

```csharp
IEnumerable<string> Names { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

##### Remarks

The returned enumerable will enumerate the names in the same way as they would be enumerated by a
for-in statement over this object in JavaScript.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_OwnPropertyNames"></a> OwnPropertyNames

Gets the names of the properties of this object, excluding properties from prototype objects.

```csharp
IEnumerable<string> OwnPropertyNames { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_PropertySymbols"></a> PropertySymbols

Gets the <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> instances with properties' names of this object, excluding properties from
prototype objects.

```csharp
IEnumerable<IJsSymbol> PropertySymbols { get; }
```

##### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IJsSymbol](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsSymbol)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Item_System_String_"></a> this\[string\]

Gets or sets a property with the specified name in the current JavaScript object.
The <code class="paramref">name</code> parameter represents JavaScript object's property name.

```csharp
object this[string name] { get; set; }
```

##### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">name</code> is null, empty, or contains only blank characters.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is an IJsObject with
a different JavaScript context.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Item_System_UInt32_"></a> this\[uint\]

Gets or sets a property with the specified index in the current JavaScript object.
The <code class="paramref">index</code> parameter represents JavaScript object's property index.

```csharp
object this[uint index] { get; set; }
```

##### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is an IJsObject with
a different JavaScript context.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Item_DotNetBrowser_Js_IJsSymbol_"></a> this\[IJsSymbol\]

Gets or sets a property with the specified name in the current JavaScript object.
The <code class="paramref">name</code> parameter represents a JavaScript Symbol with a name of the object's property.

```csharp
object this[IJsSymbol name] { get; set; }
```

##### Property Value

 [object](https://learn.microsoft.com/dotnet/api/system.object)

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">name</code> is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is an IJsObject with
a different JavaScript context.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

### Methods

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Contains_System_String_"></a> Contains\(string\)

Checks whether the JavaScript object has a property or function with the specified <code class="paramref">name</code>.

```csharp
bool Contains(string name)
```

##### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The name of the property or function.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the object has a property or function with the specified <code class="paramref">name</code>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Contains_System_UInt32_"></a> Contains\(uint\)

Checks whether the JavaScript object has a property with the specified <code class="paramref">index</code>.

```csharp
bool Contains(uint index)
```

##### Parameters

`index` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

The index of the property.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the object has a property with the given <code class="paramref">index</code>.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Contains_DotNetBrowser_Js_IJsSymbol_"></a> Contains\(IJsSymbol\)

Checks whether the JavaScript object has a property or function with a name specified in the
<xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> input parameter.

```csharp
bool Contains(IJsSymbol name)
```

##### Parameters

`name` [IJsSymbol](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsSymbol)

The <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> instance with the property or function name.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the object has a property or function with a name specified in the <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref>
input parameter.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Remove_System_String_"></a> Remove\(string\)

Removes a property with the specified <code class="paramref">name</code> from the JavaScript object.
Once you remove the property, it will not be available in the current JavaScript object anymore.

```csharp
bool Remove(string name)
```

##### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The name of the property or function.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the property was successfully removed.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Remove_System_UInt32_"></a> Remove\(uint\)

Removes a property with the specified <code class="paramref">index</code> in the JavaScript object.
Once you remove the property, it will not be available in the current JavaScript object anymore.

```csharp
bool Remove(uint index)
```

##### Parameters

`index` [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

The index of the property or function.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the property was successfully removed.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsObjectPropertyCollection_Remove_DotNetBrowser_Js_IJsSymbol_"></a> Remove\(IJsSymbol\)

Removes a property with a name specified in the input <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> instance from the JavaScript object.
Once you remove the property, it will not be available in the current JavaScript object anymore.

```csharp
bool Remove(IJsSymbol name)
```

##### Parameters

`name` [IJsSymbol](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsSymbol)

The <xref href="DotNetBrowser.Js.IJsSymbol" data-throw-if-not-resolved="false"></xref> instance with a name of the property or function.

##### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the property was successfully removed.

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

## <a id="DotNetBrowser_Js_IJsPromise"></a> Interface IJsPromise

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

The JavaScript Promise.

```csharp
public interface IJsPromise : IJsObject, IAutoDisposable
```

##### Implements

[IJsObject](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsObject), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

##### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.md#DotNetBrowser_Js_JsonExtensions_ToJsonString_DotNetBrowser_Js_IJsObject_)

### Remarks

<p>The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> interface can be used to register .NET delegates as Promise handlers.</p>

### Methods

#### <a id="DotNetBrowser_Js_IJsPromise_Catch_System_Action_System_Object__"></a> Catch\(Action<object\>\)

Appends the rejection handler to the promise.

```csharp
IJsPromise Catch(Action<object> onRejected)
```

##### Parameters

`onRejected` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

##### Returns

 [IJsPromise](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsPromise)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsPromise_Catch_System_Func_System_Object_System_Object__"></a> Catch\(Func<object, object\>\)

Appends the rejection handler to the promise.

```csharp
IJsPromise Catch(Func<object, object> onRejected)
```

##### Parameters

`onRejected` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

##### Returns

 [IJsPromise](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsPromise)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsPromise_Finally_System_Action_System_Object__"></a> Finally\(Action<object\>\)

Appends the handler that will be invoked if the promise is settled (fulfilled/rejected).

```csharp
IJsPromise Finally(Action<object> onFinally)
```

##### Parameters

`onFinally` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

##### Returns

 [IJsPromise](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsPromise)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref>resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsPromise_Finally_System_Func_System_Object_System_Object__"></a> Finally\(Func<object, object\>\)

Appends the handler that will be invoked if the promise is settled (fulfilled/rejected).

```csharp
IJsPromise Finally(Func<object, object> onFinally)
```

##### Parameters

`onFinally` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

##### Returns

 [IJsPromise](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsPromise)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsPromise_Then_System_Action_System_Object__System_Action_System_Object__"></a> Then\(Action<object\>, Action<object\>\)

Appends fulfillment and rejection handlers to the promise.

```csharp
IJsPromise Then(Action<object> onFulfilled, Action<object> onRejected = null)
```

##### Parameters

`onFulfilled` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The fulfillment handler.

`onRejected` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

##### Returns

 [IJsPromise](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsPromise)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Js_IJsPromise_Then_System_Func_System_Object_System_Object__System_Func_System_Object_System_Object__"></a> Then\(Func<object, object\>, Func<object, object\>\)

Appends fulfillment and rejection handlers to the promise.

```csharp
IJsPromise Then(Func<object, object> onFulfilled, Func<object, object> onRejected = null)
```

##### Parameters

`onFulfilled` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

The fulfillment handler.

`onRejected` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

##### Returns

 [IJsPromise](DotNetBrowser.Js.md#DotNetBrowser_Js_IJsPromise)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

##### Exceptions

 [JsException](DotNetBrowser.Js.md#DotNetBrowser_Js_JsException)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

## <a id="DotNetBrowser_Js_IJsSymbol"></a> Interface IJsSymbol

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

Represent a JavaScript "Symbol".
<remarks>
    JavaScript symbols are unique and immutable primitive values that may be used as the key of an object property.
    Symbols are often used to add unique property keys to an object that won't collide with keys any other code
    might add to the object, and which are hidden from any mechanisms other code might use to access the object.
</remarks>

```csharp
public interface IJsSymbol : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Js_IJsSymbol_Description"></a> Description

Gets the symbol description.

```csharp
string Description { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)
