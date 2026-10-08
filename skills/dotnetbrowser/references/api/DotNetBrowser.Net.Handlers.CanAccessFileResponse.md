# <a id="DotNetBrowser_Net_Handlers_CanAccessFileResponse"></a> Class CanAccessFileResponse

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response for the <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanAccessFileResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CanAccessFileResponse](DotNetBrowser.Net.Handlers.CanAccessFileResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Net_Handlers_CanAccessFileResponse_Can"></a> Can\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse" data-throw-if-not-resolved="false"></xref> that allows access to the file.

```csharp
public static CanAccessFileResponse Can()
```

#### Returns

 [CanAccessFileResponse](DotNetBrowser.Net.Handlers.CanAccessFileResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Net_Handlers_CanAccessFileResponse_Cannot"></a> Cannot\(\)

Creates a <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse" data-throw-if-not-resolved="false"></xref> that denies access to the file.

```csharp
public static CanAccessFileResponse Cannot()
```

#### Returns

 [CanAccessFileResponse](DotNetBrowser.Net.Handlers.CanAccessFileResponse.md)

The <xref href="DotNetBrowser.Net.Handlers.CanAccessFileResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a
return value in <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref> implementation.

