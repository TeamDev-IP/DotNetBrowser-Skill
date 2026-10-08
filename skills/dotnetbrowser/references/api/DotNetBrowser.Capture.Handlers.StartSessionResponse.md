# <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse"></a> Class StartSessionResponse

Namespace: [DotNetBrowser.Capture.Handlers](DotNetBrowser.Capture.Handlers.md)  
Assembly: DotNetBrowser.dll  

A response to the <xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class StartSessionResponse
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[StartSessionResponse](DotNetBrowser.Capture.Handlers.StartSessionResponse.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse_Cancel"></a> Cancel\(\)

Creates a <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser that the capture session request
should be canceled.

```csharp
public static StartSessionResponse Cancel()
```

#### Returns

 [StartSessionResponse](DotNetBrowser.Capture.Handlers.StartSessionResponse.md)

The <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref> implementation.

### <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse_SelectSource_DotNetBrowser_Capture_Source_DotNetBrowser_Capture_AudioMode_DotNetBrowser_Capture_NotificationVisibility_"></a> SelectSource\(Source, AudioMode, NotificationVisibility\)

Creates a <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to use the given capture source.

```csharp
public static StartSessionResponse SelectSource(Source source, AudioMode audioMode, NotificationVisibility notificationVisibility = NotificationVisibility.Show)
```

#### Parameters

`source` [Source](DotNetBrowser.Capture.Source.md)

The content source to use for the capture.

`audioMode` [AudioMode](DotNetBrowser.Capture.AudioMode.md)

The mode of capturing the audio from the browser.

`notificationVisibility` [NotificationVisibility](DotNetBrowser.Capture.NotificationVisibility.md)

The visibility of the capture session notification.

#### Returns

 [StartSessionResponse](DotNetBrowser.Capture.Handlers.StartSessionResponse.md)

The <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Remarks

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

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">source</code> is null.

### <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse_SelectSource_DotNetBrowser_Browser_IBrowser_DotNetBrowser_Capture_AudioMode_DotNetBrowser_Capture_NotificationVisibility_"></a> SelectSource\(IBrowser, AudioMode, NotificationVisibility\)

Creates a <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to use the given browser as the
capture source.

```csharp
public static StartSessionResponse SelectSource(IBrowser browser, AudioMode audioMode, NotificationVisibility notificationVisibility = NotificationVisibility.Show)
```

#### Parameters

`browser` [IBrowser](DotNetBrowser.Browser.IBrowser.md)

The browser which contents will be captured.

`audioMode` [AudioMode](DotNetBrowser.Capture.AudioMode.md)

The mode of capturing the audio from the browser.

`notificationVisibility` [NotificationVisibility](DotNetBrowser.Capture.NotificationVisibility.md)

The visibility of the capture session notification.

#### Returns

 [StartSessionResponse](DotNetBrowser.Capture.Handlers.StartSessionResponse.md)

The <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref> implementation.

#### Remarks

<p>
    The passed browser instance and the browser instance requesting the capture session
    must be created by the same <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.
    Otherwise, the content capture will be cancelled.
</p>

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">browser</code> is null.

### <a id="DotNetBrowser_Capture_Handlers_StartSessionResponse_ShowSelectSourceDialog"></a> ShowSelectSourceDialog\(\)

Creates a <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> that notifies the browser to display the default dialog
for choosing the capture source.

```csharp
public static StartSessionResponse ShowSelectSourceDialog()
```

#### Returns

 [StartSessionResponse](DotNetBrowser.Capture.Handlers.StartSessionResponse.md)

The <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse" data-throw-if-not-resolved="false"></xref> instance that can be used as a return value in
<xref href="DotNetBrowser.Capture.ICapture.StartSessionHandler" data-throw-if-not-resolved="false"></xref> implementation.

