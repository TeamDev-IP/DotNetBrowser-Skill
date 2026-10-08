# <a id="DotNetBrowser_Js_IJsPromise"></a> Interface IJsPromise

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

The JavaScript Promise.

```csharp
public interface IJsPromise : IJsObject, IAutoDisposable
```

#### Implements

[IJsObject](DotNetBrowser.Js.IJsObject.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

#### Extension Methods

[JsonExtensions.ToJsonString\(IJsObject\)](DotNetBrowser.Js.JsonExtensions.md\#DotNetBrowser\_Js\_JsonExtensions\_ToJsonString\_DotNetBrowser\_Js\_IJsObject\_)

## Remarks

<p>The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> interface can be used to register .NET delegates as Promise handlers.</p>

## Methods

### <a id="DotNetBrowser_Js_IJsPromise_Catch_System_Action_System_Object__"></a> Catch\(Action<object\>\)

Appends the rejection handler to the promise.

```csharp
IJsPromise Catch(Action<object> onRejected)
```

#### Parameters

`onRejected` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

#### Returns

 [IJsPromise](DotNetBrowser.Js.IJsPromise.md)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsPromise_Catch_System_Func_System_Object_System_Object__"></a> Catch\(Func<object, object\>\)

Appends the rejection handler to the promise.

```csharp
IJsPromise Catch(Func<object, object> onRejected)
```

#### Parameters

`onRejected` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

#### Returns

 [IJsPromise](DotNetBrowser.Js.IJsPromise.md)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsPromise_Finally_System_Action_System_Object__"></a> Finally\(Action<object\>\)

Appends the handler that will be invoked if the promise is settled (fulfilled/rejected).

```csharp
IJsPromise Finally(Action<object> onFinally)
```

#### Parameters

`onFinally` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

#### Returns

 [IJsPromise](DotNetBrowser.Js.IJsPromise.md)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref>resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsPromise_Finally_System_Func_System_Object_System_Object__"></a> Finally\(Func<object, object\>\)

Appends the handler that will be invoked if the promise is settled (fulfilled/rejected).

```csharp
IJsPromise Finally(Func<object, object> onFinally)
```

#### Parameters

`onFinally` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

#### Returns

 [IJsPromise](DotNetBrowser.Js.IJsPromise.md)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsPromise_Then_System_Action_System_Object__System_Action_System_Object__"></a> Then\(Action<object\>, Action<object\>\)

Appends fulfillment and rejection handlers to the promise.

```csharp
IJsPromise Then(Action<object> onFulfilled, Action<object> onRejected = null)
```

#### Parameters

`onFulfilled` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The fulfillment handler.

`onRejected` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

#### Returns

 [IJsPromise](DotNetBrowser.Js.IJsPromise.md)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Js_IJsPromise_Then_System_Func_System_Object_System_Object__System_Func_System_Object_System_Object__"></a> Then\(Func<object, object\>, Func<object, object\>\)

Appends fulfillment and rejection handlers to the promise.

```csharp
IJsPromise Then(Func<object, object> onFulfilled, Func<object, object> onRejected = null)
```

#### Parameters

`onFulfilled` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

The fulfillment handler.

`onRejected` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<[object](https://learn.microsoft.com/dotnet/api/system.object), [object](https://learn.microsoft.com/dotnet/api/system.object)\>

The rejection handler.

#### Returns

 [IJsPromise](DotNetBrowser.Js.IJsPromise.md)

A new <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> resolving to the return value of the called handler, or to its original settled
value if the promise was not handled.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The JavaScript function raised an exception.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Js.IJsPromise" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

