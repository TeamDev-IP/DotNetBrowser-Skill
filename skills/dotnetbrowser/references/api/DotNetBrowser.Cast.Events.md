# <a id="DotNetBrowser_Cast_Events"></a> Namespace DotNetBrowser.Cast.Events

### Classes

 [CastSessionDiscoveredEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_CastSessionDiscoveredEventArgs)

Event arguments for the <xref href="DotNetBrowser.Cast.ICastSessions.Discovered" data-throw-if-not-resolved="false"></xref> event.

<p>
    The new cast session is discovered after the user started casting media content via DotNetBrowser
    API, or another application, i.e.Google Chrome.
</p>

 [CastSessionStartFailedEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Cast.ICastSessions.StartFailed" data-throw-if-not-resolved="false"></xref> event.

 [CastSessionStoppedEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_CastSessionStoppedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Cast.ICastSession.Stopped" data-throw-if-not-resolved="false"></xref> event.

<p>
    Also, the cast session is stopped when the user starts a new cast session to the
    <xref href="DotNetBrowser.Cast.ICastSession.MediaReceiver" data-throw-if-not-resolved="false"></xref> receiver of this cast session.
</p>

 [MediaReceiverDisconnectedEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_MediaReceiverDisconnectedEventArgs)

Event arguments for the <xref href="DotNetBrowser.Cast.IMediaReceiver.Disconnected" data-throw-if-not-resolved="false"></xref> event.

 [MediaReceiverDiscoveredEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_MediaReceiverDiscoveredEventArgs)

Event arguments for the <xref href="DotNetBrowser.Cast.IMediaReceivers.Discovered" data-throw-if-not-resolved="false"></xref> event.

## <a id="DotNetBrowser_Cast_Events_CastSessionDiscoveredEventArgs"></a> Class CastSessionDiscoveredEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.ICastSessions.Discovered" data-throw-if-not-resolved="false"></xref> event.

<p>
    The new cast session is discovered after the user started casting media content via DotNetBrowser
    API, or another application, i.e.Google Chrome.
</p>

```csharp
public sealed class CastSessionDiscoveredEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[CastSessionDiscoveredEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_CastSessionDiscoveredEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cast_Events_CastSessionDiscoveredEventArgs_CastSession"></a> CastSession

Gets the discovered session.

```csharp
public ICastSession CastSession { get; }
```

##### Property Value

 [ICastSession](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSession)

#### <a id="DotNetBrowser_Cast_Events_CastSessionDiscoveredEventArgs_CastSessions"></a> CastSessions

Gets the <xref href="DotNetBrowser.Cast.ICastSessions" data-throw-if-not-resolved="false"></xref> instance initiated this event.

```csharp
public ICastSessions CastSessions { get; }
```

##### Property Value

 [ICastSessions](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSessions)

## <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs"></a> Class CastSessionStartFailedEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.ICastSessions.StartFailed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class CastSessionStartFailedEventArgs : BrowserEventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs) ← 
[CastSessionStartFailedEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs)

##### Inherited Members

[BrowserEventArgs.Browser](DotNetBrowser.Browser.Events.md#DotNetBrowser_Browser_Events_BrowserEventArgs_Browser), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_CastSessions"></a> CastSessions

Gets the <xref href="DotNetBrowser.Cast.ICastSessions" data-throw-if-not-resolved="false"></xref> instance initiated this event.

```csharp
public ICastSessions CastSessions { get; }
```

##### Property Value

 [ICastSessions](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSessions)

#### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_Code"></a> Code

Gets the error code obtained from Chromium.

```csharp
public ResultCode Code { get; }
```

##### Property Value

 [ResultCode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ResultCode)

#### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_ErrorMessage"></a> ErrorMessage

Gets the error message obtained from Chromium.

```csharp
public string ErrorMessage { get; }
```

##### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_MediaReceiver"></a> MediaReceiver

Gets the media receiver of the failed cast session.

```csharp
public IMediaReceiver MediaReceiver { get; }
```

##### Property Value

 [IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)

#### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_Mode"></a> Mode

Gets the mode of the requested cast session.

```csharp
public CastMode Mode { get; }
```

##### Property Value

 [CastMode](DotNetBrowser.Cast.md#DotNetBrowser_Cast_CastMode)

## <a id="DotNetBrowser_Cast_Events_CastSessionStoppedEventArgs"></a> Class CastSessionStoppedEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.ICastSession.Stopped" data-throw-if-not-resolved="false"></xref> event.

<p>
    Also, the cast session is stopped when the user starts a new cast session to the
    <xref href="DotNetBrowser.Cast.ICastSession.MediaReceiver" data-throw-if-not-resolved="false"></xref> receiver of this cast session.
</p>

```csharp
public sealed class CastSessionStoppedEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[CastSessionStoppedEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_CastSessionStoppedEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cast_Events_CastSessionStoppedEventArgs_CastSession"></a> CastSession

Gets the cast session that has been stopped.

```csharp
public ICastSession CastSession { get; }
```

##### Property Value

 [ICastSession](DotNetBrowser.Cast.md#DotNetBrowser_Cast_ICastSession)

## <a id="DotNetBrowser_Cast_Events_MediaReceiverDisconnectedEventArgs"></a> Class MediaReceiverDisconnectedEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.IMediaReceiver.Disconnected" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MediaReceiverDisconnectedEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[MediaReceiverDisconnectedEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_MediaReceiverDisconnectedEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cast_Events_MediaReceiverDisconnectedEventArgs_MediaReceiver"></a> MediaReceiver

Gets the media receiver that has been disconnected.

```csharp
public IMediaReceiver MediaReceiver { get; }
```

##### Property Value

 [IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)

## <a id="DotNetBrowser_Cast_Events_MediaReceiverDiscoveredEventArgs"></a> Class MediaReceiverDiscoveredEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.IMediaReceivers.Discovered" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class MediaReceiverDiscoveredEventArgs : EventArgs
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[MediaReceiverDiscoveredEventArgs](DotNetBrowser.Cast.Events.md#DotNetBrowser_Cast_Events_MediaReceiverDiscoveredEventArgs)

##### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Cast_Events_MediaReceiverDiscoveredEventArgs_MediaReceiver"></a> MediaReceiver

Gets the discovered receiver.

```csharp
public IMediaReceiver MediaReceiver { get; }
```

##### Property Value

 [IMediaReceiver](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceiver)

#### <a id="DotNetBrowser_Cast_Events_MediaReceiverDiscoveredEventArgs_MediaReceivers"></a> MediaReceivers

Gets the <xref href="DotNetBrowser.Cast.IMediaReceivers" data-throw-if-not-resolved="false"></xref> instance initiated this event.

```csharp
public IMediaReceivers MediaReceivers { get; }
```

##### Property Value

 [IMediaReceivers](DotNetBrowser.Cast.md#DotNetBrowser_Cast_IMediaReceivers)
