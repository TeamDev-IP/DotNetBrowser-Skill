# <a id="DotNetBrowser_Cast_IMediaReceiver"></a> Interface IMediaReceiver

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A media receiver to which media content can be cast.

<p>
    Usually, a media receiver is a device that supports the ChromeCast technology,
    but in Chromium's logic it can be even a wired display (HDMI, DVI, or similar).
</p>

```csharp
public interface IMediaReceiver
```

## Properties

### <a id="DotNetBrowser_Cast_IMediaReceiver_Name"></a> Name

Gets the name of the receiver.

```csharp
string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Cast_IMediaReceiver_State"></a> State

Gets the current state of the receiver.

```csharp
MediaReceiverState State { get; }
```

#### Property Value

 [MediaReceiverState](DotNetBrowser.Cast.MediaReceiverState.md)

## Methods

### <a id="DotNetBrowser_Cast_IMediaReceiver_Supports_DotNetBrowser_Cast_CastMode_DotNetBrowser_Cast_PresentationRequest_"></a> Supports\(CastMode, PresentationRequest\)

Checks if the receiver supports casting of <xref href="DotNetBrowser.Cast.CastMode" data-throw-if-not-resolved="false"></xref>.

```csharp
bool Supports(CastMode castMode, PresentationRequest presentationRequest = null)
```

#### Parameters

`castMode` [CastMode](DotNetBrowser.Cast.CastMode.md)

The parameter of the types of content that can be cast to a media receiver.

`presentationRequest` [PresentationRequest](DotNetBrowser.Cast.PresentationRequest.md)

The parameter of the JavaScript PresentationRequest.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the receiver supports casting of <xref href="DotNetBrowser.Cast.CastMode" data-throw-if-not-resolved="false"></xref>, <code>false</code> otherwise.

#### Remarks

<p>
    The <xref href="DotNetBrowser.Cast.PresentationRequest" data-throw-if-not-resolved="false"></xref> parameter should be set only for the
    <xref href="DotNetBrowser.Cast.CastMode.Presentation" data-throw-if-not-resolved="false"></xref> mode.
</p>

### <a id="DotNetBrowser_Cast_IMediaReceiver_Disconnected"></a> Disconnected

Occurs when the receiver disconnected and is not observable by Chromium anymore.

```csharp
event EventHandler<MediaReceiverDisconnectedEventArgs> Disconnected
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[MediaReceiverDisconnectedEventArgs](DotNetBrowser.Cast.Events.MediaReceiverDisconnectedEventArgs.md)\>

