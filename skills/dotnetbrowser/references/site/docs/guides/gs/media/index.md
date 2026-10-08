
# Media

**Lead**
This guide gives an overview of the supported video and audio formats, describes how to control audio, get information about available web cameras and microphones, and other features.


## Codecs

Google Chrome and Chromium [differ](https://chromium.googlesource.com/chromium/src/+/master/docs/chromium_browser_vs_google_chrome.md) in several ways, including the sets of audio and video codecs they support.

The table below displays which codecs are supported by the codebase of corresponding browsers.

 |         | **Chromium** | **Google Chrome** |
 |---------|:------------:|:-----------------:|
 | AAC     |     no       |        yes        |
 | AV1     |     yes      |        yes        |
 | FLAC    |     yes      |        yes        |
 | H.264   |     no       |        yes        |
 | HEVC    |     no       |        yes        |
 | MP3     |     yes      |        yes        |
 | Opus    |     yes      |        yes        |
 | Theora  |     yes      |        yes        |
 | Vorbis  |     yes      |        yes        |
 | VP8     |     yes      |        yes        |
 | VP9     |     yes      |        yes        |
 | WAV     |     yes      |        yes        |

As you can see in the table above, Google Chrome supports certain codecs while Chromium does not. The reason is that these codecs are proprietary and cannot be used in an open-source or a commercial project without obtaining licenses from the corresponding patent holders.

Different codecs have different patent holders. For example, to use H.264, companies must acquire the license from Via LA company.

### Proprietary codecs

Patent holders do not license codecs to the software that represents only a part of the final product deployed to the end users, for example, libraries like DotNetBrowser.

To support H.264, HEVC and AAC in your products, you need to purchase appropriate licenses and enable the following proprietary features:


**C#**
```csharp
engine = EngineFactory.Create(new EngineOptions.Builder
{
    RenderingMode = RenderingMode.HardwareAccelerated,
    ProprietaryFeatures = ProprietaryFeatures.H264 |
                          ProprietaryFeatures.Aac |
                          ProprietaryFeatures.Hevc
}.Build());
```

**VB**
```vb
engine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .RenderingMode = RenderingMode.HardwareAccelerated,
    .ProprietaryFeatures = ProprietaryFeatures.H264 Or
                           ProprietaryFeatures.Aac Or
                           ProprietaryFeatures.Hevc
}.Build())
```



After providing the license information and enabling proprietary features, you can load web pages with the AAC, H.264 and HEVC formats, and play audio and video files, just like in Google Chrome. By default, the proprietary codecs are disabled.

**Note**
The H.264, HEVC and AAC codecs are the proprietary components. By enabling these codecs you state that you are aware that H.264, HEVC and AAC are the proprietary components, and you should have a license in order to use them. For more information, you could contact the patent holders: Via Licensing and MPEG LA. TeamDev shall not be responsible for your use of the H.264, HEVC and AAC codecs.



## Video

DotNetBrowser fully supports HTML5 `<video>` element and can play video in the [supported formats](#codecs).

If the library cannot play a video, or a video format is unsupported, DotNetBrowser suggests to download the video file. For details, refer to [Downloads](https://teamdev.com/dotnetbrowser/docs/guides/gs/downloads/) section containing the instructions on managing downloads.

![HTML5 Video](https://teamdev.com/dotnetbrowser/img/articles/guides/media/html5-video.webp)

## Audio
### Controlling audio

Using `IAudioController` you can find out whether audio is playing on the loaded web page:


**C#**
```csharp
bool audioPlaying = browser.Audio.IsPlaying;
```

**VB**
```vb
Dim audioPlaying As Boolean = browser.Audio.IsPlaying
```



You can mute or unmute audio on the loaded web page if required:


**C#**
```csharp
browser.Audio.Muted = true;
browser.Audio.Muted = false;
```

**VB**
```vb
browser.Audio.Muted = True
browser.Audio.Muted = False
```



To check whether audio is muted, use the following code:


**C#**
```csharp
bool audioMuted = browser.Audio.Muted;
```

**VB**
```vb
Dim audioMuted As Boolean = browser.Audio.Muted
```



### Audio events

To find out whether audio has started/stopped playing on the loaded web page, you can subscribe to the following events:


**C#**
```csharp
browser.Audio.AudioPlaybackStarted += (s, e) => { };
browser.Audio.AudioPlaybackStopped += (s, e) => { };
```

**VB**
```vb
AddHandler browser.Audio.AudioPlaybackStarted, Sub(s, e)
End Sub
AddHandler browser.Audio.AudioPlaybackStopped, Sub(s, e)
End Sub
```



## DRM
### Widevine

The web services like Netflix or Amazon Prime use [Widevine](https://www.widevine.com/) to distribute their DRM-encoded content. Widevine is a Google proprietary component and is disabled by default. To enable it and play the DRM-encoded content, use the code sample below:


**C#**
```csharp
var status = await engine.Widevine.Activate();
```

**VB**
```vb
Dim status = engine.Widevine.Activate().Result
```



The status will indicate whether the Widevine component was activated successfully.

**Note**
Widevine is a Google proprietary component, governed by its own terms of use. For more information, refer to [Widevine](https://www.widevine.com/).


On Linux, you must specify a [custom user data directory](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#user-data-directory) to activate Widevine. It is required due to the way Widevine is implemented on Linux. When the component is activated for the first time, or it is updated to the latest version during activation, the engine must be restarted to apply the changes. To find out if the restart is required, check the activation status.

Here is an example of how to specify a custom user data directory and restart the engine if it is required:


**C#**
```csharp
var options = new EngineOptions.Builder()
{
    // Specify a custom user data directory.
    UserDataDirectory = "path/to/user/data/dir"
}.Build();
var engine = EngineFactory.Create(options);
// Activate Widevine and restart the engine if necessary.
var status = engine.Widevine.Activate().Result;
if (status == WidevineActivationStatus.RestartRequired)
{
    // Restart the engine with the same options.
    engine.Dispose();
    engine = EngineFactory.Create(options);
}
var browser = engine.Profiles.Default.CreateBrowser();
```

**VB**
```vb
Dim options = New EngineOptions.Builder With 
{
    .UserDataDirectory = "path/to/user/data/dir"
}.Build()
Dim engine = EngineFactory.Create(options)
Dim status = engine.Widevine.Activate().Result
If status = WidevineActivationStatus.RestartRequired Then
    ' Restart the engine with the same options.
    engine.Dispose()
    engine = EngineFactory.Create(options)
End If
Dim browser = engine.Profiles.Default.CreateBrowser()
```



## Camera & microphone

DotNetBrowser supports a web camera and microphone. You can get information about all available media stream devices using the code sample below:


**C#**
```csharp
IMediaDevices mediaDevices = engine.MediaDevices;

// Get all available video devices, e.g. web camera.
IEnumerable<MediaDevice> videoDevices = mediaDevices.VideoCaptureDevices;

// Get all available audio devices, e.g. microphone.
IEnumerable<MediaDevice> audioDevices = mediaDevices.AudioCaptureDevices;
```

**VB**
```vb
Dim mediaDevices As IMediaDevices = engine.MediaDevices

' Get all available video devices, e.g. web camera.
Dim videoDevices As IEnumerable(Of MediaDevice) = mediaDevices.VideoCaptureDevices

' Get all available audio devices, e.g. microphone.
Dim audioDevices As IEnumerable(Of MediaDevice) = mediaDevices.AudioCaptureDevices
```



You can detect when media capturing starts or stops using these events:


**C#**
```csharp
Browser.MediaStreamCaptureStarted += (sender, args) =>
{
    Console.WriteLine($"Started capturing {args.MediaStreamType}"); 
};

Browser.MediaStreamCaptureStopped += (sender, args) =>
{
    Console.WriteLine($"Stopped capturing {args.MediaStreamType}");  
};
```

**VB**
```vb
AddHandler Browser.MediaStreamCaptureStarted, Sub(sender, args)
    Console.WriteLine($"Started capturing {args.MediaStreamType}")
End Sub

AddHandler Browser.MediaStreamCaptureStopped, Sub(sender, args)
    Console.WriteLine($"Stopped capturing {args.MediaStreamType}")
End Sub
```



## Selecting a media device

You can have multiple webcams and microphones in your environment. When a web page 
wants to use one of them, you can use `SelectMediaDeviceHandler` to instruct the web page on which device to use.

The code sample below demonstrates how to select the first device from the list of available ones:


**C#**
```csharp
mediaDevices.SelectMediaDeviceHandler = 
    new Handler<SelectMediaDeviceParameters, SelectMediaDeviceResponse>(p =>
    {
        return SelectMediaDeviceResponse.Select(p.Devices.FirstOrDefault());
    });
```

**VB**
```vb
mediaDevices.SelectMediaDeviceHandler = 
    New Handler(Of SelectMediaDeviceParameters, SelectMediaDeviceResponse)(Function(p)
        Return SelectMediaDeviceResponse.Select(p.Devices.FirstOrDefault())
    End Function)
```



**Note**
The handler **will not be invoked** if there are no media input devices of the requested type.


If you want to restrict the access to your microphone or webcam for a particular webpage, you can use `RequestPermissionHandler` as shown in the code sample below:


**C#**
```csharp
engine.Profiles.Default.Permissions.RequestPermissionHandler = 
    new Handler<RequestPermissionParameters, RequestPermissionResponse>(p => 
    {
        if (p.Type == PermissionType.AudioCapture || p.Type == PermissionType.VideoCapture)
        {
            return RequestPermissionResponse.Deny();
        }
        return RequestPermissionResponse.Grant();
    });
```

**VB**
```vb
engine.Profiles.Default.Permissions.RequestPermissionHandler =
    New Handler(Of RequestPermissionParameters, RequestPermissionResponse)(Function(p)
        Dim type = p.Type
        If type = PermissionType.AudioCapture OrElse type = PermissionType.VideoCapture Then
            Return RequestPermissionResponse.Deny()
        End If
        Return RequestPermissionResponse.Grant()
    End Function)
```



## Casting

Chromium has built-in functionality that allows casting media content to devices supporting different wireless
technologies such as Chromecast, Miracast, DLNA, AirPlay, or similar. It can be smart TVs, projectors, and other
devices.

![The Cast Diagram](https://teamdev.com/dotnetbrowser/img/articles/guides/media/cast-diagram.webp)

### Preliminary step

By default, we disable Chromium from scanning your network for media devices. To enable it and let Chromium find the
potential receivers, use the engine option:


**C#**
```csharp
EngineOptions options = new EngineOptions.Builder
{
    MediaRoutingEnabled = true
}.Build();
IEngine engine = EngineFactory.Create(options);
```

**VB**
```vb
Dim options As EngineOptions = New EngineOptions.Builder With 
        {
            .MediaRoutingEnabled = True
        }.Build()
Dim engine As IEngine = EngineFactory.Create(options)
```



### Media receivers

To start casting media content to a receiver, you need to get one. For this purpose, DotNetBrowser provides a separate
profile service `IMediaReceivers` which can be obtained this way:


**C#**
```csharp
IMediaReceivers mediaReceivers = profile.MediaCasting.Receivers;
```

**VB**
```vb
Dim mediaReceivers As IMediaReceivers = profile.MediaCasting.Receivers
```



To understand when a new receiver has been discovered, DotNetBrowser provides the `IMediaReceivers.Discovered` event:


**C#**
```csharp
IMediaReceivers mediaReceivers = profile.MediaCasting.Receivers;
mediaReceivers.Discovered += (sender, args) =>
{
    IMediaReceiver receiver = args.MediaReceiver;
};
```

**VB**
```vb
Dim mediaReceivers As IMediaReceivers = profile.MediaCasting.Receivers
AddHandler mediaReceivers.Discovered, Sub(sender, args)
    Dim receiver As IMediaReceiver = args.MediaReceiver
End Sub
```



For your convenience, DotNetBrowser keeps track of the discovered receivers. If you want to get the list of currently
discovered media receivers, use the `IMediaReceivers.AllAvailable` property:


**C#**
```csharp
IMediaReceivers mediaReceivers = profile.MediaCasting.Receivers;
IReadOnlyList<IMediaReceiver> availableReceivers = mediaReceivers.AllAvailable;
```

**VB**
```vb
Dim mediaReceivers As IMediaReceivers = profile.MediaCasting.Receivers
Dim availableReceivers As IReadOnlyList(Of IMediaReceiver) = mediaReceivers.AllAvailable
```



If you look for a specific receiver, you can obtain it via the `IMediaReceivers.RetrieveAsync(Predicate<IMediaReceiver>)`
convenience method. It executes asynchronously until the first receiver matching the predicate is discovered and returns it.


**C#**
```csharp
IMediaReceivers mediaReceivers = profile.MediaCasting.Receivers;
IMediaReceiver receiver =
        await mediaReceivers.RetrieveAsync(it => it.Name.Equals("Samsung"));
```

**VB**
```vb
Dim mediaReceivers As IMediaReceivers = profile.MediaCasting.Receivers
Dim receiver As IMediaReceiver =
        Await mediaReceivers.RetrieveAsync(Function(it) it.Name.Equals("Samsung"))
```



To detect that the media receiver has been disconnected, i.e. unplugged or disconnected from the network, use
the `IMediaReceiver.Disconnected` event:


**C#**
```csharp
receiver.Disconnected += (sender, args) =>
{
    IMediaReceiver mediaReceiver = args.MediaReceiver;
};
```

**VB**
```vb
AddHandler receiver.Disconnected, Sub(sender, args)
    Dim mediaReceiver As IMediaReceiver = args.MediaReceiver
End Sub
```



### Casting content

DotNetBrowser API allows casting content of browsers, screens and presentation using the JavaScript Presentation API.

**Note**
Media receivers can support different media sources. A media source represents a type of content 
that can be cast to a media receiver. Before you start casting, please make sure that the selected media receiver 
supports the corresponding media source.


#### Casting browser content

To start casting browser content, use the `IBrowser.Cast.CastContent(IMediaReceiver)` method:


**C#**
```csharp
IMediaReceiver receiver =
        await mediaReceivers.RetrieveAsync(it => it.Name.Contains("Samsung"));
if (receiver.Supports(CastMode.Browser))
{
    ICastSession castSession = await browser.Cast.CastContent(receiver);
}
```

**VB**
```vb
Dim receiver As IMediaReceiver =
        Await mediaReceivers.RetrieveAsync(Function(it) it.Name.Contains("Samsung"))
If receiver.Supports(CastMode.Browser) Then
    Dim castSession As ICastSession = Await browser.Cast.CastContent(receiver)
End If

```



Each session of casting media content to a media receiver is represented by the instance of `ICastSession`.

##### Default presentation request

If the web page contains the
[default `PresentationRequest`](https://developer.mozilla.org/en-US/docs/Web/API/Presentation/defaultRequest), 
the browser starts casting the content specified in this request instead of the browser's content.

To check if the browser contains the default `PresentationRequest`, use:


**C#**
```csharp
IMediaReceiver receiver =
        await mediaReceivers.RetrieveAsync(it => it.Name.Contains("Samsung"));
PresentationRequest presentationRequest = browser.Cast.DefaultPresentationRequest();
if (receiver.Supports(CastMode.Presentation, presentationRequest))
{
    ICastSession castSession = await browser.Cast.CastContent(receiver);
}
```

**VB**
```vb
Dim receiver As IMediaReceiver =
        Await mediaReceivers.RetrieveAsync(Function(it) it.Name.Contains("Samsung"))
Dim presentationRequest As PresentationRequest = browser.Cast.DefaultPresentationRequest()
If receiver.Supports(CastMode.Presentation, presentationRequest) Then
    Dim castSession As ICastSession = Await browser.Cast.CastContent(receiver)
End If

```



#### Casting a screen

To start casting the screen content, use `IBrowser.Cast.CastScreen(IMediaReceiver)`. This method will show a standard Chromium
dialog for picking the screen to cast.


**C#**
```csharp
IMediaReceiver receiver =
        await mediaReceivers.RetrieveAsync(it => it.Name.Contains("Samsung"));
if (receiver.Supports(CastMode.Screen))
{
    ICastSession castSession = await browser.Cast.CastScreen(receiver);
}
 ```

**VB**
```vb
Dim receiver As IMediaReceiver =
        Await mediaReceivers.RetrieveAsync(Function(it) it.Name.Contains("Samsung"))
If receiver.Supports(CastMode.Screen) Then
    Dim castSession As ICastSession = Await browser.Cast.CastScreen(receiver)
End If

```



If you want to select the screen programmatically, use the `IBrowser.Cast.CastScreen(IMediaReceiver,
ScreenCastOptions)` method. Find the screen you need using the `IScreens` service:


**C#**
```csharp
IMediaReceiver receiver =
        await mediaReceivers.RetrieveAsync(it => it.Name.Contains("Samsung"));
Screen screen = profile.MediaCasting.Screens.DefaultScreen;
ScreenCastOptions options = new ScreenCastOptions()
{
    Screen = screen,
    AudioMode = AudioMode.Cast
};
if (receiver.Supports(CastMode.Screen))
{
    ICastSession castSession = await browser.Cast.CastScreen(receiver, options);
}
```

**VB**
```vb
Dim receiver As IMediaReceiver =
        Await mediaReceivers.RetrieveAsync(Function(it) it.Name.Contains("Samsung"))
Dim screen As Screen = profile.MediaCasting.Screens.DefaultScreen
Dim options As New ScreenCastOptions() With {
        .Screen = screen,
        .AudioMode = AudioMode.Cast
        }
If receiver.Supports(CastMode.Screen) Then
    Dim castSession As ICastSession = Await browser.Cast.CastScreen(receiver, options)
End If
```



**Note**
For now, Chromium supports audio casting only on Windows. So enabling it on macOS/Linux via 
`ScreenCastOptions.AudioMode.Cast` is a no-op. On Windows, when selecting the screen in the picker dialog, 
Chromium provides a separate checkbox for selecting audio-casting.


#### Presentation API

DotNetBrowser allows working with
[JavaScript Presentation API](https://developer.mozilla.org/en-US/docs/Web/API/Presentation_API).

When the [`PresentationRequest.start()`](https://developer.mozilla.org/en-US/docs/Web/API/PresentationRequest/start)
method is called on the JavaScript side, DotNetBrowser invokes `StartPresentationHandler` where you can decide to start or
cancel the presentation.

To start the presentation to a receiver, use the `StartPresentationResponse.Start(IMediaReceiver)` method:


**C#**
```csharp
browser.Cast.StartPresentationHandler =
    new AsyncHandler<StartPresentationParameters, StartPresentationResponse>(async p =>
{
    IMediaReceiver receiver =
            await mediaReceivers.RetrieveAsync(it => it.Name.Contains("Samsung"));
    if (receiver.Supports(CastMode.Presentation, p.PresentationRequest))
    {
        return StartPresentationResponse.Start(receiver);
    }
    else
    {
        return StartPresentationResponse.Cancel();
    }
});
```

**VB**
```vb
browser.Cast.StartPresentationHandler =
    New AsyncHandler(Of StartPresentationParameters,
                        StartPresentationResponse)(Async Function(p)

    Dim receiver As IMediaReceiver = 
            Await mediaReceivers.RetrieveAsync(Function(it) it.Name.Contains("Samsung"))
    If receiver.Supports(CastMode.Presentation, p.PresentationRequest) Then
        Return StartPresentationResponse.Start(receiver)
    Else
        Return StartPresentationResponse.Cancel()
    End If
End Function)
```



#### Discovering cast sessions

To get notified when a cast session has been discovered, DotNetBrowser provides the `ICastSessions.Discovered` event:


**C#**
```csharp
profile.MediaCasting.CastSessions.Discovered += (o, args) =>
{
    ICastSession castSession = args.CastSession;
};
```

**VB**
```vb
AddHandler profile.MediaCasting.CastSessions.Discovered, Sub(o, args)
    Dim castSession As ICastSession = args.CastSession
End Sub

```



**Note**
Chromium can discover sessions started by other applications or instances of Chromium. To indicate that 
the cast session has been started by this profile, DotNetBrowser provides the `ICastSession.IsLocal` property. So if a cast 
session is started by another profile or even another Chromium process the property will return `false`.


#### Stopping сast sessions

To stop a cast session, use the `ICastSession.Stop()` method. If you want to get notified when a cast session has been
stopped, use the `ICastSession.Stopped` event:


**C#**
```csharp
ICastSession session = profile.MediaCasting.CastSessions.AllAlive.FirstOrDefault();
session.Stopped += (o, args) =>
{
    // Do something
};
...
session.Stop();
```

**VB**
```vb
Dim session As ICastSession = profile.MediaCasting.CastSessions.AllAlive.FirstOrDefault()
AddHandler session.Stopped, Sub(o, args)
    ' Do something
End Sub
...
session.Stop()
```



**Note**
Session can be stopped by other applications or instances of Chromium, i.e. Google Chrome. In this case, 
the event will be invoked as well.


#### Failures

Sometimes, Chromium may fail to start a new cast session, i.e. if the media receiver is not found or had
suddenly disconnected. To detect that, use the `ICastSessions.StartFailed` event:


**C#**
```csharp
IMediaReceiver receiver =
        await mediaReceivers.RetrieveAsync(it => it.Name.Contains("Samsung"));
profile.MediaCasting.CastSessions.StartFailed += (o, args) =>
{
    string errorMessage = args.ErrorMessage;
};

ICastSession castSession = await browser.Cast.CastContent(receiver);
```

**VB**
```vb
Dim receiver As IMediaReceiver =
        Await mediaReceivers.RetrieveAsync(Function(it) it.Name.Contains("Samsung"))
AddHandler profile.MediaCasting.CastSessions.StartFailed, Sub(o, args)
    Dim errorMessage As String = args.ErrorMessage
End Sub

Dim castSession As ICastSession = Await browser.Cast.CastContent(receiver)

```



**Note**
This is intentionally an event due to asynchronous nature of media casting.


Since `Browser.Cast.CastXxx()` methods return `Task<ICastSession>`, you can detect that the start of the cast session
has failed. In this case, DotNetBrowser throws the `CastSessionStartFailedException`:


**C#**
```csharp
try
{
    ICastSession castSession = await browser.Cast.CastContent(receiver);
}
catch (CastSessionStartFailedException ex)
{
    string errorMessage = ex.Message;
}
```

**VB**
```vb
Try
    Dim castSession As ICastSession = Await browser.Cast.CastContent(receiver)
Catch ex As CastSessionStartFailedException
    Dim errorMessage As String = ex.Message
End Try

```


