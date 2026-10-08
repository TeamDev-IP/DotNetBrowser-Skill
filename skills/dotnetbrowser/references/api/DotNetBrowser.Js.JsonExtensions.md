# <a id="DotNetBrowser_Js_JsonExtensions"></a> Class JsonExtensions

Namespace: [DotNetBrowser.Js](DotNetBrowser.Js.md)  
Assembly: DotNetBrowser.dll  

Contains methods for working with JSON strings

```csharp
public static class JsonExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[JsonExtensions](DotNetBrowser.Js.JsonExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Js_JsonExtensions_ParseJsonString__1_DotNetBrowser_Frames_IFrame_System_String_"></a> ParseJsonString<T\>\(IFrame, string\)

Creates an object that represents the result of parsing the given string in JSON format.

```csharp
public static T ParseJsonString<T>(this IFrame frame, string jsonString)
```

#### Parameters

`frame` [IFrame](DotNetBrowser.Frames.IFrame.md)

The frame to use for conversion.

`jsonString` [string](https://learn.microsoft.com/dotnet/api/system.string)

A string in JSON format.

#### Returns

 T

The result of parsing. Can be <code>null</code> if the result of parsing is <code>null</code>.
For example, when the given JSON string is "null", then the method returns <code>null</code>

#### Type Parameters

`T` 

The expected result type. The following types are supported: <xref href="System.Boolean" data-throw-if-not-resolved="false"></xref>,
<xref href="System.Double" data-throw-if-not-resolved="false"></xref>, <xref href="System.String" data-throw-if-not-resolved="false"></xref>, <xref href="DotNetBrowser.Js.IJsObject" data-throw-if-not-resolved="false"></xref>, or <xref href="System.Object" data-throw-if-not-resolved="false"></xref>.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The given JSON string object cannot be parsed.

### <a id="DotNetBrowser_Js_JsonExtensions_ParseJsonString_DotNetBrowser_Frames_IFrame_System_String_"></a> ParseJsonString\(IFrame, string\)

Creates an object that represents the result of parsing the given string in JSON format.

```csharp
public static object ParseJsonString(this IFrame frame, string jsonString)
```

#### Parameters

`frame` [IFrame](DotNetBrowser.Frames.IFrame.md)

The frame to use for conversion.

`jsonString` [string](https://learn.microsoft.com/dotnet/api/system.string)

A string in JSON format.

#### Returns

 [object](https://learn.microsoft.com/dotnet/api/system.object)

The result of parsing. Can be <code>null</code> if the result of parsing is <code>null</code>.
For example, when the given JSON string is "null", then the method returns <code>null</code>

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The given JSON string object cannot be parsed.

### <a id="DotNetBrowser_Js_JsonExtensions_ToJsonString_DotNetBrowser_Js_IJsObject_"></a> ToJsonString\(IJsObject\)

Converts the given JavaScript object into a JSON string.

```csharp
public static string ToJsonString(this IJsObject jsObject)
```

#### Parameters

`jsObject` [IJsObject](DotNetBrowser.Js.IJsObject.md)

The JavaScript object to convert.

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

A JSON representation of the given JavaScript object.

#### Exceptions

 [JsException](DotNetBrowser.Js.JsException.md)

The given JavaScript object cannot be converted to a JSON string.
For example, a circular reference was found in the given JavaScript object.

