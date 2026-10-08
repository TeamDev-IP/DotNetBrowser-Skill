# <a id="DotNetBrowser_Cast_IMediaCasting"></a> Interface IMediaCasting

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

A service that provides access to all the required media casting services.

```csharp
public interface IMediaCasting
```

## Properties

### <a id="DotNetBrowser_Cast_IMediaCasting_CastSessions"></a> CastSessions

Gets the service that allows observing alive cast sessions.

```csharp
ICastSessions CastSessions { get; }
```

#### Property Value

 [ICastSessions](DotNetBrowser.Cast.ICastSessions.md)

### <a id="DotNetBrowser_Cast_IMediaCasting_Receivers"></a> Receivers

Gets the service that allows observing media receivers.

```csharp
IMediaReceivers Receivers { get; }
```

#### Property Value

 [IMediaReceivers](DotNetBrowser.Cast.IMediaReceivers.md)

### <a id="DotNetBrowser_Cast_IMediaCasting_Screens"></a> Screens

Gets the service that allows obtaining connected screens for casting.

```csharp
IScreens Screens { get; }
```

#### Property Value

 [IScreens](DotNetBrowser.Cast.IScreens.md)

