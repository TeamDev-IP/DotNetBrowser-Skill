# <a id="DotNetBrowser_Capture_ISession"></a> Interface ISession

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

A content capture session.

```csharp
public interface ISession : IDisposable, IAutoDisposable
```

#### Implements

[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Capture_ISession_IsActive"></a> IsActive

Indicates whether this capture session is active.

```csharp
bool IsActive { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Capture.ISession" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Capture_ISession_Source"></a> Source

Gets the <xref href="DotNetBrowser.Capture.Source" data-throw-if-not-resolved="false"></xref> instance for this capture session.

```csharp
Source Source { get; }
```

#### Property Value

 [Source](DotNetBrowser.Capture.Source.md)

## Methods

### <a id="DotNetBrowser_Capture_ISession_Stop"></a> Stop\(\)

Stops the capture session.

```csharp
void Stop()
```

#### Remarks

<p>
    This method has no effect when this capture session is already stopped.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Capture.ISession" data-throw-if-not-resolved="false"></xref> object has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Capture_ISession_Stopped"></a> Stopped

Occurs when the browser has stopped a content capture session.

```csharp
event EventHandler<SessionStoppedEventArgs> Stopped
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[SessionStoppedEventArgs](DotNetBrowser.Capture.Events.SessionStoppedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Capture.ISession" data-throw-if-not-resolved="false"></xref> has already been disposed.

