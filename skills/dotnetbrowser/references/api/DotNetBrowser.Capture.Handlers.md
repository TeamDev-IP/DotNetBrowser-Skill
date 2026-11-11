# <a id="DotNetBrowser_Capture_Handlers"></a> Namespace DotNetBrowser.Capture.Handlers

### Classes

 [StartSessionParameters](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionParameters)

The parameters of the <xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref>.

 [StartSessionResponse](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionResponse)

A response to the <xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters"></a> Class StartSessionParameters

Namespace: [DotNetBrowser.Capture.Handlers](DotNetBrowser.Capture.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartSessionParameters : BrowserParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BrowserParameters](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters) ← 
[StartSessionParameters](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionParameters)

##### Inherited Members

[BrowserParameters.Browser](DotNetBrowser.Browser.Handlers.md#DotNetBrowser_Browser_Handlers_BrowserParameters_Browser), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters_AudioMode"></a> AudioMode

Gets the mode of capturing audio during the content capture session.

```csharp
public AudioMode AudioMode { get; }
```

##### Property Value

 [AudioMode](DotNetBrowser.Capture.md#DotNetBrowser_Capture_AudioMode)

#### <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters_Frame"></a> Frame

Gets the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> instance that requests the content capture.

```csharp
public IFrame Frame { get; }
```

##### Property Value

 [IFrame](DotNetBrowser.Frames.md#DotNetBrowser_Frames_IFrame)

#### <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters_Sources"></a> Sources

Gets the available <xref href="DotNetBrowser.Capture.Sources" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public Sources Sources { get; }
```

##### Property Value

 [Sources](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Sources)

#### <a id="DotNetBrowser_Capture_Handlers_StartSessionParameters_Url"></a> Url

Gets the URL of the currently loaded web page.

```csharp
public string Url { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse"></a> Class StartSessionResponse

Namespace: [DotNetBrowser.Capture.Handlers](DotNetBrowser.Capture.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartSessionResponse
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[StartSessionResponse](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionResponse)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Methods

#### <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the capture session request
should be canceled.

```csharp
public static StartSessionResponse Cancel()
```

##### Returns

 [StartSessionResponse](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionResponse)

The <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse_SelectSource_DotNetBrowser_Capture_Source_DotNetBrowser_Capture_AudioMode_DotNetBrowser_Capture_NotificationVisibility_"></a> SelectSource\(Source, AudioMode, NotificationVisibility\)

Creates a <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to use the given capture source.

```csharp
public static StartSessionResponse SelectSource(Source source, AudioMode audioMode, NotificationVisibility notificationVisibility = NotificationVisibility.Show)
```

##### Parameters

`source` [Source](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Source)

The content source to use for the capture.

`audioMode` [AudioMode](DotNetBrowser.Capture.md#DotNetBrowser_Capture_AudioMode)

The mode of capturing the audio from the browser.

`notificationVisibility` [NotificationVisibility](DotNetBrowser.Capture.md#DotNetBrowser_Capture_NotificationVisibility)

The visibility of the capture session notification.

##### Returns

 [StartSessionResponse](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionResponse)

The <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref> implementation.

##### Remarks

<p>
           The 

       <pre><code class="lang-csharp">source</code></pre>

must be present in the
           <xref href="DotNetBrowser.Capture.Sources" data-throw-if-not-resolved="false"></xref> received from the <xref href="DotNetBrowser.Capture.Handlers.StartSessionParameters.Sources" data-throw-if-not-resolved="false"></xref>.
       </p>
       <p>
           If the screen capture is forbidden by the system security permissions the request
           will be cancelled.This is usual for macOS where the screen or application window capture
           must be explicitly allowed in the System Preferences.
       </p>

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">source</code> is null.

#### <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse_SelectSource_DotNetBrowser_Browser_IBrowser_DotNetBrowser_Capture_AudioMode_DotNetBrowser_Capture_NotificationVisibility_"></a> SelectSource\(IBrowser, AudioMode, NotificationVisibility\)

Creates a <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to use the given browser as the
capture source.

```csharp
public static StartSessionResponse SelectSource(IBrowser browser, AudioMode audioMode, NotificationVisibility notificationVisibility = NotificationVisibility.Show)
```

##### Parameters

`browser` [IBrowser](DotNetBrowser.Browser.md#DotNetBrowser_Browser_IBrowser)

The browser which contents will be captured.

`audioMode` [AudioMode](DotNetBrowser.Capture.md#DotNetBrowser_Capture_AudioMode)

The mode of capturing the audio from the browser.

`notificationVisibility` [NotificationVisibility](DotNetBrowser.Capture.md#DotNetBrowser_Capture_NotificationVisibility)

The visibility of the capture session notification.

##### Returns

 [StartSessionResponse](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionResponse)

The <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref> implementation.

##### Remarks

<p>
    The passed browser instance and the browser instance requesting the capture session
    must be created by the same <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.
    Otherwise, the content capture will be cancelled.
</p>

##### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">browser</code> is null.

#### <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse_ShowSelectSourceDialog"></a> ShowSelectSourceDialog\(\)

Creates a <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to display the default dialog
for choosing the capture source.

```csharp
public static StartSessionResponse ShowSelectSourceDialog()
```

##### Returns

 [StartSessionResponse](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionResponse)

The <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref> implementation.
