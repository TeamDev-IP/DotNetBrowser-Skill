# <a id="DotNetBrowser_Browser_Handlers_InjectCssResponse"></a> Class InjectCssResponse

Namespace: [DotNetBrowser.Browser.Handlers](DotNetBrowser.Browser.Handlers.md)  
Assembly: DotNetBrowser.dll  

The response to the <xref href="DotNetBrowser.Browser.IBrowser.InjectCssHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class InjectCssResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[InjectCssResponse](DotNetBrowser.Browser.Handlers.InjectCssResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Browser_Handlers_InjectCssResponse_Inject_System_String_"></a> Inject\(string\)

Creates an <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse" data-throw-if-not-resolved="false"></xref> that injects the given <code class="paramref">customStylesheet</code> string that
represents a custom stylesheet
(CSS) into the document that is loaded in this browser instance.

```csharp
public static InjectCssResponse Inject(string customStylesheet)
```

#### Parameters

`customStylesheet` [string](https://learn.microsoft.com/dotnet/api/system.string)

The CSS code that will be injected into the document.

#### Returns

 [InjectCssResponse](DotNetBrowser.Browser.Handlers.InjectCssResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.InjectCssHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Remarks

If the CSS property defined in the given <code class="paramref">customStylesheet</code> string already exists
on the loaded HTML document, then the existing CSS property won't be overridden. The CSS
properties defined in the given <code class="paramref">customStylesheet</code> string will be applied only if
these properties aren't defined on the loaded document.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">customStylesheet</code> is null, empty or blank.

### <a id="DotNetBrowser_Browser_Handlers_InjectCssResponse_Proceed"></a> Proceed\(\)

Creates a <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it can proceed without injecting a custom
stylesheet.

```csharp
public static InjectCssResponse Proceed()
```

#### Returns

 [InjectCssResponse](DotNetBrowser.Browser.Handlers.InjectCssResponse.md)

The <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.InjectCssHandler" data-throw-if-not-resolved="false"></xref> implementation.

