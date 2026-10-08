# <a id="DotNetBrowser_Js"></a> Namespace DotNetBrowser.Js

### Namespaces

 [DotNetBrowser.Js.Collections](DotNetBrowser.Js.Collections.md)

### Classes

 [JsException](DotNetBrowser.Js.JsException.md)

Thrown when an exception is raised in JavaScript.

 [JsonExtensions](DotNetBrowser.Js.JsonExtensions.md)

Contains methods for working with JSON strings

 [PropertyUpdateException](DotNetBrowser.Js.PropertyUpdateException.md)

Thrown when a property update fails.

### Interfaces

 [IJsFunction](DotNetBrowser.Js.IJsFunction.md)

A JavaScript function that can be passed between .NET and JavaScript as a method
argument or a return value. The function lifetime is bound to the lifetime of the frame this
function belongs to. When the owner frame is unloaded, all the JavaScript objects are
automatically disposed. An attempt to access a disposed JavaScript object will result
in <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>

 [IJsObject](DotNetBrowser.Js.IJsObject.md)

Represents a JavaScript object. Provides access to the object's properties and functions.
The JavaScript object is alive until its JavaScript execution context exist. Once execution context
is disposed, all JavaScript objects available in the scope of this context will be automatically disposed.
If you try to access already disposed object, you will get an <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>.

 [IJsObjectPropertyCollection](DotNetBrowser.Js.IJsObjectPropertyCollection.md)

The JavaScript object properties.

 [IJsPromise](DotNetBrowser.Js.IJsPromise.md)

The JavaScript Promise.

 [IJsSymbol](DotNetBrowser.Js.IJsSymbol.md)

Represent a JavaScript "Symbol".
<remarks>
    JavaScript symbols are unique and immutable primitive values that may be used as the key of an object property.
    Symbols are often used to add unique property keys to an object that won't collide with keys any other code
    might add to the object, and which are hidden from any mechanisms other code might use to access the object.
</remarks>

