# DotNetBrowser API index

DotNetBrowser 4.3.3, generated 2026-10-08. 587 types in 93 namespaces. Every file in this directory is one public type with all of its members. Find the type below and open the file from the last column; the namespace page lists the same types with their summaries.

## DotNetBrowser

Namespace page: DotNetBrowser.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IAutoDisposable` | Represents the object which can be disposed by itself (without the explicit Dispose method call). | DotNetBrowser.IAutoDisposable.md |
| `IAutoDisposable<TArgs>` | Represents the object which can be disposed by itself (without the explicit Dispose method call). | DotNetBrowser.IAutoDisposable-1.md |

## DotNetBrowser.AvaloniaUi

Namespace page: DotNetBrowser.AvaloniaUi.md

### Classes

| Type | Summary | File |
|---|---|---|
| `BitmapExtensions` | Extensions for `Bitmap` class. | DotNetBrowser.AvaloniaUi.BitmapExtensions.md |
| `BrowserView` | The Avalonia-based implementation of a browser view. | DotNetBrowser.AvaloniaUi.BrowserView.md |

## DotNetBrowser.AvaloniaUi.Dialogs

Namespace page: DotNetBrowser.AvaloniaUi.Dialogs.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DefaultAuthenticationHandler` | Default Avalonia UI authentication handler, which displays an authentication dialog. | DotNetBrowser.AvaloniaUi.Dialogs.DefaultAuthenticationHandler.md |
| `DialogHandlerBase` | The base class for all dialog handlers. | DotNetBrowser.AvaloniaUi.Dialogs.DialogHandlerBase.md |

## DotNetBrowser.AvaloniaUi.Extensions

Namespace page: DotNetBrowser.AvaloniaUi.Extensions.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DefaultOpenExtensionActionPopupHandler` | The default implementation of the `IHandler` interface that opens a popup window with the specified `IBrowser` instance. | DotNetBrowser.AvaloniaUi.Extensions.DefaultOpenExtensionActionPopupHandler.md |
| `DefaultOpenExtensionPopupHandler` | Default extension popup handler, which displays an extension popup as a separate window. | DotNetBrowser.AvaloniaUi.Extensions.DefaultOpenExtensionPopupHandler.md |

## DotNetBrowser.Browser

Namespace page: DotNetBrowser.Browser.md

### Classes

| Type | Summary | File |
|---|---|---|
| `BitmapTimeoutException` | Thrown when a bitmap request times out. | DotNetBrowser.Browser.BitmapTimeoutException.md |
| `BrowserDisposeOptions` | The dispose options of the browser. | DotNetBrowser.Browser.BrowserDisposeOptions.md |
| `BrowserViewExtensions` | Extension methods for `IBrowserView` interface. | DotNetBrowser.Browser.BrowserViewExtensions.md |
| `CspParameters` | The parameters describing the particular key container within a particular cryptographic service provider (CSP). | DotNetBrowser.Browser.CspParameters.md |
| `UserAgentBrandVersion` | Contains the brand name and version type. | DotNetBrowser.Browser.UserAgentBrandVersion.md |
| `UserAgentBrandVersion.Builder` | A builder class to construct `UserAgentBrandVersion`. | DotNetBrowser.Browser.UserAgentBrandVersion.Builder.md |
| `UserAgentMetadata` | Contains the client hints data. | DotNetBrowser.Browser.UserAgentMetadata.md |
| `UserAgentMetadata.Builder` | A builder class to construct `UserAgentMetadata`. | DotNetBrowser.Browser.UserAgentMetadata.Builder.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IBrowser` | A web browser control that allows loading a web page or a local HTML file, accessing DOM and executing JavaScript on the loaded web page, getting notifications about loading progress, dispatching k... | DotNetBrowser.Browser.IBrowser.md |
| `IBrowserSettings` | The settings of the browser. | DotNetBrowser.Browser.IBrowserSettings.md |
| `IBrowserView` | The interface that is implemented by UI components which are able to display the browser. | DotNetBrowser.Browser.IBrowserView.md |
| `IDefaultFonts` | The default fonts used by a browser. | DotNetBrowser.Browser.IDefaultFonts.md |
| `IOffScreenRenderProvider` | Provides access to an image rendered by the browser that works in the off-screen rendering mode. | DotNetBrowser.Browser.IOffScreenRenderProvider.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `PreferredColorScheme` | The preferred color scheme for the web content in the browser. | DotNetBrowser.Browser.PreferredColorScheme.md |
| `SavePageType` | Determines how the web page will be saved. | DotNetBrowser.Browser.SavePageType.md |
| `WebRtcIpHandlingPolicy` | The media performance/privacy tradeoffs which affect how WebRTC traffic will be routed and how much local address information will be exposed. | DotNetBrowser.Browser.WebRtcIpHandlingPolicy.md |

## DotNetBrowser.Browser.Dialogs

Namespace page: DotNetBrowser.Browser.Dialogs.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IDialogs` | The browser dialogs. | DotNetBrowser.Browser.Dialogs.IDialogs.md |
| `IJsDialogs` | The JavaScript dialogs. | DotNetBrowser.Browser.Dialogs.IJsDialogs.md |

## DotNetBrowser.Browser.Dialogs.Handlers

Namespace page: DotNetBrowser.Browser.Dialogs.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `AlertParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.AlertParameters.md |
| `BeforeUnloadParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadParameters.md |
| `BeforeUnloadResponse` | The response to the `BeforeUnloadHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.md |
| `CommonDialogParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.CommonDialogParameters.md |
| `ConfirmParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.ConfirmParameters.md |
| `ConfirmResponse` | The response to the `ConfirmHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse.md |
| `DialogParameters` | The base class for dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.DialogParameters.md |
| `FileChooserParameters` | The base class for the common file chooser parameters. | DotNetBrowser.Browser.Dialogs.Handlers.FileChooserParameters.md |
| `FilteredFileChooserParameters` | The base class for the common file chooser parameters. | DotNetBrowser.Browser.Dialogs.Handlers.FilteredFileChooserParameters.md |
| `OpenDirectoryParameters` | The parameters of the `OpenDirectoryHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryParameters.md |
| `OpenDirectoryResponse` | The response to the `OpenDirectoryHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse.md |
| `OpenExternalAppParameters` | The parameters of the `OpenExternalAppHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppParameters.md |
| `OpenExternalAppResponse` | The response to the `OpenExternalAppHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse.md |
| `OpenFileParameters` | The parameters of the `OpenFileHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.OpenFileParameters.md |
| `OpenFileResponse` | The response to the `OpenFileHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse.md |
| `OpenMultipleFilesParameters` | The parameters of the `OpenMultipleFilesHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesParameters.md |
| `OpenMultipleFilesResponse` | The response to the `OpenMultipleFilesHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse.md |
| `PromptParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.PromptParameters.md |
| `PromptResponse` | The response to the `PromptHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse.md |
| `RepostFormParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.RepostFormParameters.md |
| `RepostFormResponse` | The response to the `RepostFormHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse.md |
| `SaveAsPdfParameters` | The parameters of the `SaveAsPdfHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.SaveAsPdfParameters.md |
| `SaveAsPdfResponse` | The response to the `SaveAsPdfHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.SaveAsPdfResponse.md |
| `SaveFileParameters` | The parameters of the `SaveFileHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.SaveFileParameters.md |
| `SaveFileResponse` | The response to the `SaveFileHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse.md |
| `SelectCertificateParameters` | The parameters of the `SelectCertificateHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateParameters.md |
| `SelectCertificateResponse` | The response to `SelectCertificateHandler` | DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.md |
| `SelectColorParameters` | The parameters for the `SelectColorHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.SelectColorParameters.md |
| `SelectColorResponse` | The response to the `SelectColorHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `BeforeUnloadCause` | Describes the cause of the onbeforeunload dialog. | DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadCause.md |

## DotNetBrowser.Browser.Events

Namespace page: DotNetBrowser.Browser.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `BrowserBecameResponsiveEventArgs` | Event arguments for the `BrowserBecameResponsive` event. | DotNetBrowser.Browser.Events.BrowserBecameResponsiveEventArgs.md |
| `BrowserBecameUnresponsiveEventArgs` | Event arguments for the `BrowserBecameUnresponsive` event. | DotNetBrowser.Browser.Events.BrowserBecameUnresponsiveEventArgs.md |
| `BrowserEventArgs` | The base class for `IBrowser` events. | DotNetBrowser.Browser.Events.BrowserEventArgs.md |
| `ConsoleMessageReceivedEventArgs` | Event arguments for the `ConsoleMessageReceived` event. | DotNetBrowser.Browser.Events.ConsoleMessageReceivedEventArgs.md |
| `CursorChangedEventArgs` | The `CursorChanged` event data which can be used to update the cursor for the off-screen view. | DotNetBrowser.Browser.Events.CursorChangedEventArgs.md |
| `FaviconChangedEventArgs` | Event arguments for the `FaviconChanged` event. | DotNetBrowser.Browser.Events.FaviconChangedEventArgs.md |
| `FocusGainedEventArgs` | Event arguments for the `FocusGained` event. | DotNetBrowser.Browser.Events.FocusGainedEventArgs.md |
| `FocusLostEventArgs` | Event arguments for the `FocusLost` event. | DotNetBrowser.Browser.Events.FocusLostEventArgs.md |
| `FocusRequestedEventArgs` | Event arguments for the `FocusRequested` event. | DotNetBrowser.Browser.Events.FocusRequestedEventArgs.md |
| `FrameCreatedEventArgs` | Event arguments for the `FrameCreated` event. | DotNetBrowser.Browser.Events.FrameCreatedEventArgs.md |
| `FrameDeletedEventArgs` | Event arguments for the `FrameDeleted` event. | DotNetBrowser.Browser.Events.FrameDeletedEventArgs.md |
| `FrameEventArgs` | The base class for `IBrowser` events related to `IFrame`. | DotNetBrowser.Browser.Events.FrameEventArgs.md |
| `MediaStreamCaptureStartedEventArgs` | Event arguments for the `MediaStreamCaptureStarted` | DotNetBrowser.Browser.Events.MediaStreamCaptureStartedEventArgs.md |
| `MediaStreamCaptureStoppedEventArgs` | Event arguments for the `MediaStreamCaptureStopped` | DotNetBrowser.Browser.Events.MediaStreamCaptureStoppedEventArgs.md |
| `MediaStreamEventArgs` | The base class for `IBrowser` events related to media stream events. | DotNetBrowser.Browser.Events.MediaStreamEventArgs.md |
| `PdfDocumentLoadFailedEventArgs` | Event arguments for the `PdfDocumentLoadFailed` event. | DotNetBrowser.Browser.Events.PdfDocumentLoadFailedEventArgs.md |
| `PdfDocumentLoadedEventArgs` | Event arguments for the `PdfDocumentLoaded` event. | DotNetBrowser.Browser.Events.PdfDocumentLoadedEventArgs.md |
| `PrintPreviewClosedEventArgs` | Event arguments for the `PrintPreviewClosed` | DotNetBrowser.Browser.Events.PrintPreviewClosedEventArgs.md |
| `PrintPreviewOpenedEventArgs` | Event arguments for the `PrintPreviewOpened` | DotNetBrowser.Browser.Events.PrintPreviewOpenedEventArgs.md |
| `RenderProcessTerminatedEventArgs` | Event arguments for the `RenderProcessTerminated` event. | DotNetBrowser.Browser.Events.RenderProcessTerminatedEventArgs.md |
| `SessionStartedEventArgs` | Event arguments for the `SessionStarted` event. | DotNetBrowser.Browser.Events.SessionStartedEventArgs.md |
| `SpellCheckCompletedEventArgs` | Event arguments for the `SpellCheckCompleted` event. | DotNetBrowser.Browser.Events.SpellCheckCompletedEventArgs.md |
| `StatusChangedEventArgs` | Event arguments for the `StatusChanged` event. | DotNetBrowser.Browser.Events.StatusChangedEventArgs.md |
| `TitleChangedEventArgs` | Event arguments for the `TitleChanged` event. | DotNetBrowser.Browser.Events.TitleChangedEventArgs.md |
| `UpdateBoundsRequestedEventArgs` | Event arguments for the `UpdateBoundsRequested` event. | DotNetBrowser.Browser.Events.UpdateBoundsRequestedEventArgs.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `ConsoleMessageReceivedEventArgs.MessageLevel` | Console message levels. | DotNetBrowser.Browser.Events.ConsoleMessageReceivedEventArgs.MessageLevel.md |
| `MediaStreamType` | The media type of the captured stream. | DotNetBrowser.Browser.Events.MediaStreamType.md |
| `TerminationStatus` | The termination status of the render process. | DotNetBrowser.Browser.Events.TerminationStatus.md |

