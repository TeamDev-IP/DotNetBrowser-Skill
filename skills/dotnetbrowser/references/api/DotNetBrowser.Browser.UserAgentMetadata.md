# <a id="DotNetBrowser_Browser_UserAgentMetadata"></a> Class UserAgentMetadata

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

Contains the client hints data.

```csharp
public class UserAgentMetadata
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserAgentMetadata](DotNetBrowser.Browser.UserAgentMetadata.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Architecture"></a> Architecture

Gets the CPU architecture of the system.

```csharp
public string Architecture { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Bitness"></a> Bitness

Gets the bitness of the system architecture.

```csharp
public string Bitness { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_BrandFullVersionList"></a> BrandFullVersionList

Gets the list of brand and full versions. Typically, providing more detailed version information.

```csharp
public IReadOnlyList<UserAgentBrandVersion> BrandFullVersionList { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[UserAgentBrandVersion](DotNetBrowser.Browser.UserAgentBrandVersion.md)\>

### <a id="DotNetBrowser_Browser_UserAgentMetadata_BrandVersionList"></a> BrandVersionList

Gets the list of brand and major versions.

```csharp
public IReadOnlyList<UserAgentBrandVersion> BrandVersionList { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[UserAgentBrandVersion](DotNetBrowser.Browser.UserAgentBrandVersion.md)\>

### <a id="DotNetBrowser_Browser_UserAgentMetadata_FormFactors"></a> FormFactors

Gets the form-factors associated with the device.

```csharp
public IReadOnlyList<string> FormFactors { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

### <a id="DotNetBrowser_Browser_UserAgentMetadata_FullVersion"></a> FullVersion

Gets the full version string that corresponds to the user agent, or a brand in the brand list.

```csharp
public string FullVersion { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Mobile"></a> Mobile

Gets the mobile flag that show whether the client device is a mobile device.

```csharp
public bool Mobile { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Model"></a> Model

Gets the model name of the device running the user agent.

```csharp
public string Model { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Platform"></a> Platform

Gets the commercial name of the user agent's operating system.

```csharp
public string Platform { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_PlatformVersion"></a> PlatformVersion

Gets the version of the operating system running the user agent.

```csharp
public string PlatformVersion { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_UserAgentMetadata_Wow64"></a> Wow64

Gets WOW64 flag that indicates if the user agent is running in 32-bit mode on a 64-bit Windows system.

```csharp
public bool Wow64 { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

