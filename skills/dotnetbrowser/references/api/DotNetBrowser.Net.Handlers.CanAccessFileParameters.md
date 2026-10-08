# <a id="DotNetBrowser_Net_Handlers_CanAccessFileParameters"></a> Class CanAccessFileParameters

Namespace: [DotNetBrowser.Net.Handlers](DotNetBrowser.Net.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Net.INetwork.CanAccessFileHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class CanAccessFileParameters : NetworkParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[NetworkParameters](DotNetBrowser.Net.Handlers.NetworkParameters.md) ← 
[CanAccessFileParameters](DotNetBrowser.Net.Handlers.CanAccessFileParameters.md)

#### Inherited Members

[NetworkParameters.Network](DotNetBrowser.Net.Handlers.NetworkParameters.md\#DotNetBrowser\_Net\_Handlers\_NetworkParameters\_Network), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_Handlers_CanAccessFileParameters_AbsolutePath"></a> AbsolutePath

Gets the absolute path to the file the request would like to access. On Linux and
macOS returns the path after resolving all symbolic links. On Windows, if the requested
file is a shortcut, the callback will be invoked twice: once for the shortcut, and once
for the destination file path.

```csharp
public string AbsolutePath { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