## DotNetBrowser.Browser.FullScreen

Namespace page: DotNetBrowser.Browser.FullScreen.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IFullScreen` | A service that is used for controlling the browser's fullscreen mode. | DotNetBrowser.Browser.FullScreen.IFullScreen.md |

## DotNetBrowser.Browser.FullScreen.Events

Namespace page: DotNetBrowser.Browser.FullScreen.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `FullScreenEnteredEventArgs` | Event arguments for the `Entered` event. | DotNetBrowser.Browser.FullScreen.Events.FullScreenEnteredEventArgs.md |
| `FullScreenExitedEventArgs` | Event arguments for the `Exited` event. | DotNetBrowser.Browser.FullScreen.Events.FullScreenExitedEventArgs.md |

## DotNetBrowser.Browser.Handlers

Namespace page: DotNetBrowser.Browser.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `BrowserParameters` | The base class for `IBrowser` handlers parameters. | DotNetBrowser.Browser.Handlers.BrowserParameters.md |
| `CreatePopupParameters` | The parameters of the `CreatePopupHandler`. | DotNetBrowser.Browser.Handlers.CreatePopupParameters.md |
| `CreatePopupResponse` | The response to the `CreatePopupHandler`. | DotNetBrowser.Browser.Handlers.CreatePopupResponse.md |
| `FrameParameters` | Represents the parameters of `IBrowser`-related handlers associated with `IFrame`. | DotNetBrowser.Browser.Handlers.FrameParameters.md |
| `InjectCssParameters` | The parameters of the `InjectCssHandler`. | DotNetBrowser.Browser.Handlers.InjectCssParameters.md |
| `InjectCssResponse` | The response to the `InjectCssHandler`. | DotNetBrowser.Browser.Handlers.InjectCssResponse.md |
| `InjectJsParameters` | The parameters of the `InjectJsHandler`. | DotNetBrowser.Browser.Handlers.InjectJsParameters.md |
| `OpenExtensionActionPopupParameters` | The parameters of the `OpenExtensionActionPopupHandler`. | DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters.md |
| `OpenPopupParameters` | The parameters of the `OpenPopupHandler`. | DotNetBrowser.Browser.Handlers.OpenPopupParameters.md |
| `RequestPdfDocumentPasswordParameters` | The parameters of the `RequestPdfDocumentPasswordHandler`. | DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordParameters.md |
| `RequestPdfDocumentPasswordResponse` | The response to the `RequestPdfDocumentPasswordHandler`. | DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.md |
| `RequestPrintParameters` | The parameters of the `RequestPrintHandler`. | DotNetBrowser.Browser.Handlers.RequestPrintParameters.md |
| `RequestPrintResponse` | The response to the `RequestPrintHandler`. | DotNetBrowser.Browser.Handlers.RequestPrintResponse.md |
| `ShowContextMenuParameters` | The parameters of the `ShowContextMenuHandler`. | DotNetBrowser.Browser.Handlers.ShowContextMenuParameters.md |
| `ShowContextMenuResponse` | The response to the `ShowContextMenuHandler`. | DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.md |

## DotNetBrowser.Cache

Namespace page: DotNetBrowser.Cache.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IHttpAuthCache` | An HTTP Authentication cache service. | DotNetBrowser.Cache.IHttpAuthCache.md |
| `IHttpCache` | An HTTP cache service. | DotNetBrowser.Cache.IHttpCache.md |

## DotNetBrowser.Capture

Namespace page: DotNetBrowser.Capture.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Source` | The source for the content capture session. | DotNetBrowser.Capture.Source.md |
| `Sources` | Provides the access to the sources available for content capture. | DotNetBrowser.Capture.Sources.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `ICapture` | A service that can be used for listening and handling capturing sessions. | DotNetBrowser.Capture.ICapture.md |
| `ISession` | A content capture session. | DotNetBrowser.Capture.ISession.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `AudioMode` | The mode of capturing audio during the content capture session. | DotNetBrowser.Capture.AudioMode.md |
| `NotificationVisibility` | Specifies whether the notification about the capture session should be shown or hidden. | DotNetBrowser.Capture.NotificationVisibility.md |
| `SourceType` | The type of the content capture source. | DotNetBrowser.Capture.SourceType.md |

## DotNetBrowser.Capture.Events

Namespace page: DotNetBrowser.Capture.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `SessionStoppedEventArgs` | Event arguments for the `Stopped` event. | DotNetBrowser.Capture.Events.SessionStoppedEventArgs.md |

## DotNetBrowser.Capture.Handlers

Namespace page: DotNetBrowser.Capture.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `StartSessionParameters` | The parameters of the `StartSessionHandler`. | DotNetBrowser.Capture.Handlers.StartSessionParameters.md |
| `StartSessionResponse` | A response to the `StartSessionHandler`. | DotNetBrowser.Capture.Handlers.StartSessionResponse.md |

## DotNetBrowser.Card

Namespace page: DotNetBrowser.Card.md

### Classes

| Type | Summary | File |
|---|---|---|
| `CreditCard` | The credit card information persisted in `ICreditCardStore` the credit card store. | DotNetBrowser.Card.CreditCard.md |
| `CreditCard.Builder` | A builder for creating a new `CreditCard` instance. | DotNetBrowser.Card.CreditCard.Builder.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `ICreditCardStore` | A service that allows working with `CreditCard` credit cards in the Chromium credit cards store. | DotNetBrowser.Card.ICreditCardStore.md |
| `ICreditCards` | A service that allows managing credit cards. | DotNetBrowser.Card.ICreditCards.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `CreditCardNetworkType` | The type of the credit card network. | DotNetBrowser.Card.CreditCardNetworkType.md |

## DotNetBrowser.Card.Handlers

Namespace page: DotNetBrowser.Card.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `SaveCreditCardParameters` | The parameters of the `SaveCreditCardHandler`. | DotNetBrowser.Card.Handlers.SaveCreditCardParameters.md |
| `SaveCreditCardResponse` | A response to the `SaveCreditCardHandler`. | DotNetBrowser.Card.Handlers.SaveCreditCardResponse.md |

## DotNetBrowser.Cast

Namespace page: DotNetBrowser.Cast.md

### Classes

| Type | Summary | File |
|---|---|---|
| `CastSessionStartFailedException` | Thrown when the cast session start has been failed. | DotNetBrowser.Cast.CastSessionStartFailedException.md |
| `MediaRoutingException` | Thrown when the media routing is disabled. | DotNetBrowser.Cast.MediaRoutingException.md |
| `PresentationRequest` | The JavaScript | DotNetBrowser.Cast.PresentationRequest.md |
| `ReceiverDisconnectedException` | Thrown when the receiver has been disconnected. | DotNetBrowser.Cast.ReceiverDisconnectedException.md |
| `ReceiverNotDiscoveredException` | Thrown when the receiver has not been discovered within the specified timeout. | DotNetBrowser.Cast.ReceiverNotDiscoveredException.md |
| `Screen` | The screen whose content can be cast. | DotNetBrowser.Cast.Screen.md |
| `ScreenCastOptions` | Configuration options for screen casting. | DotNetBrowser.Cast.ScreenCastOptions.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `ICast` | A service that provides access for casting media on receivers. | DotNetBrowser.Cast.ICast.md |
| `ICastSession` | A session of casting media content to a media `IMediaReceiver` receiver. | DotNetBrowser.Cast.ICastSession.md |
| `ICastSessions` | A service that allows observing `IsAlive` cast `ICastSession` sessions. | DotNetBrowser.Cast.ICastSessions.md |
| `IMediaCasting` | A service that provides access to all the required media casting services. | DotNetBrowser.Cast.IMediaCasting.md |
| `IMediaReceiver` | A media receiver to which media content can be cast. | DotNetBrowser.Cast.IMediaReceiver.md |
| `IMediaReceivers` | The service that allows observing media `IMediaReceiver` receivers in the environment. | DotNetBrowser.Cast.IMediaReceivers.md |
| `IScreens` | The service that allows obtaining connected screens whose content can be cast. | DotNetBrowser.Cast.IScreens.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `AudioMode` | The audio casting mode for the content cast session. | DotNetBrowser.Cast.AudioMode.md |
| `CastMode` | The types of content that can be cast to a media receiver. | DotNetBrowser.Cast.CastMode.md |
| `MediaReceiverState` | The state of the media receiver. | DotNetBrowser.Cast.MediaReceiverState.md |
| `ResultCode` | Contains the codes indicating the result of creating a cast session. | DotNetBrowser.Cast.ResultCode.md |

## DotNetBrowser.Cast.Events

Namespace page: DotNetBrowser.Cast.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `CastSessionDiscoveredEventArgs` | Event arguments for the `Discovered` event. | DotNetBrowser.Cast.Events.CastSessionDiscoveredEventArgs.md |
| `CastSessionStartFailedEventArgs` | Event arguments for the `StartFailed` event. | DotNetBrowser.Cast.Events.CastSessionStartFailedEventArgs.md |
| `CastSessionStoppedEventArgs` | Event arguments for the `Stopped` event. | DotNetBrowser.Cast.Events.CastSessionStoppedEventArgs.md |
| `MediaReceiverDisconnectedEventArgs` | Event arguments for the `Disconnected` event. | DotNetBrowser.Cast.Events.MediaReceiverDisconnectedEventArgs.md |
| `MediaReceiverDiscoveredEventArgs` | Event arguments for the `Discovered` event. | DotNetBrowser.Cast.Events.MediaReceiverDiscoveredEventArgs.md |

## DotNetBrowser.Cast.Handlers

Namespace page: DotNetBrowser.Cast.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `StartPresentationParameters` | The parameters of the `StartPresentationHandler`. | DotNetBrowser.Cast.Handlers.StartPresentationParameters.md |
| `StartPresentationResponse` | A response to the `StartPresentationHandler`. | DotNetBrowser.Cast.Handlers.StartPresentationResponse.md |

## DotNetBrowser.Chromium

Namespace page: DotNetBrowser.Chromium.md

### Classes

| Type | Summary | File |
|---|---|---|
| `ChromiumBinariesExtractor` | A tool that is used to extract the corresponding Chromium binaries. | DotNetBrowser.Chromium.ChromiumBinariesExtractor.md |
| `ChromiumInfo` | Provides information about the Chromium engine used in DotNetBrowser. | DotNetBrowser.Chromium.ChromiumInfo.md |

## DotNetBrowser.ContextMenu

Namespace page: DotNetBrowser.ContextMenu.md

### Classes

| Type | Summary | File |
|---|---|---|
| `ContextMenuItem` | A custom context menu item. | DotNetBrowser.ContextMenu.ContextMenuItem.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `ContextMenuItemType` | The context menu item types. | DotNetBrowser.ContextMenu.ContextMenuItemType.md |

## DotNetBrowser.Cookies

Namespace page: DotNetBrowser.Cookies.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Cookie` | Represents an HTTP cookie. | DotNetBrowser.Cookies.Cookie.md |
| `Cookie.Builder` | A builder class to construct cookie. | DotNetBrowser.Cookies.Cookie.Builder.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `ICookieStore` | The system for storing and retrieving cookies. The cookies can be stored in the process memory (session cookies) or in files (persistent cookies). The `ICookieStore` instance provides access to bot... | DotNetBrowser.Cookies.ICookieStore.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `SameSite` | The SameSite cookie attribute values of the Set-Cookie HTTP response header. This attribute is used to declare in which context the cookies can be sent. | DotNetBrowser.Cookies.SameSite.md |

