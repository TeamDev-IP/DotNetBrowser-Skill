# <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters"></a> Class StartSessionParameters

Namespace: [DotNetBrowser.Capture.Handlers](DotNetBrowser.Capture.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartSessionParameters : BrowserParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.BrowserParameters.md) ← 
[StartSessionParameters](DotNetBrowser.Capture.Handlers.StartSessionParameters.md)

#### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.BrowserParameters.md\#DotNetBrowser\_Browser\_Handlers\_BrowserParameters\_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters_AudioMode"></a> AudioMode

Gets the mode of capturing audio during the content capture session.

```csharp
public AudioMode AudioMode { get; }
```

#### Property Value

 [AudioMode](DotNetBrowser.Capture.AudioMode.md)

### <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters_Frame"></a> Frame

Gets the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> instance that requests the content capture.

```csharp
public IFrame Frame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

### <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters_Sources"></a> Sources

Gets the available <xref href="DotNetBrowser.Capture.Sources" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public Sources Sources { get; }
```

#### Property Value

 [Sources](DotNetBrowser.Capture.Sources.md)

### <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters_Url"></a> Url

Gets the URL of the currently loaded web page.

```csharp
public string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

