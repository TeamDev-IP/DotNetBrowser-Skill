# <a id="DotNetBrowser_Navigation_LoadUrlParameters"></a> Class LoadUrlParameters

Namespace: [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)  
Assembly: DotNetBrowser.dll  

The parameters of the load url request.

```csharp
public sealed class LoadUrlParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[LoadUrlParameters](DotNetBrowser.Navigation.LoadUrlParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Navigation_LoadUrlParameters__ctor_System_String_"></a> LoadUrlParameters\(string\)

Initializes a new instance of <xref href="DotNetBrowser.Navigation.LoadUrlParameters" data-throw-if-not-resolved="false"></xref> with the specified <code class="paramref">url</code>.

```csharp
public LoadUrlParameters(string url)
```

#### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to load.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">url</code> is null, empty or contain only white space.

## Properties

### <a id="DotNetBrowser_Navigation_LoadUrlParameters_HttpHeaders"></a> HttpHeaders

Gets or sets the HTTP headers that will be sent with the request.

```csharp
public IEnumerable<HttpHeader> HttpHeaders { get; set; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[HttpHeader](DotNetBrowser.Net.HttpHeader.md)\>

#### Remarks

Setting certain forbidden headers (such as 'Referer', 'Host', 'Content-Length', 'Keep-Alive', 'Proxy-headers',
'TE', etc.) will have no effect due to browser security restrictions. These headers are controlled by the browser and
cannot be set for <xref href="DotNetBrowser.Navigation.LoadUrlParameters" data-throw-if-not-resolved="false"></xref> for security reasons.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">value</code> is null or contains null items.

### <a id="DotNetBrowser_Navigation_LoadUrlParameters_UploadData"></a> UploadData

Gets or sets the POST upload data that will be sent with the request.

```csharp
public UploadData UploadData { get; set; }
```

#### Property Value

 [UploadData](DotNetBrowser.Net.UploadData.md)

### <a id="DotNetBrowser_Navigation_LoadUrlParameters_Url"></a> Url

Gets the URL of the resource to load.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