## DotNetBrowser.DevTools

Namespace page: DotNetBrowser.DevTools.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IDevTools` | Allows working with Chromium Developer Tools and access the remote debugging URL of the currently loaded web page in the browser instance associated with this DevTools instance. | DotNetBrowser.DevTools.IDevTools.md |

## DotNetBrowser.Dom

Namespace page: DotNetBrowser.Dom.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DomException` | Thrown when an operation on the DOM element fails. | DotNetBrowser.Dom.DomException.md |
| `PointInspection` | Provides information about a DOM node at the specified point inside the loaded document. | DotNetBrowser.Dom.PointInspection.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IAttribute` | This interface is implemented by all `INode` implementations to support DOM event model. | DotNetBrowser.Dom.IAttribute.md |
| `IAttributes` | A dictionary that contains `IElement` attributes. Modifying this dictionary will lead to modifying the element attributes. | DotNetBrowser.Dom.IAttributes.md |
| `IDocument` | Represents DOM HTML document of the web page. | DotNetBrowser.Dom.IDocument.md |
| `IElement` | This interface is implemented by all `INode` implementations to support DOM event model. | DotNetBrowser.Dom.IElement.md |
| `IFormControlElement` | Represents the form control element. | DotNetBrowser.Dom.IFormControlElement.md |
| `IFormElement` | Represents DOM HTML Form element. | DotNetBrowser.Dom.IFormElement.md |
| `IFrameElement` | Represents an HTML <frame> or <iframe> element. | DotNetBrowser.Dom.IFrameElement.md |
| `IImageElement` | Represents DOM HTML image element <img>. | DotNetBrowser.Dom.IImageElement.md |
| `IInputElement` | Represents the DOM element with <input> tag. | DotNetBrowser.Dom.IInputElement.md |
| `INode` | This interface is implemented by all `INode` implementations to support DOM event model. | DotNetBrowser.Dom.INode.md |
| `INodeCollection` | Represents a collection of the DOM nodes. | DotNetBrowser.Dom.INodeCollection.md |
| `IOptionElement` | Represents the DOM HTML <option> element. | DotNetBrowser.Dom.IOptionElement.md |
| `ISearchContext` | The base interface for search that is implemented by the DOM objects that provide search mechanisms. | DotNetBrowser.Dom.ISearchContext.md |
| `ISelectElement` | Represents DOM HTML <select> element. | DotNetBrowser.Dom.ISelectElement.md |
| `ITextAreaElement` | Represents DOM HTML <textarea> element. | DotNetBrowser.Dom.ITextAreaElement.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `AlignTo` | Represents the values that can be used to describe how the element will be aligned to the visible area of the scrollable ancestor. | DotNetBrowser.Dom.AlignTo.md |
| `DocumentPosition` | Enumeration of the document position that represent the relationship between two nodes within the Document. | DotNetBrowser.Dom.DocumentPosition.md |
| `NodeType` | Represents the node types that can be used to distinguish different kind of nodes (such as an HTML element, text, attribute) from each other. | DotNetBrowser.Dom.NodeType.md |

## DotNetBrowser.Dom.Events

Namespace page: DotNetBrowser.Dom.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DomEventArgs` | The common DOM event arguments. | DotNetBrowser.Dom.Events.DomEventArgs.md |
| `Event` | Represents a DOM event that can be handled on the .NET side. | DotNetBrowser.Dom.Events.Event.md |
| `EventParameters` | The parameters of creating the DOM event. | DotNetBrowser.Dom.Events.EventParameters.md |
| `EventParameters.Builder` | The `EventParameters` builder. | DotNetBrowser.Dom.Events.EventParameters.Builder.md |
| `EventType` | The DOM event type. Wraps a string that specifies the name of the event without the "on" prefix. | DotNetBrowser.Dom.Events.EventType.md |
| `KeyEventParameters` | Represents the DOM keyboard event parameters. | DotNetBrowser.Dom.Events.KeyEventParameters.md |
| `MouseEventParameters` | Represents the DOM mouse event parameters. | DotNetBrowser.Dom.Events.MouseEventParameters.md |
| `UiEventModifierParameters` | Represents the DOM UI event parameters with the key modifiers. | DotNetBrowser.Dom.Events.UiEventModifierParameters.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IEvent` | Represents DOM Event object and provides access to the event object data. | DotNetBrowser.Dom.Events.IEvent.md |
| `IEventTarget` | This interface is implemented by all `INode` implementations to support DOM event model. | DotNetBrowser.Dom.Events.IEventTarget.md |
| `IEvents` | A collection of custom DOM events that can be listened and/or handled. | DotNetBrowser.Dom.Events.IEvents.md |
| `IKeyEvent` | Represents a keyboard event and provides an access to specific keyboard event data. | DotNetBrowser.Dom.Events.IKeyEvent.md |
| `IMouseEvent` | Represents a mouse event and provides an access to specific mouse event data. | DotNetBrowser.Dom.Events.IMouseEvent.md |
| `ITouchEvent` | Represents a touch event and provides an access to specific touch event data. | DotNetBrowser.Dom.Events.ITouchEvent.md |
| `IUiKeyEventModifier` | Represents a DOM UI event that can be fired with the key modifiers. | DotNetBrowser.Dom.Events.IUiKeyEventModifier.md |
| `IWheelEvent` | A wheel event that provides access to the wheel event data. | DotNetBrowser.Dom.Events.IWheelEvent.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `DeltaMode` | The type of the delta units. | DotNetBrowser.Dom.Events.DeltaMode.md |
| `DomKeyCode` | The DOM key codes represent physical keys on the keyboard (as opposed to the character generated by pressing the key). In other words, these values are not altered by keyboard layout or the state o... | DotNetBrowser.Dom.Events.DomKeyCode.md |
| `DomMouseButton` | A DOM mouse button. | DotNetBrowser.Dom.Events.DomMouseButton.md |
| `EventPhase` | Represents the DOM event phases. | DotNetBrowser.Dom.Events.EventPhase.md |

## DotNetBrowser.Dom.XPath

Namespace page: DotNetBrowser.Dom.XPath.md

### Classes

| Type | Summary | File |
|---|---|---|
| `XPathException` | This exception is thrown if XPath evaluation error occurs. | DotNetBrowser.Dom.XPath.XPathException.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IXPathResult` | Represents the result of the XPath expression evaluation. | DotNetBrowser.Dom.XPath.IXPathResult.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `XPathResultType` | Represents the XPath result types. | DotNetBrowser.Dom.XPath.XPathResultType.md |

## DotNetBrowser.Downloads

Namespace page: DotNetBrowser.Downloads.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DownloadInfo` | The general information about the download. | DotNetBrowser.Downloads.DownloadInfo.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IDownload` | Represents a download. | DotNetBrowser.Downloads.IDownload.md |
| `IDownloads` | A service that can be used to work with the downloads. | DotNetBrowser.Downloads.IDownloads.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `DownloadState` | The download state. | DotNetBrowser.Downloads.DownloadState.md |

## DotNetBrowser.Downloads.Events

Namespace page: DotNetBrowser.Downloads.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `CanceledEventArgs` | Event arguments for the `Canceled` event. | DotNetBrowser.Downloads.Events.CanceledEventArgs.md |
| `DownloadEventArgs` | The base class for `IDownload` events. | DotNetBrowser.Downloads.Events.DownloadEventArgs.md |
| `FinishedEventArgs` | Event arguments for the `Finished` event. | DotNetBrowser.Downloads.Events.FinishedEventArgs.md |
| `InterruptedEventArgs` | Event arguments for the `Interrupted` event. | DotNetBrowser.Downloads.Events.InterruptedEventArgs.md |
| `PausedEventArgs` | Event arguments for the `Paused` event. | DotNetBrowser.Downloads.Events.PausedEventArgs.md |
| `UpdatedEventArgs` | Event arguments for the `Updated` event. | DotNetBrowser.Downloads.Events.UpdatedEventArgs.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `DownloadInterruptionReason` | Possible download interruption reason. | DotNetBrowser.Downloads.Events.DownloadInterruptionReason.md |

## DotNetBrowser.Downloads.Handlers

Namespace page: DotNetBrowser.Downloads.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `StartDownloadParameters` | The parameters of the `StartDownloadHandler`. | DotNetBrowser.Downloads.Handlers.StartDownloadParameters.md |
| `StartDownloadResponse` | A response to the `StartDownloadHandler`. | DotNetBrowser.Downloads.Handlers.StartDownloadResponse.md |

## DotNetBrowser.Engine

Namespace page: DotNetBrowser.Engine.md

### Classes

| Type | Summary | File |
|---|---|---|
| `BinariesExtractionOptions` | The options that are used to configure the Chromium binaries extraction process. | DotNetBrowser.Engine.BinariesExtractionOptions.md |
| `ChromiumBinariesMissingException` | Thrown when the engine initialization fails due to missing compatible Chromium binaries. | DotNetBrowser.Engine.ChromiumBinariesMissingException.md |
| `ConnectionClosedException` | The exception thrown when the connection to the Chromium engine appears to be closed. | DotNetBrowser.Engine.ConnectionClosedException.md |
| `EngineFactory` | Factory class that is used to create `IEngine` instances. | DotNetBrowser.Engine.EngineFactory.md |
| `EngineInitializationException` | The base class for those exceptions that can be thrown during `IEngine` initialization. | DotNetBrowser.Engine.EngineInitializationException.md |
| `EngineOptions` | The options that are used to configure `IEngine` instances. | DotNetBrowser.Engine.EngineOptions.md |
| `EngineOptions.Builder` | A builder class to construct engine options. | DotNetBrowser.Engine.EngineOptions.Builder.md |
| `InvalidLicenseException` | Thrown when the given license is invalid. | DotNetBrowser.Engine.InvalidLicenseException.md |
| `LicenseException` | The base class for those exceptions that can be thrown during license checking. | DotNetBrowser.Engine.LicenseException.md |
| `MissingDependencyException` | Thrown when Chromium fails to find the required system libraries on Linux. | DotNetBrowser.Engine.MissingDependencyException.md |
| `NoLicenseException` | Thrown when no license found. | DotNetBrowser.Engine.NoLicenseException.md |
| `PasswordStore` | Defines password store types that are used to specify which encryption storage backend to use to encrypt cookies on Linux. | DotNetBrowser.Engine.PasswordStore.md |
| `SandboxNotSupportedException` | Thrown when the current environment does not support creating processes within a new user namespace, preventing Chromium from being launched in sandbox mode. | DotNetBrowser.Engine.SandboxNotSupportedException.md |
| `UserDataCreationException` | Thrown when the user data directory cannot be created. | DotNetBrowser.Engine.UserDataCreationException.md |
| `UserDataInUseException` | Thrown when the user data directory is already in use by another Chromium engine instance. | DotNetBrowser.Engine.UserDataInUseException.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IEngine` | Provides access to the Chromium engine functionality. | DotNetBrowser.Engine.IEngine.md |
| `IWidevine` | The Widevine DRM (Digital Rights Management) component. | DotNetBrowser.Engine.IWidevine.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `BinariesVerificationLevel` | The level of the Chromium binaries verification. | DotNetBrowser.Engine.BinariesVerificationLevel.md |
| `ProprietaryFeatures` | The list of supported proprietary features. | DotNetBrowser.Engine.ProprietaryFeatures.md |
| `RenderingMode` | The supported rendering modes. | DotNetBrowser.Engine.RenderingMode.md |
| `Theme` | The Chromium theme, which affects the appearanceof web pages and their contents, as well as Chromium dialogs, such as Print Preview and DevTools. | DotNetBrowser.Engine.Theme.md |
| `WidevineActivationStatus` | Represents the result of attempting to activate the Widevine component. | DotNetBrowser.Engine.WidevineActivationStatus.md |

## DotNetBrowser.Engine.Events

Namespace page: DotNetBrowser.Engine.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `EngineDisposedEventArgs` | The event arguments for the event indicating that the `IEngine` has been disposed. | DotNetBrowser.Engine.Events.EngineDisposedEventArgs.md |

## DotNetBrowser.Extensions

Namespace page: DotNetBrowser.Extensions.md

### Classes

| Type | Summary | File |
|---|---|---|
| `ExtensionInstallationException` | Thrown when the extension installation has failed for some reason. | DotNetBrowser.Extensions.ExtensionInstallationException.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IExtension` | A Chromium extension. | DotNetBrowser.Extensions.IExtension.md |
| `IExtensionAction` | The extension action is a clickable extension icon. | DotNetBrowser.Extensions.IExtensionAction.md |
| `IExtensions` | A service that allows managing extensions. | DotNetBrowser.Extensions.IExtensions.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `ExtensionActionType` | The extension action type. | DotNetBrowser.Extensions.ExtensionActionType.md |
| `ExtensionPermission` | The extension permission types. | DotNetBrowser.Extensions.ExtensionPermission.md |

