# <a id="DotNetBrowser_Browser_CspParameters"></a> Class CspParameters

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

The parameters describing the particular key container within
a particular cryptographic service provider (CSP).

```csharp
public sealed class CspParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CspParameters](DotNetBrowser.Browser.CspParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_CspParameters_KeyContainerName"></a> KeyContainerName

Gets or sets the key container name.

```csharp
public string KeyContainerName { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_CspParameters_Pin"></a> Pin

Gets or sets the PIN associated with a smart card key.

```csharp
public string Pin { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

Use this property to supply a password for a smart card key.
When you specify a password using this property, a password dialog box
will not be presented to the user.

### <a id="DotNetBrowser_Browser_CspParameters_ProviderName"></a> ProviderName

Gets or sets the cryptographic service provider (CSP) name.

```csharp
public string ProviderName { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Browser_CspParameters_ProviderType"></a> ProviderType

Gets or sets the provider type.

```csharp
public int ProviderType { get; set; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

