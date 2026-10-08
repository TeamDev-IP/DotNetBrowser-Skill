# <a id="DotNetBrowser_Js_IJsFunction"></a> Interface IJsFunction

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

#### Implements

[IJsObject](DotNetBrowser.Js.IJsObject.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.JsonExtensions.md\#DotNetBrowser\_Js\_JsonExtensions\_ToJsonString\_DotNetBrowser\_Js\_IJsObject\_)

## Remarks

<p> This API is available since DotNetBrowser 2.1.</p>

## Methods

### <a id="DotNetBrowser_Js_IJsFunction_Invoke__1_DotNetBrowser_Js_IJsObject_System_Object___"></a> Invoke<T\>\(IJsObject, params object\[\]\)

Executes the function on the given <code class="paramref">jsObject</code> with the <code class="paramref">args</code>.
This method blocks current thread execution until the function finishes
its execution. If the function raises an exception, then a <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> with an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

```csharp
T Invoke<T>(IJsObject jsObject, params object[] args)
```

#### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.IJsObject.md)

The JavaScript object to invoke this function on. Pass <code>null</code> to invoke
the function as a global function.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
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

The <xref href="DotNetBrowser.Js.IJsFunction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsFunction_Invoke_DotNetBrowser_Js_IJsObject_System_Object___"></a> Invoke\(IJsObject, params object\[\]\)

Executes the function on the given <code class="paramref">jsObject</code> with the <code class="paramref">args</code>.
This method blocks current thread execution until the function finishes
its execution. If the function raises an exception, then <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> with an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

```csharp
object Invoke(IJsObject jsObject, params object[] args)
```

#### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.IJsObject.md)

The JavaScript object to invoke this function on. Pass <code>null</code> to invoke
the function as a global function.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

#### Returns

 [object](https://learn.microsoft.com/dotnet/api/system.object)

The result of the JavaScript function execution.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsFunction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsFunction_InvokeAsync_DotNetBrowser_Js_IJsObject_System_Object___"></a> InvokeAsync\(IJsObject, params object\[\]\)

Asynchronously executes the function on the given <code class="paramref">jsObject</code> with the <code class="paramref">args</code>
without blocking the current thread.

```csharp
Task<object> InvokeAsync(IJsObject jsObject, params object[] args)
```

#### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.IJsObject.md)

The JavaScript object to invoke this function on. Pass <code>null</code> to invoke
the function as a global function.

`args` [object](https://learn.microsoft.com/dotnet/api/system.object)\[\]

The list of input arguments. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The task that can be used to wait for completion and obtain the result of the JavaScript function execution.

#### Remarks

If the function raises an exception, the task will complete with <xref href="DotNetBrowser.Js.JsException" data-throw-if-not-resolved="false"></xref> containing an error
message that describes the reason of the exception will be thrown. Same error message will be
printed in JavaScript Console.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsFunction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsFunction_InvokeAsync__1_DotNetBrowser_Js_IJsObject_System_Object___"></a> InvokeAsync<T\>\(IJsObject, params object\[\]\)

Asynchronously executes the function on the given <code class="paramref">jsObject</code> with the <code class="paramref">args</code>
without blocking the current thread.

```csharp
Task<T> InvokeAsync<T>(IJsObject jsObject, params object[] args)
```

#### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.IJsObject.md)

The JavaScript object to invoke this function on. Pass <code>null</code> to invoke
the function as a global function.

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
message that describes the reason of the exception. Same error message will be  printed in JavaScript Console.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsFunction" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

