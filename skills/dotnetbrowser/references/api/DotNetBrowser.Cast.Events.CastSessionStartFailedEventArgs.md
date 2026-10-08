# <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs"></a> Class CastSessionStartFailedEventArgs

Namespace: [DotNetBrowser.Cast.Events](DotNetBrowser.Cast.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Cast.ICastSessions.StartFailed" data-throw-if-not-resolved="false"></xref> event.

```csharp
public sealed class CastSessionStartFailedEventArgs : BrowserEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[BrowserEventArgs](DotNetBrowser.Browser.Events.BrowserEventArgs.md) ← 
[CastSessionStartFailedEventArgs](DotNetBrowser.Cast.Events.CastSessionStartFailedEventArgs.md)

#### Inherited Members

[BrowserEventArgs.Browser](DotNetBrowser.Browser.Events.BrowserEventArgs.md\#DotNetBrowser\_Browser\_Events\_BrowserEventArgs\_Browser), 
[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_CastSessions"></a> CastSessions

Gets the <xref href="DotNetBrowser.Cast.ICastSessions" data-throw-if-not-resolved="false"></xref> instance initiated this event.

```csharp
public ICastSessions CastSessions { get; }
```

#### Property Value

 [ICastSessions](DotNetBrowser.Cast.ICastSessions.md)

### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_Code"></a> Code

Gets the error code obtained from Chromium.

```csharp
public ResultCode Code { get; }
```

#### Property Value

 [ResultCode](DotNetBrowser.Cast.ResultCode.md)

### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_ErrorMessage"></a> ErrorMessage

Gets the error message obtained from Chromium.

```csharp
public string ErrorMessage { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_MediaReceiver"></a> MediaReceiver

Gets the media receiver of the failed cast session.

```csharp
public IMediaReceiver MediaReceiver { get; }
```

#### Property Value

 [IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)

### <a id="DotNetBrowser_Cast_Events_CastSessionStartFailedEventArgs_Mode"></a> Mode

Gets the mode of the requested cast session.

```csharp
public CastMode Mode { get; }
```

#### Property Value

 [CastMode](DotNetBrowser.Cast.CastMode.md)

