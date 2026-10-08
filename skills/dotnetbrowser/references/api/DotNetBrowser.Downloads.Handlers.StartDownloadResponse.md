# <a id="DotNetBrowser_Downloads_Handlers_StartDownloadResponse"></a> Class StartDownloadResponse

Namespace: [DotNetBrowser.Downloads.Handlers](DotNetBrowser.Downloads.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Browser.IBrowser.StartDownloadHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartDownloadResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[StartDownloadResponse](DotNetBrowser.Downloads.Handlers.StartDownloadResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Downloads_Handlers_StartDownloadResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the file download should be canceled.

```csharp
public static StartDownloadResponse Cancel()
```

#### Returns

 [StartDownloadResponse](DotNetBrowser.Downloads.Handlers.StartDownloadResponse.md)

The <xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.StartDownloadHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Downloads_Handlers_StartDownloadResponse_DownloadTo_System_String_"></a> DownloadTo\(string\)

Creates a <xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse" data-throw-if-not-resolved="false"></xref> that notifies the engine that the file should be downloaded into a
specific
location.

```csharp
public static StartDownloadResponse DownloadTo(string filePath)
```

#### Parameters

`filePath` [string](https://learn.microsoft.com/dotnet/api/system.string)

The absolute path to store the downloaded file.

#### Returns

 [StartDownloadResponse](DotNetBrowser.Downloads.Handlers.StartDownloadResponse.md)

The <xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Browser.IBrowser.StartDownloadHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">filePath</code> is null, empty, or contains only blank characters.

