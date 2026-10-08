# <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse"></a> Class ShowHttpErrorPageResponse

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowHttpErrorPageResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ShowHttpErrorPageResponse](DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse_Show_System_String_"></a> Show\(string\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should display an error page
with the specified <code class="paramref">errorHtml</code>.

```csharp
public static ShowHttpErrorPageResponse Show(string errorHtml)
```

#### Parameters

`errorHtml` [string](https://learn.microsoft.com/dotnet/api/system.string)

The HTML code of the error page to display.

#### Returns

 [ShowHttpErrorPageResponse](DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse.md)

The <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">errorHtml</code> is null, empty, or contains only white space.

### <a id="DotNetBrowser_Navigation_Handlers_ShowHttpErrorPageResponse_ShowDefault"></a> ShowDefault\(\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should display
the default error page.

```csharp
public static ShowHttpErrorPageResponse ShowDefault()
```

#### Returns

 [ShowHttpErrorPageResponse](DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse.md)

The <xref href="DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.ShowHttpErrorPageHandler" data-throw-if-not-resolved="false"></xref> implementation.

