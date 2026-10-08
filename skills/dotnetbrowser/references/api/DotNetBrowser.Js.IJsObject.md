# <a id="DotNetBrowser_Js_IJsObject"></a> Interface IJsObject

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

Represents a JavaScript object. Provides access to the object's properties and functions.
The JavaScript object is alive until its JavaScript execution context exist. Once execution context
is disposed, all JavaScript objects available in the scope of this context will be automatically disposed.
If you try to access already disposed object, you will get an <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>.

```csharp
public interface IJsObject : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.JsonExtensions.md\#DotNetBrowser\_Js\_JsonExtensions\_ToJsonString\_DotNetBrowser\_Js\_IJsObject\_)

## Properties

### <a id="DotNetBrowser_Js_IJsObject_Frame"></a> Frame

Gets the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> instance this JavaScript object is bound to.

```csharp
IFrame Frame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

### <a id="DotNetBrowser_Js_IJsObject_Properties"></a> Properties

Gets the object properties as a live collection.
Modifying this collection will lead to updating the object properties.

```csharp
IJsObjectPropertyCollection Properties { get; }
```

#### Property Value

 [IJsObjectPropertyCollection](DotNetBrowser.Js.IJsObjectPropertyCollection.md)

## Methods

### <a id="DotNetBrowser_Js_IJsObject_Invoke__1_System_String_System_Object___"></a> Invoke<T\>\(string, params object\[\]\)

Executes the function with the given <code class="paramref">methodName</code> and the <code class="paramref">args</code> in the
JavaScript object. This method blocks current thread execution until the function finishes
its execution. If the function raises an exception, then a <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> with an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

```csharp
T Invoke<T>(string methodName, params object[] args)
```

#### Parameters

`methodName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The function name.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

the list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

#### Returns

 T

The result of the JavaScript function execution.

#### Type Parameters

`T` 

The expected type of the result of the JavaScript function execution

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObject_Invoke_System_String_System_Object___"></a> Invoke\(string, params object\[\]\)

Executes the function with the given <code class="paramref">methodName</code> and the <code class="paramref">args</code>  in the
JavaScript object. This method blocks current thread execution until the function finishes
its execution. If the function raises an exception, then <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> with an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

```csharp
object Invoke(string methodName, params object[] args)
```

#### Parameters

`methodName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The function name.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

the list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

#### Returns

 [object](https://learn.microsoft.com/dotnet/api/system.object)

The result of the JavaScript function execution.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObject_InvokeAsync_System_String_System_Object___"></a> InvokeAsync\(string, params object\[\]\)

Asynchronously executes the function with the given <code class="paramref">methodName</code> and the <code class="paramref">args</code>
in the JavaScript object without blocking the current thread.

```csharp
Task<object> InvokeAsync(string methodName, params object[] args)
```

#### Parameters

`methodName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The function name.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The task that can be used to wait for completion and obtain the result of the JavaScript function execution.

#### Remarks

If the function raises an exception, the task will complete with <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> containing an error
message that describes the reason of the exception. Same error message will be printed in JavaScript Console.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsObject_InvokeAsync__1_System_String_System_Object___"></a> InvokeAsync<T\>\(string, params object\[\]\)

Asynchronously executes the function with the given <code class="paramref">methodName</code> and the <code class="paramref">args</code>
in the JavaScript object without blocking the current thread.

```csharp
Task<T> InvokeAsync<T>(string methodName, params object[] args)
```

#### Parameters

`methodName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The function name.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<T\>

The task that can be used to wait for completion and obtain the result of the JavaScript function execution.

#### Type Parameters

`T` 

The expected type of the result of the JavaScript function execution.

#### Remarks

If the function raises an exception, the task will complete with <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> containing an error
message that describes the reason of the exception. Same error message will be printed in JavaScript Console.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

