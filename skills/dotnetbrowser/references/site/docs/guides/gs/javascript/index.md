
# JavaScript

**Lead**
This guide describes how to access JavaScript on the loaded web page, execute JavaScript code, inject .NET objects to call .NET from JavaScript, and other features.


## Executing JavaScript

DotNetBrowser allows accessing and executing JavaScript code on the loaded web page.

**Note**
To access JavaScript, make sure that the web page is loaded completely and JavaScript is [enabled](https://teamdev.com/dotnetbrowser/docs/guides/gs/content/#javascript).


To execute JavaScript code, use the `IFrame.ExecuteJavaScript(string)` method. This method returns a `Task` that can be used to obtain the execution result.
Getting the `Task.Result` property or calling the `Task.Wait()` method blocks the execution of the current thread until the JavaScript execution is completed.
 
By default, the method returns a `Task<object>` that represents the result of the execution. The result is `null` if JavaScript returns `null` or `undefined`.
The generic overload of this method performs a direct cast. If there is a type mismatch, the returned task fails with `InvalidCastException`. If you need to avoid this, use
the non-generic overload in a combination with the safe cast, namely [`as` operator](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/operators/type-testing-and-cast#the-as-operator). 

Choose the type parameter by the [conversion rules](#javascript-to-net). For
example, `ExecuteJavaScript<int>()` fails for a JavaScript number, because
numbers are converted to `double`. If the result can be `null`, use a reference
type or a nullable value type such as `double?`: casting `null` to `double` or
`bool` fails the task with `NullReferenceException`.

`ExecuteJavaScript()` does not report errors thrown by the script. The
non-generic overload returns `null`. The generic overload returns `null` too,
or, for a value type, fails with `NullReferenceException`. To handle a
JavaScript exception in .NET, get the function as `IJsFunction` and call
`Invoke()` or `InvokeAsync()`. If the function throws, `Invoke()` throws
`JsException`, and the task returned by `InvokeAsync()` fails with
`JsException`, so await the task to catch it. See [Functions](#functions) and
[Working with JavaScript functions](#working-with-javascript-functions).

The sample below executes the JavaScript code that returns a title of the `document`:


**C#**
```csharp
string title = frame.ExecuteJavaScript<string>("document.title").Result;
```

**VB**
```vb
Dim title As String = frame.ExecuteJavaScript(Of String)("document.title").Result
```



You can execute any JavaScript code:


**C#**
```csharp
double number = frame.ExecuteJavaScript<double>("123").Result;
bool boolean = frame.ExecuteJavaScript<bool>("true").Result;
string str = frame.ExecuteJavaScript<string>("'Hello'").Result;
IJsObject window = frame.ExecuteJavaScript<IJsObject>("window").Result;
IElement body = frame.ExecuteJavaScript<IElement>("document.body").Result;
BigInteger bigNumber = frame.ExecuteJavaScript<BigInteger>("9007199254740991n").Result;
IJsSymbol symbol = frame.ExecuteJavaScript<IJsSymbol>("Symbol('bacf2f')").Result;
```

**VB**
```vb
Dim number As Double = frame.ExecuteJavaScript(Of Double)("123").Result
Dim [boolean] As Boolean = frame.ExecuteJavaScript(Of Boolean)("true").Result
Dim str As String = frame.ExecuteJavaScript(Of String)("'Hello'").Result
Dim window As IJsObject = frame.ExecuteJavaScript(Of IJsObject)("window").Result
Dim body As IElement = frame.ExecuteJavaScript(Of IElement)("document.body").Result
Dim bigNumber As BigInteger = frame.ExecuteJavaScript(Of BigInteger)("9007199254740991n").Result
Dim symbol As IJsSymbol = frame.ExecuteJavaScript(Of IJsSymbol)("Symbol('bacf2f')").Result
```



## Injecting JavaScript

You can inject a custom JavaScript code on the web page using the `IBrowser.InjectJsHandler`
property. This handler is intended to inject: 
- a .NET object into JavaScript code; 
- a custom JavaScript code for further execution before any scripts are executed in the particular frame. 

See the code sample below:


**C#**
```csharp
browser.InjectJsHandler = new Handler<InjectJsParameters>(args =>
{
    IJsObject window = args.Frame.ExecuteJavaScript<IJsObject>("window").Result;
    window.Properties["myObject"] = new MyObject();
});
```

**VB**
```vb
browser.InjectJsHandler = New Handler(Of InjectJsParameters)(Sub(args)
    Dim window As IJsObject = args.Frame.ExecuteJavaScript(Of IJsObject)("window").Result
    window.Properties("myObject") = New MyObject()
End Sub)
```



The `MyObject` class may look like this:


**C#**
```csharp
public class MyObject
{
    public string SayHelloTo(string firstName) => "Hello " + firstName + "!";
}
```

**VB**
```vb
Public Class MyObject
    Public Function SayHelloTo(ByVal firstName As String) As String
        Return "Hello " & firstName & "!"
    End Function
End Class
```



When the property is set, you can call methods of the injected .NET object from JavaScript:
```js
window.myObject.SayHelloTo('John');
```
This handler may be invoked several times for the same frame.

**Important**
Avoid executing a JavaScript code that modifies the DOM tree of the web page being loaded. You must not use DotNetBrowser DOM API to remove the frame for which this handler is invoked, otherwise the render process crashes.



## Type conversion

JavaScript and .NET work with different primitive types. DotNetBrowser implements an automatic type conversion from JavaScript to .NET types and vice versa.

### JavaScript to .NET

The following rules are used to convert JavaScript into .NET types:

- Numbers are converted to `System.Double`;
- `string` to `System.String`;
- `boolean` to `System.Boolean`;
- `BigInt` to `System.Numerics.BigInteger`;
- `Symbol` is wrapped as `IJsSymbol`;
- `null` and `undefined` to `null`;
- JavaScript `Promise` is wrapped as `IJsPromise`;
- Objects are wrapped as `IJsObject`;
- DOM nodes get wrapped as both `IJsObject` and `IEventTarget`.

In the code sample above we know that the `document.title` is a string, so we use the generic method overload with the `string` type parameter.

### .NET to JavaScript

The following rules are used to convert .NET into JavaScript types:

- `System.Double` to `Number`;
- `System.String` to `string`;
- `System.Boolean` to `boolean`;
- `null` to `null`;
- `System.Numerics.BigInteger` to `BigInt`;
- `IJsSymbol` to an appropriate JavaScript `Symbol`;
- `IJsPromise` to an appropriate JavaScript `Promise`;
- `IJsObject` to an appropriate JavaScript object;
- `IEventTarget` to an appropriate DOM node object;
- `System.Object` will be wrapped into a JavaScript object.

## DOM wrappers

According to the rules of the automatic type conversion, JavaScript DOM objects get wrapped as both `IJsObject` and `IEventTarget`. You can work with the JavaScript DOM objects using DotNetBrowser DOM API.

In the code sample below, we return the `document` that represents a JavaScript DOM object. In this case, the return value type can be set to `IJsObject` or `IDocument`:


**C#**
```csharp
IDocument document = frame.ExecuteJavaScript<IDocument>("document").Result;
```

**VB**
```vb
Dim document As IDocument = frame.ExecuteJavaScript(Of IDocument)("document").Result
```




**C#**
```csharp
IJsObject document = frame.ExecuteJavaScript<IJsObject>("document").Result;
```

**VB**
```vb
Dim document As IJsObject = frame.ExecuteJavaScript(Of IJsObject)("document").Result
```



## Working with JsObject

To work with JavaScript objects from .NET code, use the `IJsObject` interface. This interface allows working with the object properties and calling its functions.

### Properties

To get property names of a JavaScript object, including properties from the prototype objects, use the `IJsObjectPropertyCollection.Names` property:


**C#**
```csharp
IEnumerable<string> propertyNames = jsObject.Properties.Names;
```

**VB**
```vb
Dim propertyNames As IEnumerable(Of String) = jsObject.Properties.Names
```



To check whether JavaScript object has a specified property, use the `IJsObjectPropertyCollection.Contains(string)` method:


**C#**
```csharp
bool has = jsObject.Properties.Contains("<property-name>");
```

**VB**
```vb
Dim has As Boolean = jsObject.Properties.Contains("<property-name>")
```



To get a value of the JavaScript object property by its name, use `Properties[string]`. See the code sample below:


**C#**
```csharp
IJsObject document = frame.ExecuteJavaScript<IJsObject>("document").Result;
object title = document.Properties["title"];
```

**VB**
```vb
Dim document As IJsObject = frame.ExecuteJavaScript(Of IJsObject)("document").Result
Dim title As Object = document.Properties("title")
```



The `Properties[string]` can also be used to set the properties of the JavaScript object. For example:


**C#**
```csharp
document.Properties["title"] = "New Title";
```

**VB**
```vb
document.Properties("title") = "New Title"
```



The return value is `System.Object` that can be set to the required type. For details, refer to the [Type Conversion](#type-conversion) section.

You can remove a property using the following approach:


**C#**
```csharp
bool success = jsObject.Properties.Remove("<property-name>");
```

**VB**
```vb
Dim success As Boolean = jsObject.Properties.Remove("<property-name>")
```



### Functions

To call a function with the required name and arguments, use the `Invoke(string methodName, object... args)` method. The code sample below demonstrates how to call the `document.getElementById()` JavaScript function:


**C#**
```csharp
IJsObject element = document.Invoke("getElementById", "demo");
```

**VB**
```vb
Dim element As IJsObject = document.Invoke("getElementById", "demo")
```



...which is equivalent to the following code in JavaScript:

```js
var element = document.getElementById("demo");
```

**Note**
The method throws `JsException` if an error occurs during the function execution.


### Dynamic type

You can perform calls to JavaScript objects as shown below:


**C#**
```csharp
dynamic document = Browser.MainFrame.ExecuteJavaScript("document").Result;
document.write("Hello world!");
```

**VB**
```vb
Dim document As Object = Browser.MainFrame.ExecuteJavaScript("document").Result
document.write("Hello world!")
```



Here is a more complex example demonstrating how to work with `XMLHttpRequest` and send AJAX request using the 
<span class="code-tab-content inline" lang="C#">dynamic type:</span>
<span class="code-tab-content inline" lang="VB">late binding:</span>


**C#**
```csharp
dynamic xhr = browser.MainFrame.ExecuteJavaScript("new XMLHttpRequest()").Result;
var url = "https://jsonplaceholder.typicode.com/todos/1";
xhr.open("GET", url, true);

// Execute function on readystatechange.
xhr.onreadystatechange = (Action<dynamic>)((o) =>
{
    if (xhr.readyState == 4 && xhr.status == 200)
    {
        System.Console.WriteLine(xhr.responseText);
    }
});
// Send our request.
xhr.send();

// Wait in the main thread to see the response printed out.
Thread.Sleep(10000);
```

**VB**
```vb
Dim xhr As Object
xhr = browser.MainFrame.ExecuteJavaScript("new XMLHttpRequest()").Result
Dim url = "https://jsonplaceholder.typicode.com/todos/1"
xhr.open("GET", url, true)

' Execute function on readystatechange.
xhr.onreadystatechange = Sub (o As Object)
    If xhr.readyState = 4 And xhr.status = 200
        System.Console.WriteLine(xhr.responseText.ToString())
    End If
End Sub
' Send the request.
xhr.send()

' Wait in the main thread to see the response printed out.
Thread.Sleep(10000)
```



## Working with JavaScript functions

Since DotNetBrowser [2.1](https://teamdev.com/dotnetbrowser/releases/2020/v2-1/), you can work with the JavaScript functions directly from the .NET code and pass the reference to a function from JavaScript to .NET. For example: 


**C#**
```csharp
IJsFunction alert = frame.ExecuteJavaScript<IJsFunction>("window.alert").Result;
alert?.Invoke(window, "Hello world!");
```

**VB**
```vb
Dim alert As IJsFunction = frame.ExecuteJavaScript(Of IJsFunction)("window.alert").Result
alert?.Invoke(window, "Hello world!")
```



## Working with JavaScript Promises

Since DotNetBrowser [2.7](https://teamdev.com/dotnetbrowser/releases/2021/v2-7/) you can work with the JavaScript Promises directly without a need to create a wrapper over `IJsObject`. For example:


**C#**
```csharp
IJsPromise promise = browser.MainFrame
                            .ExecuteJavaScript<IJsPromise>("Promise.resolve(\"test\")")
                            .Result;

// Invoke some .NET code when the promise is fulfilled or rejected.
promise.Then(o => Console.WriteLine("Promise fulfilled"),
             e => Console.WriteLine("Promise rejected"));
```

**VB**
```vb
Dim promise As IJsPromise =
    browser1.MainFrame.ExecuteJavaScript(
        Of IJsPromise)("Promise.resolve(""test"")").Result

' Invoke some .NET code when the promise is fulfilled or rejected.
promise.Then(Sub(o) Console.WriteLine("Promise fulfilled"), 
             Sub(e) Console.WriteLine("Promise rejected"))
```



## Calling .NET from JavaScript

When you pass a `System.Object` as a property value or an argument while calling JavaScript 
function, the .NET object will be automatically converted/wrapped into a JavaScript object. It allows injecting .NET objects into JavaScript and invoking its public methods from the JavaScript code.

The code samples below demonstrates how to pass a .NET object as a property value and call its public method from JavaScript:


**C#**
```csharp
public class MyObject {

    public string SayHelloTo(string firstName) {
        return "Hello " + firstName + "!";
    }
}
```

**VB**
```vb
Public Class MyObject
    Public Function SayHelloTo(ByVal firstName As String) As String
        Return "Hello " & firstName & "!"
    End Function
End Class
```




**C#**
```csharp
IJsObject window = frame.ExecuteJavaScript<IJsObject>("window").Result;
window.Properties["MyObject"] = new MyObject();
```

**VB**
```vb
Dim window As IJsObject = frame.ExecuteJavaScript(Of IJsObject)("window").Result
window.Properties("MyObject") = New MyObject()
```



After that, you can refer to the object and call its method from the JavaScript code:

```js
console.log(window.MyObject.SayHelloTo("John"));
```

The Console output is as follows:

```
Hello John!
```

### Type conversion

The JavaScript-.NET bridge provides automatic types conversion functionality when 
calling a public method of the injected .NET object from JavaScript.

The library automatically convert the given JavaScript `Number` to the required .NET type **if 
it is possible**. If we detect that the given number cannot be converted to, for example, a .NET 
`byte` without data loss, then the library throws an exception and notifies JavaScript that there is 
no appropriate .NET method. If the given value can be converted without data loss, then the library 
converts it and invokes the appropriate .NET method.

For example, if you inject the following .NET object into JavaScript:


**C#**
```csharp
public sealed class MyObject {

    public int Method(int intValue) {
        return intValue;
    }
}
```

**VB**
```vb
Public NotInheritable Class MyObject
    Public Function Method(ByVal intValue As Integer) As Integer
        Return intValue
    End Function
End Class
```




After that, you can call it from JavaScript and pass the JavaScript `Number` value that can be converted to 
an `Integer` without data loss:

```javascript
window.MyObject.method(123);
```

However, if you pass `Double` value that cannot be converted to an `Integer` without data loss, you get the following error:

```javascript
window.MyObject.method(3.14); // <- error
```

### Injecting delegates

The other way to call .NET from JavaScript is injecting delegates.

JavaScript-.NET bridge allows you to associate a delegate with a JavaScript property. Such a delegate will be treated as a function that can be invoked in JavaScript code.

For example, you can register a JavaScript function associated with the delegate 
using the following code:


**C#**
```csharp
IJsObject window = frame.ExecuteJavaScript<IJsObject>("window").Result;
if (window != null) {
    window.Properties["sayHello"] = (Func<string, string>) ((args) => "Hello, " + args[0]);
}
```

**VB**
```vb
Dim window As IJsObject = frame.ExecuteJavaScript(Of IJsObject)("window").Result
If window IsNot Nothing Then
    window.Properties("sayHello") = CType(Function(args) "Hello, " & args(0), 
        Func(Of String, String))
End If
```



Now, you can invoke this function in JavaScript the following way:

```javascript
window.sayHello('John');
```
**Important**
The type conversion rules do not apply to the delegates. The JavaScript `Number` is always interpreted as `Double` in this case.


## Console messages

DotNetBrowser allows receiving all output messages sent to the Console using the `console.log()` JavaScript function. You can _listen_ to the messages with the following levels:
- `DEBUG`
- `LOG`
- `WARNING`
- `ERROR`

To get a notification on the Console receives a message, use the `ConsoleMessageReceived` event. See the code sample below:


**C#**
```csharp
browser.ConsoleMessageReceived += (s, e) => {
    string consoleMessage = e.Message;
    ConsoleMessageReceivedEventArgs.MessageLevel level = e.Level;
};
```

**VB**
```vb
AddHandler browser.ConsoleMessageReceived, Sub(s, e)
    Dim consoleMessage As String = e.Message
    Dim level As ConsoleMessageReceivedEventArgs.MessageLevel = e.Level
End Sub
```



## Working with JSON

DotNetBrowser JS - .NET Bridge API allows converting a string that represents JSON to a JavaScript object/objects. The code sample below demonstrates how to create a JavaScript object from the JSON string:


**C#**
```csharp
string jsonString = "[123, \"Hello\"]";
IJsObject jsObject = browser.MainFrame.ParseJsonString<IJsObject>(jsonString);
```

**VB**
```vb
Dim jsonString As String = "[123, ""Hello""]"
Dim jsObject As IJsObject = browser.MainFrame.ParseJsonString(Of IJsObject)(jsonString)
```



**Note**
If you try parsing the string value that doesn't represent a valid JSON, a `JsException` is thrown. 


In the code sample above, the `"[123, \"Hello\"]"` JSON string is converted into an appropriate JavaScript object. In this case, it will be converted to an array. 

It is possible to convert `IJsObject` into a JSON string using the `ToJsonString()` extension method. It returns a string equivalent to JavaScript `JSON.stringify()` method:


**C#**
```csharp
string jsonRepresentation = jsObject.ToJsonString();
```

**VB**
```vb
Dim jsonRepresentation As String = jsObject.ToJsonString()
```


