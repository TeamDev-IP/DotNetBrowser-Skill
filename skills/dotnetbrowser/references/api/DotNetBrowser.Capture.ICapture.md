# <a id="DotNetBrowser_Capture_ICapture"></a> Interface ICapture

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

A service that can be used for listening and handling capturing sessions.

```csharp
public interface ICapture
```

## Properties

### <a id="DotNetBrowser_Capture_ICapture_Sessions"></a> Sessions

Gets all active capture sessions of the current browser.

```csharp
IReadOnlyList<ISession> Sessions { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ISession](DotNetBrowser.Capture.ISession.md)\>

### <a id="DotNetBrowser_Capture_ICapture_StartSessionHandler"></a> StartSessionHandler

Gets or sets a handler that is used when the browser is about to start capturing sessions.

```csharp
IHandler<StartSessionParameters, StartSessionResponse> StartSessionHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[StartSessionParameters](DotNetBrowser.Capture.Handlers.StartSessionParameters.md), [StartSessionResponse](DotNetBrowser.Capture.Handlers.StartSessionResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Capture_ICapture_SessionStarted"></a> SessionStarted

Occurs when a capture session is started for this browser instance.

```csharp
event EventHandler<SessionStartedEventArgs> SessionStarted
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[SessionStartedEventArgs](DotNetBrowser.Browser.Events.SessionStartedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

