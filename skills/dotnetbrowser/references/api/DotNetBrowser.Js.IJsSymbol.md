# <a id="DotNetBrowser_Js_IJsSymbol"></a> Interface IJsSymbol

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

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Js_IJsSymbol_Description"></a> Description

Gets the symbol description.

```csharp
string Description { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