## DotNetBrowser.Extensions.Events

Namespace page: DotNetBrowser.Extensions.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `ExtensionActionUpdatedEventArgs` | Event arguments for the `Updated` event. | DotNetBrowser.Extensions.Events.ExtensionActionUpdatedEventArgs.md |
| `ExtensionEventArgs` | The base class for the extension-related event arguments. | DotNetBrowser.Extensions.Events.ExtensionEventArgs.md |
| `ExtensionInstalledEventArgs` | Event arguments for the `ExtensionInstalled` event. | DotNetBrowser.Extensions.Events.ExtensionInstalledEventArgs.md |
| `ExtensionUninstalledEventArgs` | Event arguments for the `ExtensionUninstalled` event. | DotNetBrowser.Extensions.Events.ExtensionUninstalledEventArgs.md |
| `ExtensionUpdatedEventArgs` | Event arguments for the `ExtensionUpdated` event. | DotNetBrowser.Extensions.Events.ExtensionUpdatedEventArgs.md |

## DotNetBrowser.Extensions.Handlers

Namespace page: DotNetBrowser.Extensions.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `InstallExtensionParameters` | The parameters of the `InstallExtensionHandler`. | DotNetBrowser.Extensions.Handlers.InstallExtensionParameters.md |
| `InstallExtensionResponse` | The response to the `InstallExtensionHandler`. | DotNetBrowser.Extensions.Handlers.InstallExtensionResponse.md |
| `OpenExtensionPopupParameters` | The parameters of the `OpenExtensionPopupHandler`. | DotNetBrowser.Extensions.Handlers.OpenExtensionPopupParameters.md |
| `UninstallExtensionParameters` | The parameters of the `UninstallExtensionHandler`. | DotNetBrowser.Extensions.Handlers.UninstallExtensionParameters.md |
| `UninstallExtensionResponse` | The response to the `UninstallExtensionHandler`. | DotNetBrowser.Extensions.Handlers.UninstallExtensionResponse.md |

## DotNetBrowser.Frames

Namespace page: DotNetBrowser.Frames.md

### Classes

| Type | Summary | File |
|---|---|---|
| `EditorCommand` | Provides the supported commands that can be executed in a `IFrame`. | DotNetBrowser.Frames.EditorCommand.md |
| `WebStorageException` | Thrown by `IWebStorage` properties and methods to indicate that the requested operation failed. This is a superclass of the exceptions that can be thrown during working with `IWebStorage`. | DotNetBrowser.Frames.WebStorageException.md |
| `WebStorageOverflowException` | Thrown by `IWebStorage` indexer if the new value size exceeds the available space in the storage. | DotNetBrowser.Frames.WebStorageOverflowException.md |
| `WebStorageSecurityException` | Thrown by `IWebStorage` methods if the access to the web storage is forbidden for the current document. | DotNetBrowser.Frames.WebStorageSecurityException.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IFrame` | Represents a frame in the browser. Each web page loaded in the browser has a main(top-level) frame. The frame itself may have child frames. When a web page is unloaded, its frame and all child fram... | DotNetBrowser.Frames.IFrame.md |
| `IWebStorage` | An HTML WebStorage. Provides access to the session storage or local storage for a particular document on the loaded web page. Allows you to add, modify, or delete the stored items. | DotNetBrowser.Frames.IWebStorage.md |

## DotNetBrowser.Frames.Handlers

Namespace page: DotNetBrowser.Frames.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `ConvertJsNameParameters` | The parameters of the `ConvertJsNameHandler`. | DotNetBrowser.Frames.Handlers.ConvertJsNameParameters.md |
| `ConvertJsNameResponse` | The response to the `ConvertJsNameHandler`. | DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.md |

## DotNetBrowser.Geometry

Namespace page: DotNetBrowser.Geometry.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Ellipse` | Represents a three numbers that are used to define ellipse size and orientation in the two-dimensional space. | DotNetBrowser.Geometry.Ellipse.md |
| `Point` | Represents a pair of numbers that in general are used to define coordinates in the two-dimensional space. | DotNetBrowser.Geometry.Point.md |
| `Rectangle` | Represents a rectangle described by the location and dimensions. | DotNetBrowser.Geometry.Rectangle.md |
| `Size` | Represents a pair of numbers that in general are used to define dimensions in the two-dimensional space. | DotNetBrowser.Geometry.Size.md |

## DotNetBrowser.Handlers

Namespace page: DotNetBrowser.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `AsyncHandler<TParameters, TResponse>` | The default implementation of the `IHandler` interface. | DotNetBrowser.Handlers.AsyncHandler-2.md |
| `Handler<TParameters, TResponse>` | The default implementation of the `IHandler` interface. | DotNetBrowser.Handlers.Handler-2.md |
| `Handler<TParameters>` | The default implementation of the `IHandler` interface. | DotNetBrowser.Handlers.Handler-1.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IHandler<TParameters, TResponse>` | The common interface for all handlers. | DotNetBrowser.Handlers.IHandler-2.md |
| `IHandler<TParameters>` | The common interface for all handlers that must be executed synchronously, but do not have to return a value. | DotNetBrowser.Handlers.IHandler-1.md |

## DotNetBrowser.Input

Namespace page: DotNetBrowser.Input.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IInputEvent<TIInputEventArgs, TInputEventArgs>` | An input event. It is possible to raise this input event and dispatch it to the currently loaded web page. | DotNetBrowser.Input.IInputEvent-2.md |
| `IInterceptableEvent<TIInputEventArgs>` | An interceptable input event. It is possible to intercept and suppress this input event before it is actually processed by the browser. | DotNetBrowser.Input.IInterceptableEvent-1.md |
| `IInterceptableInputEvent<TIInputEventArgs, TInputEventArgs>` | An interceptable and raisable input event. It is possible to intercept and suppress this input event before it is actually processed by the browser or to raise it and dispatch to the currently load... | DotNetBrowser.Input.IInterceptableInputEvent-2.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `InputEventResponse` | The response to the input event handlers. | DotNetBrowser.Input.InputEventResponse.md |

## DotNetBrowser.Input.DragAndDrop

Namespace page: DotNetBrowser.Input.DragAndDrop.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IDragAndDrop` | The drag and drop functionality of the browser. | DotNetBrowser.Input.DragAndDrop.IDragAndDrop.md |

## DotNetBrowser.Input.DragAndDrop.Handlers

Namespace page: DotNetBrowser.Input.DragAndDrop.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DragAndDropParameters` | The base class for all `IDragAndDrop` handlers parameters. | DotNetBrowser.Input.DragAndDrop.Handlers.DragAndDropParameters.md |
| `DragEvent` | Represents drag and drop event and provides access to the event data. | DotNetBrowser.Input.DragAndDrop.Handlers.DragEvent.md |
| `DropParameters` | The parameters of the `DropHandler`. | DotNetBrowser.Input.DragAndDrop.Handlers.DropParameters.md |
| `EnterDragParameters` | The parameters of the `EnterDragHandler`. | DotNetBrowser.Input.DragAndDrop.Handlers.EnterDragParameters.md |

## DotNetBrowser.Input.Keyboard

Namespace page: DotNetBrowser.Input.Keyboard.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IKeyboard` | A service that can be used for keyboard input simulation and handling. | DotNetBrowser.Input.Keyboard.IKeyboard.md |

## DotNetBrowser.Input.Keyboard.Events

Namespace page: DotNetBrowser.Input.Keyboard.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `KeyCharEventArgs` | The event arguments for key events which provide a character. | DotNetBrowser.Input.Keyboard.Events.KeyCharEventArgs.md |
| `KeyEventArgs` |  | DotNetBrowser.Input.Keyboard.Events.KeyEventArgs.md |
| `KeyModifiers` |  | DotNetBrowser.Input.Keyboard.Events.KeyModifiers.md |
| `KeyPressedEventArgs` | The event arguments for the `KeyPressed` event. | DotNetBrowser.Input.Keyboard.Events.KeyPressedEventArgs.md |
| `KeyReleasedEventArgs` | The event arguments for the `KeyReleased` event. | DotNetBrowser.Input.Keyboard.Events.KeyReleasedEventArgs.md |
| `KeyTypedEventArgs` | The event arguments for the `KeyTyped` event. | DotNetBrowser.Input.Keyboard.Events.KeyTypedEventArgs.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IKeyCharEventArgs` | The event arguments for key events which provide a character. | DotNetBrowser.Input.Keyboard.Events.IKeyCharEventArgs.md |
| `IKeyEventArgs` | The base interface of all event arguments for the key events. | DotNetBrowser.Input.Keyboard.Events.IKeyEventArgs.md |
| `IKeyModifiers` | The keyboard modifiers applied. | DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md |
| `IKeyPressedEventArgs` | The event arguments for the `KeyPressed` event. | DotNetBrowser.Input.Keyboard.Events.IKeyPressedEventArgs.md |
| `IKeyReleasedEventArgs` | The event arguments for the `KeyReleased` event. | DotNetBrowser.Input.Keyboard.Events.IKeyReleasedEventArgs.md |
| `IKeyTypedEventArgs` | The event arguments for the `KeyTyped` event. | DotNetBrowser.Input.Keyboard.Events.IKeyTypedEventArgs.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `KeyCode` | The virtual key codes. | DotNetBrowser.Input.Keyboard.Events.KeyCode.md |
| `KeyLocation` | The key location on the keyboard. | DotNetBrowser.Input.Keyboard.Events.KeyLocation.md |

## DotNetBrowser.Input.Mouse

Namespace page: DotNetBrowser.Input.Mouse.md

### Classes

