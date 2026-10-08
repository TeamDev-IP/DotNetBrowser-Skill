# <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse"></a> Class ShowNetErrorPageResponse

Namespace: [DotNetBrowser.Navigation.Handlers](DotNetBrowser.Navigation.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class ShowNetErrorPageResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ShowNetErrorPageResponse](DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse_Show_System_String_"></a> Show\(string\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should display an error page
with the specified <code class="paramref">errorHtml</code>.

```csharp
public static ShowNetErrorPageResponse Show(string errorHtml)
```

#### Parameters

`errorHtml` [string](https://learn.microsoft.com/dotnet/api/system.string)

The HTML code of the error page to display.

#### Returns

 [ShowNetErrorPageResponse](DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse.md)

The <xref href="DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">errorHtml</code> is null, empty, or contains only white space.

### <a id="DotNetBrowser_Navigation_Handlers_ShowNetErrorPageResponse_ShowDefault"></a> ShowDefault\(\)

Creates a <xref href="DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that it should display
the default error page.

```csharp
public static ShowNetErrorPageResponse ShowDefault()
```

#### Returns

 [ShowNetErrorPageResponse](DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse.md)

The <xref href="DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Navigation.INavigation.ShowNetErrorPageHandler" data-throw-if-not-resolved="false"></xref> implementation.

