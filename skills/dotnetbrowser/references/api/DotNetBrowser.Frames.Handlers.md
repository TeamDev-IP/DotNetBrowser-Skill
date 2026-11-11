# <a id="DotNetBrowser_Frames_Handlers"></a> Namespace DotNetBrowser.Frames.Handlers

### Classes

 [ConvertJsNameParameters](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameParameters)

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.ConvertJsNameHandler" data-throw-if-not-resolved="false"></xref>.

 [ConvertJsNameResponse](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameResponse)

The response to the <xref href="DotNetBrowser.Browser.IBrowser.ConvertJsNameHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Frames_Handlers_ConvertJsNameParameters"></a> Class ConvertJsNameParameters

Namespace: [DotNetBrowser.Frames.Handlers](DotNetBrowser.Frames.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Browser.IBrowser.ConvertJsNameHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ConvertJsNameParameters : FrameParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[FrameParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters) ← 
[ConvertJsNameParameters](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameParameters)

##### Inherited Members

[FrameParameters.Frame](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_FrameParameters_Frame), 
[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Frames_Handlers_ConvertJsNameParameters_MemberInfo"></a> MemberInfo

Gets the <xref href="System.Reflection.MemberInfo" data-throw-if-not-resolved="false"></xref> of the .NET object property, field or method.

```csharp
public MemberInfo MemberInfo { get; }
```

##### Property Value

 [MemberInfo](https://learn.microsoft.com/dotnet/api/system.reflection.memberinfo)

## <a id="DotNetBrowser_Frames_Handlers_ConvertJsNameResponse"></a> Class ConvertJsNameResponse

Namespace: [DotNetBrowser.Frames.Handlers](DotNetBrowser.Frames.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.ConvertJsNameHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ConvertJsNameResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ConvertJsNameResponse](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Frames_Handlers_ConvertJsNameResponse_CamelCase"></a> CamelCase

Creates a <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse" data-throw-if-not-resolved="false"></xref> that converts the name
to CamelCase (the first letter of the name is lower case).

```csharp
public static ConvertJsNameResponse CamelCase { get; }
```

##### Property Value

 [ConvertJsNameResponse](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameResponse)

#### <a id="DotNetBrowser_Frames_Handlers_ConvertJsNameResponse_NoConversion"></a> NoConversion

Creates a <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse" data-throw-if-not-resolved="false"></xref> that use the member name as is.

```csharp
public static ConvertJsNameResponse NoConversion { get; }
```

##### Property Value

 [ConvertJsNameResponse](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameResponse)

#### <a id="DotNetBrowser_Frames_Handlers_ConvertJsNameResponse_PascalCase"></a> PascalCase

Creates a <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse" data-throw-if-not-resolved="false"></xref> that converts the name
to PascalCase (the first letter of the name is upper case).

```csharp
public static ConvertJsNameResponse PascalCase { get; }
```

##### Property Value

 [ConvertJsNameResponse](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameResponse)

### Methods

#### <a id="DotNetBrowser_Frames_Handlers_ConvertJsNameResponse_ConvertTo_System_String_"></a> ConvertTo\(string\)

Creates a <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse" data-throw-if-not-resolved="false"></xref> that sets the custom name for
binding or executing JavaScript.

```csharp
public static ConvertJsNameResponse ConvertTo(string customName)
```

##### Parameters

`customName` [string](https://learn.microsoft.com/dotnet/api/system.string)

The custom name of the JavaScript property, field or method.

##### Returns

 [ConvertJsNameResponse](DotNetBrowser.Frames.Handlers.md#DotNetBrowser_Frames_Handlers_ConvertJsNameResponse)

The <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Browser.IBrowser.ConvertJsNameHandler" data-throw-if-not-resolved="false"></xref> implementation.

##### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">customName</code> is null, empty, or contains only blank characters.