| Type | Summary | File |
|---|---|---|
| `MouseExtensions` | The mouse input simulation service extension methods. | DotNetBrowser.Input.Mouse.MouseExtensions.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IMouse` | A service that can be used for mouse input simulation and handling. | DotNetBrowser.Input.Mouse.IMouse.md |

## DotNetBrowser.Input.Mouse.Events

Namespace page: DotNetBrowser.Input.Mouse.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `MouseButtonEventArgs` | Event arguments for the `IMouse` events associated with a mouse button. | DotNetBrowser.Input.Mouse.Events.MouseButtonEventArgs.md |
| `MouseDraggedEventArgs` | The event arguments for the `Dragged` event. | DotNetBrowser.Input.Mouse.Events.MouseDraggedEventArgs.md |
| `MouseEnteredEventArgs` | The event arguments for the `Entered` event. | DotNetBrowser.Input.Mouse.Events.MouseEnteredEventArgs.md |
| `MouseEventArgs` |  | DotNetBrowser.Input.Mouse.Events.MouseEventArgs.md |
| `MouseExitedEventArgs` | The event arguments for the `Exited` event. | DotNetBrowser.Input.Mouse.Events.MouseExitedEventArgs.md |
| `MouseModifiers` |  | DotNetBrowser.Input.Mouse.Events.MouseModifiers.md |
| `MouseMovedEventArgs` | The event arguments for the `Moved` event. | DotNetBrowser.Input.Mouse.Events.MouseMovedEventArgs.md |
| `MousePressedEventArgs` | The event arguments for the `Pressed` event. | DotNetBrowser.Input.Mouse.Events.MousePressedEventArgs.md |
| `MouseReleasedEventArgs` | The event arguments for the `Released` event. | DotNetBrowser.Input.Mouse.Events.MouseReleasedEventArgs.md |
| `MouseWheelMovedEventArgs` | The event arguments for the `WheelMoved` event. | DotNetBrowser.Input.Mouse.Events.MouseWheelMovedEventArgs.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IMouseButtonEventArgs` | Event arguments for the `IMouse` events associated with a mouse button. | DotNetBrowser.Input.Mouse.Events.IMouseButtonEventArgs.md |
| `IMouseDraggedEventArgs` | The event arguments for the `Dragged` event. | DotNetBrowser.Input.Mouse.Events.IMouseDraggedEventArgs.md |
| `IMouseEnteredEventArgs` | The event arguments for the `Entered` event. | DotNetBrowser.Input.Mouse.Events.IMouseEnteredEventArgs.md |
| `IMouseEventArgs` | The base interface for all `IMouse` event arguments. | DotNetBrowser.Input.Mouse.Events.IMouseEventArgs.md |
| `IMouseExitedEventArgs` | The event arguments for the `Exited` event. | DotNetBrowser.Input.Mouse.Events.IMouseExitedEventArgs.md |
| `IMouseModifiers` | The mouse modifiers indicating which mouse buttons are currently pressed. | DotNetBrowser.Input.Mouse.Events.IMouseModifiers.md |
| `IMouseMovedEventArgs` | The event arguments for the `Moved` event. | DotNetBrowser.Input.Mouse.Events.IMouseMovedEventArgs.md |
| `IMousePressedEventArgs` | The event arguments for the `Pressed` event. | DotNetBrowser.Input.Mouse.Events.IMousePressedEventArgs.md |
| `IMouseReleasedEventArgs` | The event arguments for the `Released` event. | DotNetBrowser.Input.Mouse.Events.IMouseReleasedEventArgs.md |
| `IMouseWheelMovedEventArgs` | The event arguments for the `WheelMoved` event. | DotNetBrowser.Input.Mouse.Events.IMouseWheelMovedEventArgs.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `MouseButton` | The mouse buttons. | DotNetBrowser.Input.Mouse.Events.MouseButton.md |
| `MouseScrollType` | Scroll type. | DotNetBrowser.Input.Mouse.Events.MouseScrollType.md |

## DotNetBrowser.Input.Touch

Namespace page: DotNetBrowser.Input.Touch.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `ITouch` | A service that can be used for touch input handling. | DotNetBrowser.Input.Touch.ITouch.md |

## DotNetBrowser.Input.Touch.Events

Namespace page: DotNetBrowser.Input.Touch.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `TouchCanceledEventArgs` |  | DotNetBrowser.Input.Touch.Events.TouchCanceledEventArgs.md |
| `TouchEndedEventArgs` |  | DotNetBrowser.Input.Touch.Events.TouchEndedEventArgs.md |
| `TouchEventArgs` |  | DotNetBrowser.Input.Touch.Events.TouchEventArgs.md |
| `TouchMovedEventArgs` |  | DotNetBrowser.Input.Touch.Events.TouchMovedEventArgs.md |
| `TouchPoint` |  | DotNetBrowser.Input.Touch.Events.TouchPoint.md |
| `TouchStartedEventArgs` |  | DotNetBrowser.Input.Touch.Events.TouchStartedEventArgs.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `ITouchEventArgs` | Event arguments for the `ITouch` events associated with a surface touch. | DotNetBrowser.Input.Touch.Events.ITouchEventArgs.md |
| `ITouchPoint` | A single contact point on a touch-sensitive device. | DotNetBrowser.Input.Touch.Events.ITouchPoint.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `TouchState` | The possible states of the touch point. | DotNetBrowser.Input.Touch.Events.TouchState.md |

## DotNetBrowser.Js

Namespace page: DotNetBrowser.Js.md

### Classes

| Type | Summary | File |
|---|---|---|
| `JsException` | Thrown when an exception is raised in JavaScript. | DotNetBrowser.Js.JsException.md |
| `JsonExtensions` | Contains methods for working with JSON strings | DotNetBrowser.Js.JsonExtensions.md |
| `PropertyUpdateException` | Thrown when a property update fails. | DotNetBrowser.Js.PropertyUpdateException.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IJsFunction` | A JavaScript function that can be passed between .NET and JavaScript as a method argument or a return value. The function lifetime is bound to the lifetime of the frame this function belongs to. Wh... | DotNetBrowser.Js.IJsFunction.md |
| `IJsObject` | Represents a JavaScript object. Provides access to the object's properties and functions. The JavaScript object is alive until its JavaScript execution context exist. Once execution context is disp... | DotNetBrowser.Js.IJsObject.md |
| `IJsObjectPropertyCollection` | The JavaScript object properties. | DotNetBrowser.Js.IJsObjectPropertyCollection.md |
| `IJsPromise` | The JavaScript Promise. | DotNetBrowser.Js.IJsPromise.md |
| `IJsSymbol` | Represent a JavaScript "Symbol". JavaScript symbols are unique and immutable primitive values that may be used as the key of an object property. Symbols are often used to add unique property keys t... | DotNetBrowser.Js.IJsSymbol.md |

## DotNetBrowser.Js.Collections

Namespace page: DotNetBrowser.Js.Collections.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IJsArray` | A JavaScript array. | DotNetBrowser.Js.Collections.IJsArray.md |
| `IJsArrayBuffer` | A JavaScript array buffer. | DotNetBrowser.Js.Collections.IJsArrayBuffer.md |
| `IJsMap` | A JavaScript map. | DotNetBrowser.Js.Collections.IJsMap.md |
| `IJsSet` | A JavaScript set. | DotNetBrowser.Js.Collections.IJsSet.md |

## DotNetBrowser.Logging

Namespace page: DotNetBrowser.Logging.md

### Classes

| Type | Summary | File |
|---|---|---|
| `LoggerProvider` | Provides access to different DotNetBrowser Loggers which are used to log Browser, IPC and Chromium process messages. | DotNetBrowser.Logging.LoggerProvider.md |

## DotNetBrowser.Media

Namespace page: DotNetBrowser.Media.md

### Classes

| Type | Summary | File |
|---|---|---|
| `MediaDevice` | The details of the media input device (audio/video). | DotNetBrowser.Media.MediaDevice.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IAudio` | Allows controlling audio on the loaded web page and receive notifications when audio has been started or stopped playing. | DotNetBrowser.Media.IAudio.md |
| `IMediaDevices` | An engine service that allows accessing all the available media input devices. | DotNetBrowser.Media.IMediaDevices.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `MediaDeviceType` | The media device types. | DotNetBrowser.Media.MediaDeviceType.md |
| `MediaType` | List of the known media types. It's used in `ShowContextMenuParameters`. | DotNetBrowser.Media.MediaType.md |

## DotNetBrowser.Media.Events

Namespace page: DotNetBrowser.Media.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `AudioEventArgs` | The base class for `IAudio` related events. | DotNetBrowser.Media.Events.AudioEventArgs.md |
| `AudioPlaybackStartedEventArgs` | Event arguments for the `AudioPlaybackStarted` event. | DotNetBrowser.Media.Events.AudioPlaybackStartedEventArgs.md |
| `AudioPlaybackStoppedEventArgs` | Event arguments for the `AudioPlaybackStopped` event. | DotNetBrowser.Media.Events.AudioPlaybackStoppedEventArgs.md |

## DotNetBrowser.Media.Handlers

Namespace page: DotNetBrowser.Media.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `SelectMediaDeviceParameters` | The parameters of the `SelectMediaDeviceHandler`. | DotNetBrowser.Media.Handlers.SelectMediaDeviceParameters.md |
| `SelectMediaDeviceResponse` | A response to the `SelectMediaDeviceHandler`. | DotNetBrowser.Media.Handlers.SelectMediaDeviceResponse.md |

## DotNetBrowser.Navigation

Namespace page: DotNetBrowser.Navigation.md

### Classes

| Type | Summary | File |
|---|---|---|
| `LoadUrlParameters` | The parameters of the load url request. | DotNetBrowser.Navigation.LoadUrlParameters.md |
| `NavigationResult` | The result of the navigation occurred. | DotNetBrowser.Navigation.NavigationResult.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `INavigation` | Allows loading resources in the browser instance and working with the navigation history. | DotNetBrowser.Navigation.INavigation.md |
| `INavigationEntry` | The navigation history entry. | DotNetBrowser.Navigation.INavigationEntry.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `LoadResult` | The loading result. | DotNetBrowser.Navigation.LoadResult.md |
| `PageType` | Represents a navigation page type. | DotNetBrowser.Navigation.PageType.md |

## DotNetBrowser.Navigation.Events

Namespace page: DotNetBrowser.Navigation.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `FrameDocumentLoadFinishedEventArgs` | Event arguments for the `FrameDocumentLoadFinished` event. | DotNetBrowser.Navigation.Events.FrameDocumentLoadFinishedEventArgs.md |
| `FrameLoadFailedEventArgs` | Event arguments for the `FrameLoadFailed` event. | DotNetBrowser.Navigation.Events.FrameLoadFailedEventArgs.md |
| `FrameLoadFinishedEventArgs` | Event arguments for the `FrameLoadFinished` event. | DotNetBrowser.Navigation.Events.FrameLoadFinishedEventArgs.md |
| `FrameNavigationEventArgs` | The base class for all the `INavigation` event arguments containing `IFrame`. | DotNetBrowser.Navigation.Events.FrameNavigationEventArgs.md |
| `LoadFinishedEventArgs` | Event arguments for the `LoadFinished` event. | DotNetBrowser.Navigation.Events.LoadFinishedEventArgs.md |
| `LoadProgressChangedEventArgs` | Event arguments for the `LoadProgressChanged` event. | DotNetBrowser.Navigation.Events.LoadProgressChangedEventArgs.md |
| `LoadStartedEventArgs` | Event arguments for the `LoadStarted` event. | DotNetBrowser.Navigation.Events.LoadStartedEventArgs.md |
| `NavigationEventArgs` | The base class for `INavigation` event arguments. | DotNetBrowser.Navigation.Events.NavigationEventArgs.md |
| `NavigationFinishedEventArgs` | Event arguments for the `NavigationFinished` event. | DotNetBrowser.Navigation.Events.NavigationFinishedEventArgs.md |
| `NavigationRedirectedEventArgs` | Event arguments for the `NavigationRedirected` event. | DotNetBrowser.Navigation.Events.NavigationRedirectedEventArgs.md |
| `NavigationStartedEventArgs` | The event arguments for the `NavigationStarted` event. | DotNetBrowser.Navigation.Events.NavigationStartedEventArgs.md |
| `NavigationStoppedEventArgs` | Event arguments for the `NavigationStopped` event. | DotNetBrowser.Navigation.Events.NavigationStoppedEventArgs.md |

## DotNetBrowser.Navigation.Handlers

Namespace page: DotNetBrowser.Navigation.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `NavigationParameters` | The base class for all `INavigation` handlers parameters. | DotNetBrowser.Navigation.Handlers.NavigationParameters.md |
| `ShowHttpErrorPageParameters` | The parameters of the `ShowHttpErrorPageHandler`. | DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageParameters.md |
| `ShowHttpErrorPageResponse` | A response to the `ShowHttpErrorPageHandler`. | DotNetBrowser.Navigation.Handlers.ShowHttpErrorPageResponse.md |
| `ShowNetErrorPageParameters` | The parameters of the `ShowNetErrorPageHandler`. | DotNetBrowser.Navigation.Handlers.ShowNetErrorPageParameters.md |
| `ShowNetErrorPageResponse` | A response to the `ShowNetErrorPageHandler`. | DotNetBrowser.Navigation.Handlers.ShowNetErrorPageResponse.md |
| `StartNavigationParameters` | The parameters of the `StartNavigationHandler`. | DotNetBrowser.Navigation.Handlers.StartNavigationParameters.md |
| `StartNavigationResponse` | A response to the `StartNavigationHandler`. | DotNetBrowser.Navigation.Handlers.StartNavigationResponse.md |

## DotNetBrowser.Net

Namespace page: DotNetBrowser.Net.md

### Classes

| Type | Summary | File |
|---|---|---|
| `BytesData` | The upload data as bytes. Can be empty if the form doesn't contain any data. | DotNetBrowser.Net.BytesData.md |
| `FileValue` |  | DotNetBrowser.Net.FileValue.md |
| `FormData` | The list of key-value pairs each representing a segment of a form data. Can be empty if the form doesn't contain any data. | DotNetBrowser.Net.FormData.md |
| `HostPortPair` | A host/port pair of the URI. | DotNetBrowser.Net.HostPortPair.md |
| `HttpHeader` |  | DotNetBrowser.Net.HttpHeader.md |
| `MimeType` | The MIME type. | DotNetBrowser.Net.MimeType.md |
| `MultipartFormData` | The list of key-value pairs each representing a segment of a multi-part form data. Can be empty if the form doesn't contain any data. | DotNetBrowser.Net.MultipartFormData.md |
| `MultipartFormDataKeyValuePair` | A key-value pair that represents a segment of a multi-part form data. Can contain values corresponding a form field content, an upload file content, etc. | DotNetBrowser.Net.MultipartFormDataKeyValuePair.md |
| `Scheme` | The scheme component of a URL. | DotNetBrowser.Net.Scheme.md |
| `TextData` | The upload data of the text/plain content type. | DotNetBrowser.Net.TextData.md |
| `UploadData` | The base class for all upload data. | DotNetBrowser.Net.UploadData.md |
| `UrlRequest` | Represents the URL request received from the Chromium engine. | DotNetBrowser.Net.UrlRequest.md |
| `UrlRequestJob` | The URL request job for the intercepted URL request, which allows you to provide the response data for this URL request. | DotNetBrowser.Net.UrlRequestJob.md |
| `UrlRequestJobExtensions` | Provides extension methods for `UrlRequestJob`. | DotNetBrowser.Net.UrlRequestJobExtensions.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IFileValue` | File data. | DotNetBrowser.Net.IFileValue.md |
| `IHttpAuthPreferences` | The HTTP authorization preferences. | DotNetBrowser.Net.IHttpAuthPreferences.md |
| `IHttpHeader` | Represents the single HTTP header with all its values. | DotNetBrowser.Net.IHttpHeader.md |
| `INetwork` | Allows access and modifying to the network-level activities. | DotNetBrowser.Net.INetwork.md |
| `IUploadData` | The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`, `application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the ... | DotNetBrowser.Net.IUploadData.md |
| `IUploadData<T>` | The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`, `application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the ... | DotNetBrowser.Net.IUploadData-1.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `NetError` | The network errors. | DotNetBrowser.Net.NetError.md |
| `RequestStatus` | The status of a URL request. | DotNetBrowser.Net.RequestStatus.md |
| `SslVersion` | The supported SSL connection versions. | DotNetBrowser.Net.SslVersion.md |

