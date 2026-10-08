# <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder"></a> Class UserAgentBrandVersion.Builder

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

A builder class to construct <xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref>.

```csharp
public class UserAgentBrandVersion.Builder
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserAgentBrandVersion.Builder](DotNetBrowser.Browser.UserAgentBrandVersion.Builder.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Each of the properties modifies the state of the builder. Builders are not thread-safe and should
not be used concurrently from multiple threads without external synchronization.

## Constructors

### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder__ctor"></a> Builder\(\)

Initializes a new instance of <xref href="DotNetBrowser.Browser.UserAgentBrandVersion.Builder" data-throw-if-not-resolved="false"></xref>.

```csharp
public Builder()
```

### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder__ctor_DotNetBrowser_Browser_UserAgentBrandVersion_"></a> Builder\(UserAgentBrandVersion\)

Initializes a new instance of <xref href="DotNetBrowser.Browser.UserAgentBrandVersion.Builder" data-throw-if-not-resolved="false"></xref> with an existing <xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref>
instance.

```csharp
public Builder(UserAgentBrandVersion brandVersion)
```

#### Parameters

`brandVersion` [UserAgentBrandVersion](DotNetBrowser.Browser.UserAgentBrandVersion.md)

<xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref> instance to initialize Builder.

## Properties

### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder_Brand"></a> Brand

Gets or sets the commercial name of the user agent or brand.

```csharp
public string Brand { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder_Version"></a> Version

Gets or sets the version of the brand.

```csharp
public string Version { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Browser_UserAgentBrandVersion_Builder_Build"></a> Build\(\)

Creates a <xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public UserAgentBrandVersion Build()
```

#### Returns

 [UserAgentBrandVersion](DotNetBrowser.Browser.UserAgentBrandVersion.md)

new <xref href="DotNetBrowser.Browser.UserAgentBrandVersion" data-throw-if-not-resolved="false"></xref> instance initialized according to the current builder state.

