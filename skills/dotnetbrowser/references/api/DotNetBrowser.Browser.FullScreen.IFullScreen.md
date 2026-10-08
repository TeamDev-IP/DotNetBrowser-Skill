# <a id="DotNetBrowser_Browser_FullScreen_IFullScreen"></a> Interface IFullScreen

Namespace: [DotNetBrowser.Browser.FullScreen](DotNetBrowser.Browser.FullScreen.md)  
Assembly: DotNetBrowser.dll  

A service that is used for controlling the browser's fullscreen mode.

```csharp
public interface IFullScreen : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Methods

### <a id="DotNetBrowser_Browser_FullScreen_IFullScreen_Exit"></a> Exit\(\)

Tells the browser to exit fullscreen mode.

```csharp
void Exit()
```

#### Remarks

This method iterates over the frames in the browser and exits fullscreen mode
for each of them. This also includes internal frames of the PDF viewer
that are not accessible through the public API. If there is no element being presented
in fullscreen mode, this method does nothing.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_FullScreen_IFullScreen_Entered"></a> Entered

Occurs when the browser instance has been toggled into full-screen mode.

```csharp
event EventHandler<FullScreenEnteredEventArgs> Entered
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FullScreenEnteredEventArgs](DotNetBrowser.Browser.FullScreen.Events.FullScreenEnteredEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_FullScreen_IFullScreen_Exited"></a> Exited

Occurs when the browser instance has been toggled out of full-screen mode.

```csharp
event EventHandler<FullScreenExitedEventArgs> Exited
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FullScreenExitedEventArgs](DotNetBrowser.Browser.FullScreen.Events.FullScreenExitedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