## DotNetBrowser.Net.Certificates

Namespace page: DotNetBrowser.Net.Certificates.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Certificate` | Provides information about the digital certificate. This certificate represents a X.509 certificate, which consists of a particular identity or end-entity certificate, such as an server identity or... | DotNetBrowser.Net.Certificates.Certificate.md |
| `CertificateVerificationError` | Provides information about an error found by Chromium when verifying an SSL certificate. | DotNetBrowser.Net.Certificates.CertificateVerificationError.md |
| `ExtendedKeyUsage` | Defines how the certificate key can be used. | DotNetBrowser.Net.Certificates.ExtendedKeyUsage.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `CertificateVerificationStatus` | The status that indicates result of SSL certificate verification by default Chromium certificate verifier. | DotNetBrowser.Net.Certificates.CertificateVerificationStatus.md |

## DotNetBrowser.Net.Events

Namespace page: DotNetBrowser.Net.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `ConnectionTypeChangedEventArgs` | Event arguments for the `ConnectionTypeChanged` event. | DotNetBrowser.Net.Events.ConnectionTypeChangedEventArgs.md |
| `NetworkEventArgs` | The base class for `INetwork` event arguments. | DotNetBrowser.Net.Events.NetworkEventArgs.md |
| `PacScriptErrorEventArgs` | Event arguments for the `PacScriptErrorOccurred` event. | DotNetBrowser.Net.Events.PacScriptErrorEventArgs.md |
| `RedirectResponseCodeReceivedEventArgs` | Event arguments for the `RedirectResponseCodeReceived` event. | DotNetBrowser.Net.Events.RedirectResponseCodeReceivedEventArgs.md |
| `RequestCompletedEventArgs` | Event arguments for the `RequestCompleted` event. | DotNetBrowser.Net.Events.RequestCompletedEventArgs.md |
| `RequestDestroyedEventArgs` | Event arguments for the `RequestDestroyed` event. | DotNetBrowser.Net.Events.RequestDestroyedEventArgs.md |
| `ResponseBytesReceivedEventArgs` | Event arguments for the `ResponseBytesReceived` event. | DotNetBrowser.Net.Events.ResponseBytesReceivedEventArgs.md |
| `ResponseStartedEventArgs` | Event arguments for the `ResponseStarted` event. | DotNetBrowser.Net.Events.ResponseStartedEventArgs.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `ConnectionType` | The network connection type. | DotNetBrowser.Net.Events.ConnectionType.md |

## DotNetBrowser.Net.Handlers

Namespace page: DotNetBrowser.Net.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `AuthenticateParameters` | The parameters of the `AuthenticateHandler`. | DotNetBrowser.Net.Handlers.AuthenticateParameters.md |
| `AuthenticateResponse` | A response for the `AuthenticateHandler`. | DotNetBrowser.Net.Handlers.AuthenticateResponse.md |
| `CanAccessFileParameters` | The parameters of the `CanAccessFileHandler`. | DotNetBrowser.Net.Handlers.CanAccessFileParameters.md |
| `CanAccessFileResponse` | A response for the `CanAccessFileHandler`. | DotNetBrowser.Net.Handlers.CanAccessFileResponse.md |
| `CanGetCookiesParameters` | The parameters of the `CanGetCookiesHandler`. | DotNetBrowser.Net.Handlers.CanGetCookiesParameters.md |
| `CanGetCookiesResponse` | A response for the `CanGetCookiesHandler`. | DotNetBrowser.Net.Handlers.CanGetCookiesResponse.md |
| `CanSetCookieParameters` | The parameters of the `CanSetCookieHandler`. | DotNetBrowser.Net.Handlers.CanSetCookieParameters.md |
| `CanSetCookieResponse` | A response for the `CanSetCookieHandler`. | DotNetBrowser.Net.Handlers.CanSetCookieResponse.md |
| `InterceptRequestParameters` | The parameters of the scheme handler. | DotNetBrowser.Net.Handlers.InterceptRequestParameters.md |
| `InterceptRequestResponse` | A response for the scheme handler. | DotNetBrowser.Net.Handlers.InterceptRequestResponse.md |
| `NetworkParameters` | The base class for `INetwork`-related handlers parameters. | DotNetBrowser.Net.Handlers.NetworkParameters.md |
| `ReceiveHeadersParameters` | The parameters of the `ReceiveHeadersHandler`. | DotNetBrowser.Net.Handlers.ReceiveHeadersParameters.md |
| `ReceiveHeadersResponse` | The response for the `ReceiveHeadersHandler`. | DotNetBrowser.Net.Handlers.ReceiveHeadersResponse.md |
| `SendUploadDataParameters` | The parameters of the `SendUploadDataHandler`. | DotNetBrowser.Net.Handlers.SendUploadDataParameters.md |
| `SendUploadDataResponse` | The response for the `SendUploadDataHandler`. | DotNetBrowser.Net.Handlers.SendUploadDataResponse.md |
| `SendUrlRequestParameters` | The parameters of the `SendUrlRequestHandler`. | DotNetBrowser.Net.Handlers.SendUrlRequestParameters.md |
| `SendUrlRequestResponse` | A response of the `SendUrlRequestHandler`. | DotNetBrowser.Net.Handlers.SendUrlRequestResponse.md |
| `StartTransactionParameters` | The parameters of the `StartTransactionHandler`. | DotNetBrowser.Net.Handlers.StartTransactionParameters.md |
| `StartTransactionResponse` | A response for the `StartTransactionHandler`. | DotNetBrowser.Net.Handlers.StartTransactionResponse.md |
| `UrlRequestJobOptions` | The options needed to create the `UrlRequestJob`. | DotNetBrowser.Net.Handlers.UrlRequestJobOptions.md |
| `UrlRequestParameters` | The base class for all the `INetwork`-related handlers parameters containing `UrlRequest`. | DotNetBrowser.Net.Handlers.UrlRequestParameters.md |
| `VerifyCertificateParameters` | The parameters of the `VerifyCertificateHandler`. | DotNetBrowser.Net.Handlers.VerifyCertificateParameters.md |
| `VerifyCertificateResponse` | A response for the `VerifyCertificateHandler` | DotNetBrowser.Net.Handlers.VerifyCertificateResponse.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `ResourceType` | The type of the resource being loaded. | DotNetBrowser.Net.Handlers.ResourceType.md |

## DotNetBrowser.Net.Proxy

Namespace page: DotNetBrowser.Net.Proxy.md

### Classes

| Type | Summary | File |
|---|---|---|
| `AutoDetectProxySettings` | With this proxy configuration the connection automatically detects proxy settings. | DotNetBrowser.Net.Proxy.AutoDetectProxySettings.md |
| `CustomProxySettings` | Describes a user's proxy settings. | DotNetBrowser.Net.Proxy.CustomProxySettings.md |
| `DirectProxySettings` | With this proxy configuration the connection doesn't use a proxy server. | DotNetBrowser.Net.Proxy.DirectProxySettings.md |
| `PacProxySettings` | With this proxy configuration the connection uses proxy settings received from proxy auto-config (PAC) file which is located at the specific address. | DotNetBrowser.Net.Proxy.PacProxySettings.md |
| `ProxySettings` | The base class for all proxy settings. | DotNetBrowser.Net.Proxy.ProxySettings.md |
| `SystemProxySettings` | The system proxy settings defined by the operating system. | DotNetBrowser.Net.Proxy.SystemProxySettings.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IProxy` | The service that allows modifying the proxy configuration for the current engine. | DotNetBrowser.Net.Proxy.IProxy.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `ProxyType` | Types of proxy settings. | DotNetBrowser.Net.Proxy.ProxyType.md |

## DotNetBrowser.Passwords

Namespace page: DotNetBrowser.Passwords.md

### Classes

| Type | Summary | File |
|---|---|---|
| `PasswordRecord` | A record saved in the `IPasswordStore`. | DotNetBrowser.Passwords.PasswordRecord.md |
| `PasswordRecord.Builder` | A builder for creating a new `PasswordRecord` instance. | DotNetBrowser.Passwords.PasswordRecord.Builder.md |
| `PasswordStoreExtensions` | Provides extension methods for `IPasswordStore`. | DotNetBrowser.Passwords.PasswordStoreExtensions.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IPasswordStore` | A service that allows working with `PasswordRecord` logins and passwords saved in the Chromium password store. | DotNetBrowser.Passwords.IPasswordStore.md |
| `IPasswords` | A service that allows managing passwords. | DotNetBrowser.Passwords.IPasswords.md |

## DotNetBrowser.Passwords.Handlers

Namespace page: DotNetBrowser.Passwords.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `SavePasswordParameters` | The parameters of the `SavePasswordHandler`. | DotNetBrowser.Passwords.Handlers.SavePasswordParameters.md |
| `SavePasswordResponse` | A response to the `SavePasswordHandler`. | DotNetBrowser.Passwords.Handlers.SavePasswordResponse.md |
| `UpdatePasswordParameters` | The parameters of the `UpdatePasswordHandler`. | DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.md |
| `UpdatePasswordResponse` | A response to the `UpdatePasswordHandler`. | DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse.md |

## DotNetBrowser.Permissions

Namespace page: DotNetBrowser.Permissions.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IPermissions` | A service that allows managing permissions. | DotNetBrowser.Permissions.IPermissions.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `PermissionType` | Represents the permission types. | DotNetBrowser.Permissions.PermissionType.md |

