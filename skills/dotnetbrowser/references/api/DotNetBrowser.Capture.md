# <a id="DotNetBrowser_Capture"></a> Namespace DotNetBrowser.Capture

### Namespaces

 [DotNetBrowser.Capture.Events](DotNetBrowser.Capture.Events.md)

 [DotNetBrowser.Capture.Handlers](DotNetBrowser.Capture.Handlers.md)

### Classes

 [Source](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Source)

The source for the content capture session.

 [Sources](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Sources)

Provides the access to the sources available for content capture.

### Interfaces

 [ICapture](DotNetBrowser.Capture.md#DotNetBrowser_Capture_ICapture)

A service that can be used for listening and handling capturing sessions.

 [ISession](DotNetBrowser.Capture.md#DotNetBrowser_Capture_ISession)

A content capture session.

### Enums

 [AudioMode](DotNetBrowser.Capture.md#DotNetBrowser_Capture_AudioMode)

The mode of capturing audio during the content capture session.

 [NotificationVisibility](DotNetBrowser.Capture.md#DotNetBrowser_Capture_NotificationVisibility)

Specifies whether the notification about the capture session should be shown or hidden.

 [SourceType](DotNetBrowser.Capture.md#DotNetBrowser_Capture_SourceType)

The type of the content capture source.

## <a id="DotNetBrowser_Capture_Source"></a> Class Source

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

The source for the content capture session.

```csharp
public sealed class Source
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Source](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Source)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Capture_Source_Name"></a> Name

Gets the name of the capture source.

```csharp
public string Name { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Capture_Source_Thumbnail"></a> Thumbnail

Gets the <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> instance that contains the image of the capture source.

```csharp
public Bitmap Thumbnail { get; }
```

##### Property Value

 [Bitmap](DotNetBrowser.Ui.md#DotNetBrowser_Ui_Bitmap)

#### <a id="DotNetBrowser_Capture_Source_Type"></a> Type

Gets the type of this capture source.

```csharp
public SourceType Type { get; }
```

##### Property Value

 [SourceType](DotNetBrowser.Capture.md#DotNetBrowser_Capture_SourceType)

## <a id="DotNetBrowser_Capture_Sources"></a> Class Sources

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

Provides the access to the sources available for content capture.

```csharp
public sealed class Sources
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Sources](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Sources)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Capture_Sources_ApplicationWindows"></a> ApplicationWindows

Gets all of the available application windows for capture.

```csharp
public IReadOnlyList<Source> ApplicationWindows { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Source](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Source)\>

#### <a id="DotNetBrowser_Capture_Sources_Browsers"></a> Browsers

Gets all of the available browsers for capture.

```csharp
public IReadOnlyList<Source> Browsers { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Source](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Source)\>

#### <a id="DotNetBrowser_Capture_Sources_Screens"></a> Screens

Gets all of the available screens for capture.

```csharp
public IReadOnlyList<Source> Screens { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[Source](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Source)\>

## <a id="DotNetBrowser_Capture_ICapture"></a> Interface ICapture

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

A service that can be used for listening and handling capturing sessions.

```csharp
public interface ICapture
```

### Properties

#### <a id="DotNetBrowser_Capture_ICapture_Sessions"></a> Sessions

Gets all active capture sessions of the current browser.

```csharp
IReadOnlyList<ISession> Sessions { get; }
```

##### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ISession](DotNetBrowser.Capture.md#DotNetBrowser_Capture_ISession)\>

#### <a id="DotNetBrowser_Capture_ICapture_StartSessionHandler"></a> StartSessionHandler

Gets or sets a handler that is used when the browser is about to start capturing sessions.

```csharp
IHandler<StartSessionParameters, StartSessionResponse> StartSessionHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[StartSessionParameters](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionParameters), [StartSessionResponse](DotNetBrowser.Capture.Handlers.md#DotNetBrowser_Capture_Handlers_StartSessionResponse)\>

##### Remarks

<p>
    Use the <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse.ShowSelectSourceDialog" data-throw-if-not-resolved="false"></xref> method to
    display the default dialog for choosing the capture source.
</p>
<p>
    Use the <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse.SelectSource(DotNetBrowser.Capture.Source%2cDotNetBrowser.Capture.AudioMode%2cDotNetBrowser.Capture.NotificationVisibility)" data-throw-if-not-resolved="false"></xref> method to
    use the given capture source.
</p>
<p>
    Use the <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse.SelectSource(DotNetBrowser.Browser.IBrowser%2cDotNetBrowser.Capture.AudioMode%2cDotNetBrowser.Capture.NotificationVisibility)" data-throw-if-not-resolved="false"></xref> method to
    use the given browser as the capture source.
</p>
<p>
    Use the<xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse.Cancel" data-throw-if-not-resolved="false"></xref> method
    if the capture session request should be canceled.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Capture.Handlers.StartSessionResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

#### <a id="DotNetBrowser_Capture_ICapture_SessionStarted"></a> SessionStarted

Occurs when a capture session is started for this browser instance.

```csharp
event EventHandler<SessionStartedEventArgs> SessionStarted
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[SessionStartedEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_SessionStartedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Capture_ISession"></a> Interface ISession

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

A content capture session.

```csharp
public interface ISession : IDisposable, IAutoDisposable
```

##### Implements

[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Capture_ISession_IsActive"></a> IsActive

Indicates whether this capture session is active.

```csharp
bool IsActive { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Capture.ISession" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Capture_ISession_Source"></a> Source

Gets the <xref href="DotNetBrowser.Capture.Source" data-throw-if-not-resolved="false"></xref> instance for this capture session.

```csharp
Source Source { get; }
```

##### Property Value

 [Source](DotNetBrowser.Capture.md#DotNetBrowser_Capture_Source)

### Methods

#### <a id="DotNetBrowser_Capture_ISession_Stop"></a> Stop\(\)

Stops the capture session.

```csharp
void Stop()
```

##### Remarks

<p>
    This method has no effect when this capture session is already stopped.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Capture.ISession" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Capture_ISession_Stopped"></a> Stopped

Occurs when the browser has stopped a content capture session.

```csharp
event EventHandler<SessionStoppedEventArgs> Stopped
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[SessionStoppedEventArgs](DotNetBrowser.Capture.Events.md#DotNetBrowser_Capture_Events_SessionStoppedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Capture.ISession" data-throw-if-not-resolved="false"></xref> has already been disposed.

## <a id="DotNetBrowser_Capture_AudioMode"></a> Enum AudioMode

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

The mode of capturing audio during the content capture session.

```csharp
public enum AudioMode
```

### Fields

`Capture = 1` 

The audio content should be captured along with the video content.



`Ignore = 0` 

The audio content should not be captured along with the video content.

## <a id="DotNetBrowser_Capture_NotificationVisibility"></a> Enum NotificationVisibility

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

Specifies whether the notification about the capture session should be shown or hidden.

```csharp
public enum NotificationVisibility
```

### Fields

`Hide = 1` 

The notification about the capture session should be hidden during the capture session.



`Show = 0` 

The notification about the capture session should be shown during the capture session.

## <a id="DotNetBrowser_Capture_SourceType"></a> Enum SourceType

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

The type of the content capture source.

```csharp
public enum SourceType
```

### Fields

`ApplicationWindow = 2` 

The content is captured from an application window.



`Browser = 3` 

The content is captured from a <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.



`Screen = 1` 

The content is captured from a screen.
