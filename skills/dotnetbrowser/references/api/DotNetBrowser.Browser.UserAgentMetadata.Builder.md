# <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder"></a> Class UserAgentMetadata.Builder

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

A builder class to construct <xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref>.

```csharp
public class UserAgentMetadata.Builder
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserAgentMetadata.Builder](DotNetBrowser.Browser.UserAgentMetadata.Builder.md)

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

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder__ctor"></a> Builder\(\)

Initializes a new instance of <xref href="DotNetBrowser.Browser.UserAgentMetadata.Builder" data-throw-if-not-resolved="false"></xref> is initialized with default values.

```csharp
public Builder()
```

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder__ctor_DotNetBrowser_Browser_UserAgentMetadata_"></a> Builder\(UserAgentMetadata\)

Initializes a new instance of <xref href="DotNetBrowser.Browser.UserAgentMetadata.Builder" data-throw-if-not-resolved="false"></xref> with an existing <xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public Builder(UserAgentMetadata metadata)
```

#### Parameters

`metadata` [UserAgentMetadata](DotNetBrowser.Browser.UserAgentMetadata.md)

<xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref> instance to initialize Builder.

## Properties

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Architecture"></a> Architecture

Gets or sets the CPU architecture of the system.

```csharp
public string Architecture { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Bitness"></a> Bitness

Gets or sets bitness of the system architecture.

```csharp
public string Bitness { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_BrandFullVersionList"></a> BrandFullVersionList

Gets the list of brand and full versions. Typically, providing more detailed version information.

```csharp
public List<UserAgentBrandVersion> BrandFullVersionList { get; }
```

#### Property Value

 [List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<[UserAgentBrandVersion](DotNetBrowser.Browser.UserAgentBrandVersion.md)\>

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_BrandVersionList"></a> BrandVersionList

Gets the list of brand and major versions.

```csharp
public List<UserAgentBrandVersion> BrandVersionList { get; }
```

#### Property Value

 [List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<[UserAgentBrandVersion](DotNetBrowser.Browser.UserAgentBrandVersion.md)\>

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_FormFactors"></a> FormFactors

Gets the form-factors associated with the device.

```csharp
public List<string> FormFactors { get; }
```

#### Property Value

 [List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_FullVersion"></a> FullVersion

Gets or sets the full version string that corresponds to the user agent, or a brand in the brand list.

```csharp
public string FullVersion { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Mobile"></a> Mobile

Gets or sets the mobile flag that show whether the client device is a mobile device.

```csharp
public bool Mobile { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Model"></a> Model

Gets or sets the model name of the device running the user agent.

```csharp
public string Model { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Platform"></a> Platform

Gets or sets the commercial name of the user agent's operating system.

```csharp
public string Platform { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_PlatformVersion"></a> PlatformVersion

Gets or sets the version of the operating system running the user agent.

```csharp
public string PlatformVersion { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Wow64"></a> Wow64

Gets or sets WOW64 flag that indicates if the user agent is running in 32-bit mode on a 64-bit Windows system.

```csharp
public bool Wow64 { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

## Methods

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Builder_Build"></a> Build\(\)

Creates a <xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public UserAgentMetadata Build()
```

#### Returns

 [UserAgentMetadata](DotNetBrowser.Browser.UserAgentMetadata.md)

new <xref href="DotNetBrowser.Browser.UserAgentMetadata" data-throw-if-not-resolved="false"></xref> instance initialized according to the current builder state.