## DotNetBrowser.Permissions.Handlers

Namespace page: DotNetBrowser.Permissions.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `RequestPermissionParameters` | The parameters of the `RequestPermissionHandler`. | DotNetBrowser.Permissions.Handlers.RequestPermissionParameters.md |
| `RequestPermissionResponse` | A response to the `RequestPermissionHandler`. | DotNetBrowser.Permissions.Handlers.RequestPermissionResponse.md |

## DotNetBrowser.Plugins

Namespace page: DotNetBrowser.Plugins.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Plugin` | The detailed information about the installed Chromium plugin. | DotNetBrowser.Plugins.Plugin.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IPluginSettings` | The settings to configure the available Chromium `Plugins`. | DotNetBrowser.Plugins.IPluginSettings.md |
| `IPlugins` | The engine service that provides the details about the available Chromium plugins. | DotNetBrowser.Plugins.IPlugins.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `PluginType` | The plugin types. | DotNetBrowser.Plugins.PluginType.md |

## DotNetBrowser.Plugins.Handlers

Namespace page: DotNetBrowser.Plugins.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `AllowPluginParameters` | The parameters for the `AllowPluginHandler`. | DotNetBrowser.Plugins.Handlers.AllowPluginParameters.md |
| `AllowPluginResponse` | A response to the `AllowPluginHandler`. | DotNetBrowser.Plugins.Handlers.AllowPluginResponse.md |

## DotNetBrowser.Print

Namespace page: DotNetBrowser.Print.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Capabilities` | The capabilities of a printer. | DotNetBrowser.Print.Capabilities.md |
| `PageMargins` | The page margins used for printing. | DotNetBrowser.Print.PageMargins.md |
| `PageRange` | The page range to be printed. | DotNetBrowser.Print.PageRange.md |
| `PaperSize` | The paper size used for printing. | DotNetBrowser.Print.PaperSize.md |
| `PdfPrinter` | A printer that allows you to print to PDF. | DotNetBrowser.Print.PdfPrinter.md |
| `PdfPrinter<TPrintSettings>` | A printer that allows you to print to PDF. | DotNetBrowser.Print.PdfPrinter-1.md |
| `Printer<TPrintSettings>` | The base class for the printers. | DotNetBrowser.Print.Printer-1.md |
| `Scaling` | The scaling used for printing. | DotNetBrowser.Print.Scaling.md |
| `SystemPrinter` | A local or network printer available in the system. | DotNetBrowser.Print.SystemPrinter.md |
| `SystemPrinter<TPrintSettings>` | A local or network printer available in the system. | DotNetBrowser.Print.SystemPrinter-1.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IPrintJob<TPrintSettings>` | A printing operation that is currently in-progress. | DotNetBrowser.Print.IPrintJob-1.md |
| `IPrinters<TPrintSettings, TPdfPrintSettings>` | The collection of the available printers. | DotNetBrowser.Print.IPrinters-2.md |
| `PdfPrinter.IHtmlSettings` | The print settings available when printing HTML content on the PDF printer. | DotNetBrowser.Print.PdfPrinter.IHtmlSettings.md |
| `PdfPrinter.IPdfSettings` | The print settings available when printing PDF content on the PDF printer. | DotNetBrowser.Print.PdfPrinter.IPdfSettings.md |
| `PdfPrinter.ISettings<T>` | The print settings available when printing HTML or PDF content on the PDF printer. | DotNetBrowser.Print.PdfPrinter.ISettings-1.md |
| `SystemPrinter.IHtmlSettings` | Print settings available when printing HTML content on a physical printer. | DotNetBrowser.Print.SystemPrinter.IHtmlSettings.md |
| `SystemPrinter.IPdfSettings` | Print settings available when printing PDF content on a physical printer. | DotNetBrowser.Print.SystemPrinter.IPdfSettings.md |
| `SystemPrinter.ISettings<T>` | Print settings available when printing HTML or PDF content on a physical printer. | DotNetBrowser.Print.SystemPrinter.ISettings-1.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `ColorModel` | The color models used for printing. | DotNetBrowser.Print.ColorModel.md |
| `DuplexMode` | The duplex modes used for printing. | DotNetBrowser.Print.DuplexMode.md |
| `Fit` | The content fit used for printing. | DotNetBrowser.Print.Fit.md |
| `Orientation` | The page orientation values used for printing. | DotNetBrowser.Print.Orientation.md |
| `PagesPerSheet` | The pages per sheet values that Chromium supports. | DotNetBrowser.Print.PagesPerSheet.md |
| `PaperSize.Unit` | The measurement unit of the paper size. | DotNetBrowser.Print.PaperSize.Unit.md |

## DotNetBrowser.Print.Events

Namespace page: DotNetBrowser.Print.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `PageCountUpdatedEventArgs<TPrintSettings>` | Event arguments for the `PageCountUpdated` event. | DotNetBrowser.Print.Events.PageCountUpdatedEventArgs-1.md |
| `PrintCompletedEventArgs<TPrintSettings>` | Event arguments for the `PrintCompleted` event. | DotNetBrowser.Print.Events.PrintCompletedEventArgs-1.md |

## DotNetBrowser.Print.Handlers

Namespace page: DotNetBrowser.Print.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `PrintContentParameters<TPrintSettings, TPdfPrintSettings>` | The base class for content printing handlers parameters. | DotNetBrowser.Print.Handlers.PrintContentParameters-2.md |
| `PrintHtmlContentParameters` | The parameters of the `PrintHtmlContentHandler`. | DotNetBrowser.Print.Handlers.PrintHtmlContentParameters.md |
| `PrintHtmlContentResponse` | A response for the `PrintHtmlContentHandler`. | DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.md |
| `PrintPdfContentParameters` | The parameters of the `PrintPdfContentHandler`. | DotNetBrowser.Print.Handlers.PrintPdfContentParameters.md |
| `PrintPdfContentResponse` | A response for the `PrintPdfContentHandler`. | DotNetBrowser.Print.Handlers.PrintPdfContentResponse.md |

## DotNetBrowser.Print.Settings

Namespace page: DotNetBrowser.Print.Settings.md

### Classes

| Type | Summary | File |
|---|---|---|
| `CollateExtensions` | Extension methods for `ICollate` interface. | DotNetBrowser.Print.Settings.CollateExtensions.md |
| `ColorModelExtensions` | Extension methods for `IColorModel` interface. | DotNetBrowser.Print.Settings.ColorModelExtensions.md |
| `CopiesExtensions` | Extension methods for `ICopies` interface. | DotNetBrowser.Print.Settings.CopiesExtensions.md |
| `DuplexModeExtensions` | Extension methods for `IDuplexMode` interface. | DotNetBrowser.Print.Settings.DuplexModeExtensions.md |
| `FitExtensions` | Extension methods for `IFit` interface. | DotNetBrowser.Print.Settings.FitExtensions.md |
| `FooterTemplateExtensions` | Extension methods for `IFooterTemplate` interface. | DotNetBrowser.Print.Settings.FooterTemplateExtensions.md |
| `HeaderTemplateExtensions` | Extension methods for `IHeaderTemplate` interface. | DotNetBrowser.Print.Settings.HeaderTemplateExtensions.md |
| `OrientationExtensions` | Extension methods for `IOrientation` interface. | DotNetBrowser.Print.Settings.OrientationExtensions.md |
| `PageMarginsExtensions` | Extension methods for `IPageMargins` interface. | DotNetBrowser.Print.Settings.PageMarginsExtensions.md |
| `PageRangesExtensions` | Extension methods for `IPageRanges` interface. | DotNetBrowser.Print.Settings.PageRangesExtensions.md |
| `PagesPerSheetExtensions` | Extension methods for `IPagesPerSheet` interface. | DotNetBrowser.Print.Settings.PagesPerSheetExtensions.md |
| `PaperSizeExtensions` | Extension methods for `IPaperSize` interface. | DotNetBrowser.Print.Settings.PaperSizeExtensions.md |
| `PdfFilePathExtensions` | Extension methods for `IPdfFilePath` interface. | DotNetBrowser.Print.Settings.PdfFilePathExtensions.md |
| `PrintBackgroundsExtensions` | Extension methods for `IPrintBackgrounds` interface. | DotNetBrowser.Print.Settings.PrintBackgroundsExtensions.md |
| `PrintHeaderFooterExtensions` | Extension methods for `IPrintHeaderFooter` interface. | DotNetBrowser.Print.Settings.PrintHeaderFooterExtensions.md |
| `PrintSelectionOnlyExtensions` | Extension methods for `IPrintSelectionOnly` interface. | DotNetBrowser.Print.Settings.PrintSelectionOnlyExtensions.md |
| `PrintSettingsExtensions` | Extension methods for `IPrintSettings` interface. | DotNetBrowser.Print.Settings.PrintSettingsExtensions.md |
| `ScalingExtensions` | Extension methods for `IScaling` interface. | DotNetBrowser.Print.Settings.ScalingExtensions.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `ICollate<TPrintSettings>` | Allows configuring collate printing. | DotNetBrowser.Print.Settings.ICollate-1.md |
| `IColorModel<TPrintSettings>` | Allows configuring the color model for printing. | DotNetBrowser.Print.Settings.IColorModel-1.md |
| `ICopies<TPrintSettings>` | Allows configuring the number of copies to print. | DotNetBrowser.Print.Settings.ICopies-1.md |
| `IDuplexMode<TPrintSettings>` | Allows configuring the duplex mode for printing. | DotNetBrowser.Print.Settings.IDuplexMode-1.md |
| `IFit<TPrintSettings>` | Allows configuring the content fit for printing. | DotNetBrowser.Print.Settings.IFit-1.md |
| `IFooterTemplate<TPrintSettings>` | Allows configuring the HTML template for the print footer. | DotNetBrowser.Print.Settings.IFooterTemplate-1.md |
| `IHeaderTemplate<TPrintSettings>` | Allows configuring the HTML template for the print header. | DotNetBrowser.Print.Settings.IHeaderTemplate-1.md |
| `IOrientation<TPrintSettings>` | Allows configuring the page orientation. | DotNetBrowser.Print.Settings.IOrientation-1.md |
| `IPageMargins<TPrintSettings>` | Allows configuring the page margins. | DotNetBrowser.Print.Settings.IPageMargins-1.md |
| `IPageRanges<TPrintSettings>` | Allows configuring the page ranges for printing. | DotNetBrowser.Print.Settings.IPageRanges-1.md |
| `IPagesPerSheet<TPrintSettings>` | Allows configuring the number of pages per sheet. | DotNetBrowser.Print.Settings.IPagesPerSheet-1.md |
| `IPaperSize<TPrintSettings>` | Allows configuring the paper size for printing. | DotNetBrowser.Print.Settings.IPaperSize-1.md |
| `IPdfFilePath<TPrintSettings>` | Allows configuring the destination PDF file path. | DotNetBrowser.Print.Settings.IPdfFilePath-1.md |
| `IPrintBackgrounds<TPrintSettings>` | Allows configuring printing background graphics. | DotNetBrowser.Print.Settings.IPrintBackgrounds-1.md |
| `IPrintHeaderFooter<TPrintSettings>` | Allows configuring printing headers and footers. | DotNetBrowser.Print.Settings.IPrintHeaderFooter-1.md |
| `IPrintSelectionOnly<TPrintSettings>` | Allows configuring printing only the selected content. | DotNetBrowser.Print.Settings.IPrintSelectionOnly-1.md |
| `IPrintSettings` | The common interface for the concrete print job settings to implement. | DotNetBrowser.Print.Settings.IPrintSettings.md |
| `IScaling<TPrintSettings>` | Allows configuring the scaling for printing. | DotNetBrowser.Print.Settings.IScaling-1.md |

## DotNetBrowser.Profile

Namespace page: DotNetBrowser.Profile.md

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IProfile` | The Chromium profile. | DotNetBrowser.Profile.IProfile.md |
| `IProfilePreferences` | The preferences of a `IProfile`. | DotNetBrowser.Profile.IProfilePreferences.md |
| `IProfiles` | The collection of the Chromium profiles. | DotNetBrowser.Profile.IProfiles.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `CookieControlsMode` | The Chromium third-party cookies block mode. | DotNetBrowser.Profile.CookieControlsMode.md |
| `ProfileType` | The Chromium profile type. | DotNetBrowser.Profile.ProfileType.md |

## DotNetBrowser.Search

Namespace page: DotNetBrowser.Search.md

### Classes

| Type | Summary | File |
|---|---|---|
| `FindOptions` | The find text options. | DotNetBrowser.Search.FindOptions.md |
| `FindResult` | A result of the text search. | DotNetBrowser.Search.FindResult.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `ITextFinder` | Allows finding text on the loaded web page. | DotNetBrowser.Search.ITextFinder.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `Direction` | The search direction. | DotNetBrowser.Search.Direction.md |
| `StopFindAction` | The stop find actions. | DotNetBrowser.Search.StopFindAction.md |

## DotNetBrowser.Search.Handlers

Namespace page: DotNetBrowser.Search.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `FindResultReceivedParameters` | The parameters of the handler that is passed to the `Find` method and called when a find result is received. | DotNetBrowser.Search.Handlers.FindResultReceivedParameters.md |

## DotNetBrowser.SpellCheck

Namespace page: DotNetBrowser.SpellCheck.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Language` | The language for which Chromium can perform spell checking. | DotNetBrowser.SpellCheck.Language.md |
| `LanguageNotAvailableException` | Thrown when the engine fails to configure the spellchecker to use the language passed to the `Add` method. | DotNetBrowser.SpellCheck.LanguageNotAvailableException.md |
| `SpellCheckMenu` | A spell check menu in the context menu. | DotNetBrowser.SpellCheck.SpellCheckMenu.md |
| `SpellCheckingResult` | The spell checking result that contains the bounds of a mis-spelled substring of the checked text. | DotNetBrowser.SpellCheck.SpellCheckingResult.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `ILanguages` | The collection of the languages used for spell checking. | DotNetBrowser.SpellCheck.ILanguages.md |
| `ISpellCheckDictionary` | Provides functionality for working with a spell check dictionary. | DotNetBrowser.SpellCheck.ISpellCheckDictionary.md |
| `ISpellChecker` | Represents an engine service that provides functionality for configuring spell checking. | DotNetBrowser.SpellCheck.ISpellChecker.md |

## DotNetBrowser.Ui

Namespace page: DotNetBrowser.Ui.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Bitmap` | Represents a binary image that consists of an image size and a byte array that contains the pre-multiplied image pixels in the BGRA format. | DotNetBrowser.Ui.Bitmap.md |
| `Color` | A numeric model of an RGB color. The components of the color instance are presented in the arithmetic notation. This means that each component accepts any fractional value from 0 to 1. | DotNetBrowser.Ui.Color.md |
| `Font` | A system font. | DotNetBrowser.Ui.Font.md |
| `FontSize` | The browser font size. | DotNetBrowser.Ui.FontSize.md |
| `Language` | The supported user interface languages. | DotNetBrowser.Ui.Language.md |

## DotNetBrowser.Ui.Cursors

Namespace page: DotNetBrowser.Ui.Cursors.md

### Enums

| Type | Summary | File |
|---|---|---|
| `CursorType` | The cursor types. | DotNetBrowser.Ui.Cursors.CursorType.md |

## DotNetBrowser.UserData

Namespace page: DotNetBrowser.UserData.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Address` | The user's address containing information about a street, city, state, etc. | DotNetBrowser.UserData.Address.md |
| `Address.Builder` | A builder for the `Address` class. | DotNetBrowser.UserData.Address.Builder.md |
| `UserDataProfile` | The collected data entered by the user to a form and persisted to `the user data store`. | DotNetBrowser.UserData.UserDataProfile.md |
| `UserDataProfile.Builder` | A builder for creating a new `UserDataProfile` instance. | DotNetBrowser.UserData.UserDataProfile.Builder.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IUserDataProfileStore` | The data store for `the user data`. | DotNetBrowser.UserData.IUserDataProfileStore.md |
| `IUserDataProfiles` | A service that allows managing user data profiles. | DotNetBrowser.UserData.IUserDataProfiles.md |

## DotNetBrowser.UserData.Handlers

Namespace page: DotNetBrowser.UserData.Handlers.md

### Classes

| Type | Summary | File |
|---|---|---|
| `SaveUserDataProfileParameters` | The parameters of the `SaveUserDataProfileHandler`. | DotNetBrowser.UserData.Handlers.SaveUserDataProfileParameters.md |
| `SaveUserDataProfileResponse` | A response to the `SaveUserDataProfileHandler`. | DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse.md |
| `UpdateUserDataProfileParameters` | The parameters of the `UpdateUserDataProfileHandler`. | DotNetBrowser.UserData.Handlers.UpdateUserDataProfileParameters.md |
| `UpdateUserDataProfileResponse` | A response to the `UpdateUserDataProfileHandler`. | DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse.md |

## DotNetBrowser.WinForms

Namespace page: DotNetBrowser.WinForms.md

### Classes

| Type | Summary | File |
|---|---|---|
| `BitmapExtensions` | Extensions for `Bitmap` class. | DotNetBrowser.WinForms.BitmapExtensions.md |
| `BrowserView` | The WinForms-based implementation of browser view. | DotNetBrowser.WinForms.BrowserView.md |

## DotNetBrowser.WinForms.Dialogs

Namespace page: DotNetBrowser.WinForms.Dialogs.md

### Classes

| Type | Summary | File |
|---|---|---|
| `ColorExtensions` | Extension methods for performing color conversion. | DotNetBrowser.WinForms.Dialogs.ColorExtensions.md |
| `DefaultAuthenticationHandler` | Default WinForms authentication handler, which displays an authentication dialog. | DotNetBrowser.WinForms.Dialogs.DefaultAuthenticationHandler.md |
| `DefaultStartDownloadHandler` | The default WinForms implementation of `StartDownloadHandler`, which displays a save file dialog to specify the path to store the downloaded file. | DotNetBrowser.WinForms.Dialogs.DefaultStartDownloadHandler.md |
| `DialogHandlerBase` | The base class for all dialog handlers. | DotNetBrowser.WinForms.Dialogs.DialogHandlerBase.md |

## DotNetBrowser.WinForms.Extensions

Namespace page: DotNetBrowser.WinForms.Extensions.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DefaultOpenExtensionPopupHandler` | Default extension popup handler, which displays an extension popup as a separate window. | DotNetBrowser.WinForms.Extensions.DefaultOpenExtensionPopupHandler.md |

## DotNetBrowser.WinUi3

Namespace page: DotNetBrowser.WinUi3.md

### Classes

| Type | Summary | File |
|---|---|---|
| `BitmapExtensions` | Extensions for `Bitmap` class. | DotNetBrowser.WinUi3.BitmapExtensions.md |
| `BrowserView` | The WinUI3-based implementation of browser view. | DotNetBrowser.WinUi3.BrowserView.md |

## DotNetBrowser.WinUi3.ContextMenu

Namespace page: DotNetBrowser.WinUi3.ContextMenu.md

### Classes

| Type | Summary | File |
|---|---|---|
| `MenuItemViewModel` | Represent the view model of a single menu item. | DotNetBrowser.WinUi3.ContextMenu.MenuItemViewModel.md |

## DotNetBrowser.WinUi3.Dialogs

Namespace page: DotNetBrowser.WinUi3.Dialogs.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DefaultAuthenticationHandler` | Default WinUI 3 authentication handler, which displays an authentication dialog. | DotNetBrowser.WinUi3.Dialogs.DefaultAuthenticationHandler.md |
| `DialogHandlerBase` | The base class for all dialog handlers. | DotNetBrowser.WinUi3.Dialogs.DialogHandlerBase.md |

## DotNetBrowser.WinUi3.Extensions

Namespace page: DotNetBrowser.WinUi3.Extensions.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DefaultOpenExtensionPopupHandler` | Default extension popup handler, which displays an extension popup as a separate window. | DotNetBrowser.WinUi3.Extensions.DefaultOpenExtensionPopupHandler.md |

## DotNetBrowser.Wpf

Namespace page: DotNetBrowser.Wpf.md

### Classes

| Type | Summary | File |
|---|---|---|
| `BitmapExtensions` | Extensions for `Bitmap` class. | DotNetBrowser.Wpf.BitmapExtensions.md |
| `BrowserView` | The Wpf-based implementation of browser view. | DotNetBrowser.Wpf.BrowserView.md |

## DotNetBrowser.Wpf.ContextMenu

Namespace page: DotNetBrowser.Wpf.ContextMenu.md

### Classes

| Type | Summary | File |
|---|---|---|
| `MenuItemViewModel` |  | DotNetBrowser.Wpf.ContextMenu.MenuItemViewModel.md |

## DotNetBrowser.Wpf.Dialogs

Namespace page: DotNetBrowser.Wpf.Dialogs.md

### Classes

| Type | Summary | File |
|---|---|---|
| `ColorExtensions` | Extension methods for performing color conversion. | DotNetBrowser.Wpf.Dialogs.ColorExtensions.md |
| `DefaultAuthenticationHandler` | Default Wpf authentication handler, which displays an authentication dialog. | DotNetBrowser.Wpf.Dialogs.DefaultAuthenticationHandler.md |
| `DefaultStartDownloadHandler` | The default Wpf implementation of `StartDownloadHandler`, which displays a save file dialog to specify the path to store the downloaded file. | DotNetBrowser.Wpf.Dialogs.DefaultStartDownloadHandler.md |
| `DialogHandlerBase` | The base class for all dialog handlers. | DotNetBrowser.Wpf.Dialogs.DialogHandlerBase.md |

## DotNetBrowser.Wpf.Extensions

Namespace page: DotNetBrowser.Wpf.Extensions.md

### Classes

| Type | Summary | File |
|---|---|---|
| `DefaultOpenExtensionPopupHandler` | Default extension popup handler, which displays an extension popup as a separate window. | DotNetBrowser.Wpf.Extensions.DefaultOpenExtensionPopupHandler.md |

## DotNetBrowser.Zoom

Namespace page: DotNetBrowser.Zoom.md

### Classes

| Type | Summary | File |
|---|---|---|
| `Level` | A zoom level of a web page. Provides a set of the pre-defined constants. Each constant name consists of the P prefix followed by a number. The number represents a zoom level in percents. For exampl... | DotNetBrowser.Zoom.Level.md |

### Interfaces

| Type | Summary | File |
|---|---|---|
| `IZoom` | Allows zooming content of a web page. | DotNetBrowser.Zoom.IZoom.md |
| `IZoomLevels` | Allows configuring the default zoom levels and receive notifications about zoom changes. | DotNetBrowser.Zoom.IZoomLevels.md |

### Enums

| Type | Summary | File |
|---|---|---|
| `ZoomMode` | Defines how zoom settings are stored and applied. | DotNetBrowser.Zoom.ZoomMode.md |

## DotNetBrowser.Zoom.Events

Namespace page: DotNetBrowser.Zoom.Events.md

### Classes

| Type | Summary | File |
|---|---|---|
| `LevelChangedEventArgs` | The event arguments for the `LevelChanged` event. | DotNetBrowser.Zoom.Events.LevelChangedEventArgs.md |
