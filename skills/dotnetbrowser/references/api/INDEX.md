# DotNetBrowser API index

DotNetBrowser 4.4.1, generated 2026-11-11. 588 types in 93 namespaces. Each namespace is one file: a list of its types, then every type with all of its members. Find the type below and read only the lines from the last column: `<Namespace>.md:<first>-<last>` is lines `<first>` to `<last>` of `<Namespace>.md`.

## DotNetBrowser

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IAutoDisposable` | Represents the object which can be disposed by itself (without the explicit Dispose method call). | DotNetBrowser.md:87-122 |
| `IAutoDisposable<TArgs>` | Represents the object which can be disposed by itself (without the explicit Dispose method call). | DotNetBrowser.md:124-156 |

## DotNetBrowser.AvaloniaUi

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `BitmapExtensions` | Extensions for `Bitmap` class. | DotNetBrowser.AvaloniaUi.md:19-107 |
| `BrowserView` | The Avalonia-based implementation of a browser view. | DotNetBrowser.AvaloniaUi.md:109-765 |

## DotNetBrowser.AvaloniaUi.Dialogs

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DefaultAuthenticationHandler` | Default Avalonia UI authentication handler, which displays an authentication dialog. | DotNetBrowser.AvaloniaUi.Dialogs.md:13-86 |
| `DialogHandlerBase` | The base class for all dialog handlers. | DotNetBrowser.AvaloniaUi.Dialogs.md:88-185 |

## DotNetBrowser.AvaloniaUi.Extensions

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DefaultOpenExtensionActionPopupHandler` | The default implementation of the `IHandler` interface that opens a popup window with the specified `IBrowser` instance. | DotNetBrowser.AvaloniaUi.Extensions.md:14-76 |
| `DefaultOpenExtensionPopupHandler` | Default extension popup handler, which displays an extension popup as a separate window. | DotNetBrowser.AvaloniaUi.Extensions.md:78-137 |

## DotNetBrowser.Browser

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `BitmapTimeoutException` | Thrown when a bitmap request times out. | DotNetBrowser.Browser.md:88-142 |
| `BrowserDisposeOptions` | The dispose options of the browser. | DotNetBrowser.Browser.md:144-182 |
| `BrowserViewExtensions` | Extension methods for `IBrowserView` interface. | DotNetBrowser.Browser.md:184-229 |
| `CspParameters` | The parameters describing the particular key container within a particular cryptographic service provider (CSP). | DotNetBrowser.Browser.md:231-311 |
| `UserAgentBrandVersion` | Contains the brand name and version type. | DotNetBrowser.Browser.md:313-363 |
| `UserAgentBrandVersion.Builder` | A builder class to construct `UserAgentBrandVersion`. | DotNetBrowser.Browser.md:365-461 |
| `UserAgentMetadata` | Contains the client hints data. | DotNetBrowser.Browser.md:463-621 |
| `UserAgentMetadata.Builder` | A builder class to construct `UserAgentMetadata`. | DotNetBrowser.Browser.md:623-826 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IBrowser` | A web browser control that allows loading a web page or a local HTML file, accessing DOM and executing JavaScript on the loaded web page, getting notifications about loading progress, dispatching k... | DotNetBrowser.Browser.md:828-2578 |
| `IBrowserSettings` | The settings of the browser. | DotNetBrowser.Browser.md:2580-2985 |
| `IBrowserView` | The interface that is implemented by UI components which are able to display the browser. | DotNetBrowser.Browser.md:2987-3000 |
| `IDefaultFonts` | The default fonts used by a browser. | DotNetBrowser.Browser.md:3002-3173 |
| `IOffScreenRenderProvider` | Provides access to an image rendered by the browser that works in the off-screen rendering mode. | DotNetBrowser.Browser.md:3175-3247 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `PreferredColorScheme` | The preferred color scheme for the web content in the browser. | DotNetBrowser.Browser.md:3249-3277 |
| `SavePageType` | Determines how the web page will be saved. | DotNetBrowser.Browser.md:3279-3306 |
| `WebRtcIpHandlingPolicy` | The media performance/privacy tradeoffs which affect how WebRTC traffic will be routed and how much local address information will be exposed. | DotNetBrowser.Browser.md:3308-3347 |

## DotNetBrowser.Browser.Dialogs

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IDialogs` | The browser dialogs. | DotNetBrowser.Browser.Dialogs.md:17-341 |
| `IJsDialogs` | The JavaScript dialogs. | DotNetBrowser.Browser.Dialogs.md:343-501 |

## DotNetBrowser.Browser.Dialogs.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `AlertParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.md:127-181 |
| `BeforeUnloadParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.md:183-249 |
| `BeforeUnloadResponse` | The response to the `BeforeUnloadHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:251-308 |
| `CommonDialogParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.md:310-372 |
| `ConfirmParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.md:374-440 |
| `ConfirmResponse` | The response to the `ConfirmHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:442-500 |
| `DialogParameters` | The base class for dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.md:502-546 |
| `FileChooserParameters` | The base class for the common file chooser parameters. | DotNetBrowser.Browser.Dialogs.Handlers.md:548-581 |
| `FilteredFileChooserParameters` | The base class for the common file chooser parameters. | DotNetBrowser.Browser.Dialogs.Handlers.md:583-647 |
| `OpenDirectoryParameters` | The parameters of the `OpenDirectoryHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:649-689 |
| `OpenDirectoryResponse` | The response to the `OpenDirectoryHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:691-780 |
| `OpenExternalAppParameters` | The parameters of the `OpenExternalAppHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:782-848 |
| `OpenExternalAppResponse` | The response to the `OpenExternalAppHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:850-914 |
| `OpenFileParameters` | The parameters of the `OpenFileHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:916-959 |
| `OpenFileResponse` | The response to the `OpenFileHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:961-1049 |
| `OpenMultipleFilesParameters` | The parameters of the `OpenMultipleFilesHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1051-1080 |
| `OpenMultipleFilesResponse` | The response to the `OpenMultipleFilesHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1082-1178 |
| `PromptParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.md:1180-1259 |
| `PromptResponse` | The response to the `PromptHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1261-1349 |
| `RepostFormParameters` | The base class for common dialog parameters. | DotNetBrowser.Browser.Dialogs.Handlers.md:1351-1405 |
| `RepostFormResponse` | The response to the `RepostFormHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1407-1462 |
| `SaveAsPdfParameters` | The parameters of the `SaveAsPdfHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1464-1516 |
| `SaveAsPdfResponse` | The response to the `SaveAsPdfHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1518-1606 |
| `SaveFileParameters` | The parameters of the `SaveFileHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1608-1698 |
| `SaveFileResponse` | The response to the `SaveFileHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1700-1791 |
| `SelectCertificateParameters` | The parameters of the `SelectCertificateHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1793-1860 |
| `SelectCertificateResponse` | The response to `SelectCertificateHandler` | DotNetBrowser.Browser.Dialogs.Handlers.md:1862-1973 |
| `SelectColorParameters` | The parameters for the `SelectColorHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:1975-2015 |
| `SelectColorResponse` | The response to the `SelectColorHandler`. | DotNetBrowser.Browser.Dialogs.Handlers.md:2017-2121 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `BeforeUnloadCause` | Describes the cause of the onbeforeunload dialog. | DotNetBrowser.Browser.Dialogs.Handlers.md:2123-2144 |

## DotNetBrowser.Browser.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `BrowserBecameResponsiveEventArgs` | Event arguments for the `BrowserBecameResponsive` event. | DotNetBrowser.Browser.Events.md:120-148 |
| `BrowserBecameUnresponsiveEventArgs` | Event arguments for the `BrowserBecameUnresponsive` event. | DotNetBrowser.Browser.Events.md:150-178 |
| `BrowserEventArgs` | The base class for `IBrowser` events. | DotNetBrowser.Browser.Events.md:180-244 |
| `ConsoleMessageReceivedEventArgs` | Event arguments for the `ConsoleMessageReceived` event. | DotNetBrowser.Browser.Events.md:246-336 |
| `CursorChangedEventArgs` | The `CursorChanged` event data which can be used to update the cursor for the off-screen view. | DotNetBrowser.Browser.Events.md:338-403 |
| `FaviconChangedEventArgs` | Event arguments for the `FaviconChanged` event. | DotNetBrowser.Browser.Events.md:405-447 |
| `FocusGainedEventArgs` | Event arguments for the `FocusGained` event. | DotNetBrowser.Browser.Events.md:449-477 |
| `FocusLostEventArgs` | Event arguments for the `FocusLost` event. | DotNetBrowser.Browser.Events.md:479-507 |
| `FocusRequestedEventArgs` | Event arguments for the `FocusRequested` event. | DotNetBrowser.Browser.Events.md:509-537 |
| `FrameCreatedEventArgs` | Event arguments for the `FrameCreated` event. | DotNetBrowser.Browser.Events.md:539-569 |
| `FrameDeletedEventArgs` | Event arguments for the `FrameDeleted` event. | DotNetBrowser.Browser.Events.md:571-601 |
| `FrameEventArgs` | The base class for `IBrowser` events related to `IFrame`. | DotNetBrowser.Browser.Events.md:603-651 |
| `MediaStreamCaptureStartedEventArgs` | Event arguments for the `MediaStreamCaptureStarted` | DotNetBrowser.Browser.Events.md:653-683 |
| `MediaStreamCaptureStoppedEventArgs` | Event arguments for the `MediaStreamCaptureStopped` | DotNetBrowser.Browser.Events.md:685-715 |
| `MediaStreamEventArgs` | The base class for `IBrowser` events related to media stream events. | DotNetBrowser.Browser.Events.md:717-764 |
| `PdfDocumentLoadFailedEventArgs` | Event arguments for the `PdfDocumentLoadFailed` event. | DotNetBrowser.Browser.Events.md:766-820 |
| `PdfDocumentLoadedEventArgs` | Event arguments for the `PdfDocumentLoaded` event. | DotNetBrowser.Browser.Events.md:822-876 |
| `PrintPreviewClosedEventArgs` | Event arguments for the `PrintPreviewClosed` | DotNetBrowser.Browser.Events.md:878-906 |
| `PrintPreviewOpenedEventArgs` | Event arguments for the `PrintPreviewOpened` | DotNetBrowser.Browser.Events.md:908-936 |
| `RenderProcessTerminatedEventArgs` | Event arguments for the `RenderProcessTerminated` event. | DotNetBrowser.Browser.Events.md:938-1004 |
| `SessionStartedEventArgs` | Event arguments for the `SessionStarted` event. | DotNetBrowser.Browser.Events.md:1006-1047 |
| `SpellCheckCompletedEventArgs` | Event arguments for the `SpellCheckCompleted` event. | DotNetBrowser.Browser.Events.md:1049-1105 |
| `StatusChangedEventArgs` | Event arguments for the `StatusChanged` event. | DotNetBrowser.Browser.Events.md:1107-1161 |
| `TitleChangedEventArgs` | Event arguments for the `TitleChanged` event. | DotNetBrowser.Browser.Events.md:1163-1217 |
| `UpdateBoundsRequestedEventArgs` | Event arguments for the `UpdateBoundsRequested` event. | DotNetBrowser.Browser.Events.md:1219-1258 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `ConsoleMessageReceivedEventArgs.MessageLevel` | Console message levels. | DotNetBrowser.Browser.Events.md:1260-1299 |
| `MediaStreamType` | The media type of the captured stream. | DotNetBrowser.Browser.Events.md:1301-1322 |
| `TerminationStatus` | The termination status of the render process. | DotNetBrowser.Browser.Events.md:1324-1375 |

## DotNetBrowser.Browser.FullScreen

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IFullScreen` | A service that is used for controlling the browser's fullscreen mode. | DotNetBrowser.Browser.FullScreen.md:13-85 |

## DotNetBrowser.Browser.FullScreen.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `FullScreenEnteredEventArgs` | Event arguments for the `Entered` event. | DotNetBrowser.Browser.FullScreen.Events.md:13-41 |
| `FullScreenExitedEventArgs` | Event arguments for the `Exited` event. | DotNetBrowser.Browser.FullScreen.Events.md:43-71 |

## DotNetBrowser.Browser.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `BrowserParameters` | The base class for `IBrowser` handlers parameters. | DotNetBrowser.Browser.Handlers.md:65-121 |
| `CreatePopupParameters` | The parameters of the `CreatePopupHandler`. | DotNetBrowser.Browser.Handlers.md:123-187 |
| `CreatePopupResponse` | The response to the `CreatePopupHandler`. | DotNetBrowser.Browser.Handlers.md:189-245 |
| `FrameParameters` | Represents the parameters of `IBrowser`-related handlers associated with `IFrame`. | DotNetBrowser.Browser.Handlers.md:247-294 |
| `InjectCssParameters` | The parameters of the `InjectCssHandler`. | DotNetBrowser.Browser.Handlers.md:296-324 |
| `InjectCssResponse` | The response to the `InjectCssHandler`. | DotNetBrowser.Browser.Handlers.md:326-404 |
| `InjectJsParameters` | The parameters of the `InjectJsHandler`. | DotNetBrowser.Browser.Handlers.md:406-434 |
| `OpenExtensionActionPopupParameters` | The parameters of the `OpenExtensionActionPopupHandler`. | DotNetBrowser.Browser.Handlers.md:436-487 |
| `OpenPopupParameters` | The parameters of the `OpenPopupHandler`. | DotNetBrowser.Browser.Handlers.md:489-552 |
| `RequestPdfDocumentPasswordParameters` | The parameters of the `RequestPdfDocumentPasswordHandler`. | DotNetBrowser.Browser.Handlers.md:554-595 |
| `RequestPdfDocumentPasswordResponse` | The response to the `RequestPdfDocumentPasswordHandler`. | DotNetBrowser.Browser.Handlers.md:597-693 |
| `RequestPrintParameters` | The parameters of the `RequestPrintHandler`. | DotNetBrowser.Browser.Handlers.md:695-721 |
| `RequestPrintResponse` | The response to the `RequestPrintHandler`. | DotNetBrowser.Browser.Handlers.md:723-795 |
| `ShowContextMenuParameters` | The parameters of the `ShowContextMenuHandler`. | DotNetBrowser.Browser.Handlers.md:797-987 |
| `ShowContextMenuResponse` | The response to the `ShowContextMenuHandler`. | DotNetBrowser.Browser.Handlers.md:989-1059 |

## DotNetBrowser.Cache

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IHttpAuthCache` | An HTTP Authentication cache service. | DotNetBrowser.Cache.md:13-72 |
| `IHttpCache` | An HTTP cache service. | DotNetBrowser.Cache.md:74-151 |

## DotNetBrowser.Capture

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Source` | The source for the content capture session. | DotNetBrowser.Capture.md:43-104 |
| `Sources` | Provides the access to the sources available for content capture. | DotNetBrowser.Capture.md:106-167 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `ICapture` | A service that can be used for listening and handling capturing sessions. | DotNetBrowser.Capture.md:169-251 |
| `ISession` | A content capture session. | DotNetBrowser.Capture.md:253-347 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `AudioMode` | The mode of capturing audio during the content capture session. | DotNetBrowser.Capture.md:349-370 |
| `NotificationVisibility` | Specifies whether the notification about the capture session should be shown or hidden. | DotNetBrowser.Capture.md:372-393 |
| `SourceType` | The type of the content capture source. | DotNetBrowser.Capture.md:395-422 |

## DotNetBrowser.Capture.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `SessionStoppedEventArgs` | Event arguments for the `Stopped` event. | DotNetBrowser.Capture.Events.md:9-48 |

## DotNetBrowser.Capture.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `StartSessionParameters` | The parameters of the `StartSessionHandler`. | DotNetBrowser.Capture.Handlers.md:13-88 |
| `StartSessionResponse` | A response to the `StartSessionHandler`. | DotNetBrowser.Capture.Handlers.md:90-242 |

## DotNetBrowser.Card

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `CreditCard` | The credit card information persisted in `ICreditCardStore` the credit card store. | DotNetBrowser.Card.md:34-149 |
| `CreditCard.Builder` | A builder for creating a new `CreditCard` instance. | DotNetBrowser.Card.md:151-260 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `ICreditCardStore` | A service that allows working with `CreditCard` credit cards in the Chromium credit cards store. | DotNetBrowser.Card.md:262-376 |
| `ICreditCards` | A service that allows managing credit cards. | DotNetBrowser.Card.md:378-447 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `CreditCardNetworkType` | The type of the credit card network. | DotNetBrowser.Card.md:449-530 |

## DotNetBrowser.Card.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `SaveCreditCardParameters` | The parameters of the `SaveCreditCardHandler`. | DotNetBrowser.Card.Handlers.md:13-52 |
| `SaveCreditCardResponse` | A response to the `SaveCreditCardHandler`. | DotNetBrowser.Card.Handlers.md:54-105 |

## DotNetBrowser.Cast

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `CastSessionStartFailedException` | Thrown when the cast session start has been failed. | DotNetBrowser.Cast.md:104-172 |
| `MediaRoutingException` | Thrown when the media routing is disabled. | DotNetBrowser.Cast.md:174-232 |
| `PresentationRequest` | The JavaScript | DotNetBrowser.Cast.md:234-302 |
| `ReceiverDisconnectedException` | Thrown when the receiver has been disconnected. | DotNetBrowser.Cast.md:304-356 |
| `ReceiverNotDiscoveredException` | Thrown when the receiver has not been discovered within the specified timeout. | DotNetBrowser.Cast.md:358-406 |
| `Screen` | The screen whose content can be cast. | DotNetBrowser.Cast.md:408-471 |
| `ScreenCastOptions` | Configuration options for screen casting. | DotNetBrowser.Cast.md:473-522 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `ICast` | A service that provides access for casting media on receivers. | DotNetBrowser.Cast.md:524-722 |
| `ICastSession` | A session of casting media content to a media `IMediaReceiver` receiver. | DotNetBrowser.Cast.md:724-850 |
| `ICastSessions` | A service that allows observing `IsAlive` cast `ICastSession` sessions. | DotNetBrowser.Cast.md:852-901 |
| `IMediaCasting` | A service that provides access to all the required media casting services. | DotNetBrowser.Cast.md:903-950 |
| `IMediaReceiver` | A media receiver to which media content can be cast. | DotNetBrowser.Cast.md:952-1037 |
| `IMediaReceivers` | The service that allows observing media `IMediaReceiver` receivers in the environment. | DotNetBrowser.Cast.md:1039-1191 |
| `IScreens` | The service that allows obtaining connected screens whose content can be cast. | DotNetBrowser.Cast.md:1193-1228 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `AudioMode` | The audio casting mode for the content cast session. | DotNetBrowser.Cast.md:1230-1251 |
| `CastMode` | The types of content that can be cast to a media receiver. | DotNetBrowser.Cast.md:1253-1287 |
| `MediaReceiverState` | The state of the media receiver. | DotNetBrowser.Cast.md:1289-1330 |
| `ResultCode` | Contains the codes indicating the result of creating a cast session. | DotNetBrowser.Cast.md:1332-1425 |

## DotNetBrowser.Cast.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `CastSessionDiscoveredEventArgs` | Event arguments for the `Discovered` event. | DotNetBrowser.Cast.Events.md:35-91 |
| `CastSessionStartFailedEventArgs` | Event arguments for the `StartFailed` event. | DotNetBrowser.Cast.Events.md:93-182 |
| `CastSessionStoppedEventArgs` | Event arguments for the `Stopped` event. | DotNetBrowser.Cast.Events.md:184-228 |
| `MediaReceiverDisconnectedEventArgs` | Event arguments for the `Disconnected` event. | DotNetBrowser.Cast.Events.md:230-269 |
| `MediaReceiverDiscoveredEventArgs` | Event arguments for the `Discovered` event. | DotNetBrowser.Cast.Events.md:271-322 |

## DotNetBrowser.Cast.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `StartPresentationParameters` | The parameters of the `StartPresentationHandler`. | DotNetBrowser.Cast.Handlers.md:13-81 |
| `StartPresentationResponse` | A response to the `StartPresentationHandler`. | DotNetBrowser.Cast.Handlers.md:83-144 |

## DotNetBrowser.Chromium

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `ChromiumBinariesExtractor` | A tool that is used to extract the corresponding Chromium binaries. | DotNetBrowser.Chromium.md:13-89 |
| `ChromiumInfo` | Provides information about the Chromium engine used in DotNetBrowser. | DotNetBrowser.Chromium.md:91-129 |

## DotNetBrowser.ContextMenu

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `ContextMenuItem` | A custom context menu item. | DotNetBrowser.ContextMenu.md:15-100 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `ContextMenuItemType` | The context menu item types. | DotNetBrowser.ContextMenu.md:102-135 |

## DotNetBrowser.Cookies

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Cookie` | Represents an HTTP cookie. | DotNetBrowser.Cookies.md:28-224 |
| `Cookie.Builder` | A builder class to construct cookie. | DotNetBrowser.Cookies.md:226-458 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `ICookieStore` | The system for storing and retrieving cookies. The cookies can be stored in the process memory (session cookies) or in files (persistent cookies). The `ICookieStore` instance provides access to bot... | DotNetBrowser.Cookies.md:460-647 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `SameSite` | The SameSite cookie attribute values of the Set-Cookie HTTP response header. This attribute is used to declare in which context the cookies can be sent. | DotNetBrowser.Cookies.md:649-678 |

## DotNetBrowser.DevTools

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IDevTools` | Allows working with Chromium Developer Tools and access the remote debugging URL of the currently loaded web page in the browser instance associated with this DevTools instance. | DotNetBrowser.DevTools.md:10-77 |

## DotNetBrowser.Dom

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DomException` | Thrown when an operation on the DOM element fails. | DotNetBrowser.Dom.md:103-159 |
| `PointInspection` | Provides information about a DOM node at the specified point inside the loaded document. | DotNetBrowser.Dom.md:161-247 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IAttribute` | This interface is implemented by all `INode` implementations to support DOM event model. | DotNetBrowser.Dom.md:249-286 |
| `IAttributes` | A dictionary that contains `IElement` attributes. Modifying this dictionary will lead to modifying the element attributes. | DotNetBrowser.Dom.md:288-329 |
| `IDocument` | Represents DOM HTML document of the web page. | DotNetBrowser.Dom.md:331-607 |
| `IElement` | This interface is implemented by all `INode` implementations to support DOM event model. | DotNetBrowser.Dom.md:609-859 |
| `IFormControlElement` | Represents the form control element. | DotNetBrowser.Dom.md:861-938 |
| `IFormElement` | Represents DOM HTML Form element. | DotNetBrowser.Dom.md:940-1061 |
| `IFrameElement` | Represents an HTML <frame> or <iframe> element. | DotNetBrowser.Dom.md:1063-1100 |
| `IImageElement` | Represents DOM HTML image element <img>. | DotNetBrowser.Dom.md:1102-1144 |
| `IInputElement` | Represents the DOM element with <input> tag. | DotNetBrowser.Dom.md:1146-1377 |
| `INode` | This interface is implemented by all `INode` implementations to support DOM event model. | DotNetBrowser.Dom.md:1379-1697 |
| `INodeCollection` | Represents a collection of the DOM nodes. | DotNetBrowser.Dom.md:1699-1877 |
| `IOptionElement` | Represents the DOM HTML <option> element. | DotNetBrowser.Dom.md:1879-1916 |
| `ISearchContext` | The base interface for search that is implemented by the DOM objects that provide search mechanisms. | DotNetBrowser.Dom.md:1918-2217 |
| `ISelectElement` | Represents DOM HTML <select> element. | DotNetBrowser.Dom.md:2219-2275 |
| `ITextAreaElement` | Represents DOM HTML <textarea> element. | DotNetBrowser.Dom.md:2277-2295 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `AlignTo` | Represents the values that can be used to describe how the element will be aligned to the visible area of the scrollable ancestor. | DotNetBrowser.Dom.md:2297-2325 |
| `DocumentPosition` | Enumeration of the document position that represent the relationship between two nodes within the Document. | DotNetBrowser.Dom.md:2327-2374 |
| `NodeType` | Represents the node types that can be used to distinguish different kind of nodes (such as an HTML element, text, attribute) from each other. | DotNetBrowser.Dom.md:2376-2441 |

## DotNetBrowser.Dom.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DomEventArgs` | The common DOM event arguments. | DotNetBrowser.Dom.Events.md:114-153 |
| `Event` | Represents a DOM event that can be handled on the .NET side. | DotNetBrowser.Dom.Events.md:155-293 |
| `EventParameters` | The parameters of creating the DOM event. | DotNetBrowser.Dom.Events.md:295-346 |
| `EventParameters.Builder` | The `EventParameters` builder. | DotNetBrowser.Dom.Events.md:348-415 |
| `EventType` | The DOM event type. Wraps a string that specifies the name of the event without the "on" prefix. | DotNetBrowser.Dom.Events.md:417-873 |
| `KeyEventParameters` | Represents the DOM keyboard event parameters. | DotNetBrowser.Dom.Events.md:875-937 |
| `MouseEventParameters` | Represents the DOM mouse event parameters. | DotNetBrowser.Dom.Events.md:939-1027 |
| `UiEventModifierParameters` | Represents the DOM UI event parameters with the key modifiers. | DotNetBrowser.Dom.Events.md:1029-1079 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IEvent` | Represents DOM Event object and provides access to the event object data. | DotNetBrowser.Dom.Events.md:1081-1188 |
| `IEventTarget` | This interface is implemented by all `INode` implementations to support DOM event model. | DotNetBrowser.Dom.Events.md:1190-1247 |
| `IEvents` | A collection of custom DOM events that can be listened and/or handled. | DotNetBrowser.Dom.Events.md:1249-1759 |
| `IKeyEvent` | Represents a keyboard event and provides an access to specific keyboard event data. | DotNetBrowser.Dom.Events.md:1761-1807 |
| `IMouseEvent` | Represents a mouse event and provides an access to specific mouse event data. | DotNetBrowser.Dom.Events.md:1809-1903 |
| `ITouchEvent` | Represents a touch event and provides an access to specific touch event data. | DotNetBrowser.Dom.Events.md:1905-1962 |
| `IUiKeyEventModifier` | Represents a DOM UI event that can be fired with the key modifiers. | DotNetBrowser.Dom.Events.md:1964-1998 |
| `IWheelEvent` | A wheel event that provides access to the wheel event data. | DotNetBrowser.Dom.Events.md:2000-2056 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `DeltaMode` | The type of the delta units. | DotNetBrowser.Dom.Events.md:2058-2085 |
| `DomKeyCode` | The DOM key codes represent physical keys on the keyboard (as opposed to the character generated by pressing the key). In other words, these values are not altered by keyboard layout or the state o... | DotNetBrowser.Dom.Events.md:2087-3526 |
| `DomMouseButton` | A DOM mouse button. | DotNetBrowser.Dom.Events.md:3528-3573 |
| `EventPhase` | Represents the DOM event phases. | DotNetBrowser.Dom.Events.md:3575-3602 |

## DotNetBrowser.Dom.XPath

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `XPathException` | This exception is thrown if XPath evaluation error occurs. | DotNetBrowser.Dom.XPath.md:21-77 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IXPathResult` | Represents the result of the XPath expression evaluation. | DotNetBrowser.Dom.XPath.md:79-177 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `XPathResultType` | Represents the XPath result types. | DotNetBrowser.Dom.XPath.md:179-253 |

## DotNetBrowser.Downloads

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DownloadInfo` | The general information about the download. | DotNetBrowser.Downloads.md:31-92 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IDownload` | Represents a download. | DotNetBrowser.Downloads.md:94-323 |
| `IDownloads` | A service that can be used to work with the downloads. | DotNetBrowser.Downloads.md:325-374 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `DownloadState` | The download state. | DotNetBrowser.Downloads.md:376-409 |

## DotNetBrowser.Downloads.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `CanceledEventArgs` | Event arguments for the `Canceled` event. | DotNetBrowser.Downloads.Events.md:35-62 |
| `DownloadEventArgs` | The base class for `IDownload` events. | DotNetBrowser.Downloads.Events.md:64-112 |
| `FinishedEventArgs` | Event arguments for the `Finished` event. | DotNetBrowser.Downloads.Events.md:114-141 |
| `InterruptedEventArgs` | Event arguments for the `Interrupted` event. | DotNetBrowser.Downloads.Events.md:143-184 |
| `PausedEventArgs` | Event arguments for the `Paused` event. | DotNetBrowser.Downloads.Events.md:186-213 |
| `UpdatedEventArgs` | Event arguments for the `Updated` event. | DotNetBrowser.Downloads.Events.md:215-293 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `DownloadInterruptionReason` | Possible download interruption reason. | DotNetBrowser.Downloads.Events.md:295-508 |

## DotNetBrowser.Downloads.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `StartDownloadParameters` | The parameters of the `StartDownloadHandler`. | DotNetBrowser.Downloads.Handlers.md:13-52 |
| `StartDownloadResponse` | A response to the `StartDownloadHandler`. | DotNetBrowser.Downloads.Handlers.md:54-123 |

## DotNetBrowser.Engine

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `AutoDeElevationException` | Thrown when Chromium is launched with admin permissions on Windows and restarts itself without them, which DotNetBrowser does not support. | DotNetBrowser.Engine.md:109-162 |
| `BinariesExtractionOptions` | The options that are used to configure the Chromium binaries extraction process. | DotNetBrowser.Engine.md:164-280 |
| `ChromiumBinariesMissingException` | Thrown when the engine initialization fails due to missing compatible Chromium binaries. | DotNetBrowser.Engine.md:282-341 |
| `ConnectionClosedException` | The exception thrown when the connection to the Chromium engine appears to be closed. | DotNetBrowser.Engine.md:343-387 |
| `EngineFactory` | Factory class that is used to create `IEngine` instances. | DotNetBrowser.Engine.md:389-603 |
| `EngineInitializationException` | The base class for those exceptions that can be thrown during `IEngine` initialization. | DotNetBrowser.Engine.md:605-689 |
| `EngineOptions` | The options that are used to configure `IEngine` instances. | DotNetBrowser.Engine.md:691-1193 |
| `EngineOptions.Builder` | A builder class to construct engine options. | DotNetBrowser.Engine.md:1195-1719 |
| `InvalidLicenseException` | Thrown when the given license is invalid. | DotNetBrowser.Engine.md:1721-1777 |
| `LicenseException` | The base class for those exceptions that can be thrown during license checking. | DotNetBrowser.Engine.md:1779-1844 |
| `MissingDependencyException` | Thrown when Chromium fails to find the required system libraries on Linux. | DotNetBrowser.Engine.md:1846-1897 |
| `NoLicenseException` | Thrown when no license found. | DotNetBrowser.Engine.md:1899-1951 |
| `PasswordStore` | Defines password store types that are used to specify which encryption storage backend to use to encrypt cookies on Linux. | DotNetBrowser.Engine.md:1953-2098 |
| `SandboxNotSupportedException` | Thrown when the current environment does not support creating processes within a new user namespace, preventing Chromium from being launched in sandbox mode. | DotNetBrowser.Engine.md:2100-2154 |
| `UserDataCreationException` | Thrown when the user data directory cannot be created. | DotNetBrowser.Engine.md:2156-2226 |
| `UserDataInUseException` | Thrown when the user data directory is already in use by another Chromium engine instance. | DotNetBrowser.Engine.md:2228-2297 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IEngine` | Provides access to the Chromium engine functionality. | DotNetBrowser.Engine.md:2299-2464 |
| `IWidevine` | The Widevine DRM (Digital Rights Management) component. | DotNetBrowser.Engine.md:2466-2613 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `BinariesVerificationLevel` | The level of the Chromium binaries verification. | DotNetBrowser.Engine.md:2615-2650 |
| `ProprietaryFeatures` | The list of supported proprietary features. | DotNetBrowser.Engine.md:2652-2704 |
| `RenderingMode` | The supported rendering modes. | DotNetBrowser.Engine.md:2706-2727 |
| `Theme` | The Chromium theme, which affects the appearanceof web pages and their contents, as well as Chromium dialogs, such as Print Preview and DevTools. | DotNetBrowser.Engine.md:2729-2757 |
| `WidevineActivationStatus` | Represents the result of attempting to activate the Widevine component. | DotNetBrowser.Engine.md:2759-2797 |

## DotNetBrowser.Engine.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `EngineDisposedEventArgs` | The event arguments for the event indicating that the `IEngine` has been disposed. | DotNetBrowser.Engine.Events.md:9-61 |

## DotNetBrowser.Extensions

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `ExtensionInstallationException` | Thrown when the extension installation has failed for some reason. | DotNetBrowser.Extensions.md:53-109 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IExtension` | A Chromium extension. | DotNetBrowser.Extensions.md:111-323 |
| `IExtensionAction` | The extension action is a clickable extension icon. | DotNetBrowser.Extensions.md:325-522 |
| `IExtensions` | A service that allows managing extensions. | DotNetBrowser.Extensions.md:524-733 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `ExtensionActionType` | The extension action type. | DotNetBrowser.Extensions.md:735-762 |
| `ExtensionPermission` | The extension permission types. | DotNetBrowser.Extensions.md:764-1211 |

## DotNetBrowser.Extensions.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `ExtensionActionUpdatedEventArgs` | Event arguments for the `Updated` event. | DotNetBrowser.Extensions.Events.md:25-76 |
| `ExtensionEventArgs` | The base class for the extension-related event arguments. | DotNetBrowser.Extensions.Events.md:78-123 |
| `ExtensionInstalledEventArgs` | Event arguments for the `ExtensionInstalled` event. | DotNetBrowser.Extensions.Events.md:125-152 |
| `ExtensionUninstalledEventArgs` | Event arguments for the `ExtensionUninstalled` event. | DotNetBrowser.Extensions.Events.md:154-193 |
| `ExtensionUpdatedEventArgs` | Event arguments for the `ExtensionUpdated` event. | DotNetBrowser.Extensions.Events.md:195-222 |

## DotNetBrowser.Extensions.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `InstallExtensionParameters` | The parameters of the `InstallExtensionHandler`. | DotNetBrowser.Extensions.Handlers.md:25-146 |
| `InstallExtensionResponse` | The response to the `InstallExtensionHandler`. | DotNetBrowser.Extensions.Handlers.md:148-199 |
| `OpenExtensionPopupParameters` | The parameters of the `OpenExtensionPopupHandler`. | DotNetBrowser.Extensions.Handlers.md:201-262 |
| `UninstallExtensionParameters` | The parameters of the `UninstallExtensionHandler`. | DotNetBrowser.Extensions.Handlers.md:264-301 |
| `UninstallExtensionResponse` | The response to the `UninstallExtensionHandler`. | DotNetBrowser.Extensions.Handlers.md:303-354 |

## DotNetBrowser.Frames

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `EditorCommand` | Provides the supported commands that can be executed in a `IFrame`. | DotNetBrowser.Frames.md:44-906 |
| `WebStorageException` | Thrown by `IWebStorage` properties and methods to indicate that the requested operation failed. This is a superclass of the exceptions that can be thrown during working with `IWebStorage`. | DotNetBrowser.Frames.md:908-968 |
| `WebStorageOverflowException` | Thrown by `IWebStorage` indexer if the new value size exceeds the available space in the storage. | DotNetBrowser.Frames.md:970-1026 |
| `WebStorageSecurityException` | Thrown by `IWebStorage` methods if the access to the web storage is forbidden for the current document. | DotNetBrowser.Frames.md:1028-1084 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IFrame` | Represents a frame in the browser. Each web page loaded in the browser has a main(top-level) frame. The frame itself may have child frames. When a web page is unloaded, its frame and all child fram... | DotNetBrowser.Frames.md:1086-1764 |
| `IWebStorage` | An HTML WebStorage. Provides access to the session storage or local storage for a particular document on the loaded web page. Allows you to add, modify, or delete the stored items. | DotNetBrowser.Frames.md:1766-1926 |

## DotNetBrowser.Frames.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `ConvertJsNameParameters` | The parameters of the `ConvertJsNameHandler`. | DotNetBrowser.Frames.Handlers.md:13-54 |
| `ConvertJsNameResponse` | The response to the `ConvertJsNameHandler`. | DotNetBrowser.Frames.Handlers.md:56-149 |

## DotNetBrowser.Geometry

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Ellipse` | Represents a three numbers that are used to define ellipse size and orientation in the two-dimensional space. | DotNetBrowser.Geometry.md:24-137 |
| `Point` | Represents a pair of numbers that in general are used to define coordinates in the two-dimensional space. | DotNetBrowser.Geometry.md:139-260 |
| `Rectangle` | Represents a rectangle described by the location and dimensions. | DotNetBrowser.Geometry.md:262-460 |
| `Size` | Represents a pair of numbers that in general are used to define dimensions in the two-dimensional space. | DotNetBrowser.Geometry.md:462-616 |

## DotNetBrowser.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `AsyncHandler<TParameters, TResponse>` | The default implementation of the `IHandler` interface. | DotNetBrowser.Handlers.md:27-110 |
| `Handler<TParameters, TResponse>` | The default implementation of the `IHandler` interface. | DotNetBrowser.Handlers.md:112-223 |
| `Handler<TParameters>` | The default implementation of the `IHandler` interface. | DotNetBrowser.Handlers.md:225-325 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IHandler<TParameters, TResponse>` | The common interface for all handlers. | DotNetBrowser.Handlers.md:327-370 |
| `IHandler<TParameters>` | The common interface for all handlers that must be executed synchronously, but do not have to return a value. | DotNetBrowser.Handlers.md:372-404 |

## DotNetBrowser.Input

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IInputEvent<TIInputEventArgs, TInputEventArgs>` | An input event. It is possible to raise this input event and dispatch it to the currently loaded web page. | DotNetBrowser.Input.md:36-78 |
| `IInterceptableEvent<TIInputEventArgs>` | An interceptable input event. It is possible to intercept and suppress this input event before it is actually processed by the browser. | DotNetBrowser.Input.md:80-110 |
| `IInterceptableInputEvent<TIInputEventArgs, TInputEventArgs>` | An interceptable and raisable input event. It is possible to intercept and suppress this input event before it is actually processed by the browser or to raise it and dispatch to the currently load... | DotNetBrowser.Input.md:112-138 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `InputEventResponse` | The response to the input event handlers. | DotNetBrowser.Input.md:140-161 |

## DotNetBrowser.Input.DragAndDrop

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IDragAndDrop` | The drag and drop functionality of the browser. | DotNetBrowser.Input.DragAndDrop.md:13-118 |

## DotNetBrowser.Input.DragAndDrop.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DragAndDropParameters` | The base class for all `IDragAndDrop` handlers parameters. | DotNetBrowser.Input.DragAndDrop.Handlers.md:21-76 |
| `DragEvent` | Represents drag and drop event and provides access to the event data. | DotNetBrowser.Input.DragAndDrop.Handlers.md:78-158 |
| `DropParameters` | The parameters of the `DropHandler`. | DotNetBrowser.Input.DragAndDrop.Handlers.md:160-187 |
| `EnterDragParameters` | The parameters of the `EnterDragHandler`. | DotNetBrowser.Input.DragAndDrop.Handlers.md:189-215 |

## DotNetBrowser.Input.Keyboard

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IKeyboard` | A service that can be used for keyboard input simulation and handling. | DotNetBrowser.Input.Keyboard.md:13-84 |

## DotNetBrowser.Input.Keyboard.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `KeyCharEventArgs` | The event arguments for key events which provide a character. | DotNetBrowser.Input.Keyboard.Events.md:61-163 |
| `KeyEventArgs` |  | DotNetBrowser.Input.Keyboard.Events.md:165-281 |
| `KeyModifiers` |  | DotNetBrowser.Input.Keyboard.Events.md:283-396 |
| `KeyPressedEventArgs` | The event arguments for the `KeyPressed` event. | DotNetBrowser.Input.Keyboard.Events.md:398-437 |
| `KeyReleasedEventArgs` | The event arguments for the `KeyReleased` event. | DotNetBrowser.Input.Keyboard.Events.md:439-473 |
| `KeyTypedEventArgs` | The event arguments for the `KeyTyped` event. | DotNetBrowser.Input.Keyboard.Events.md:475-514 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IKeyCharEventArgs` | The event arguments for key events which provide a character. | DotNetBrowser.Input.Keyboard.Events.md:516-543 |
| `IKeyEventArgs` | The base interface of all event arguments for the key events. | DotNetBrowser.Input.Keyboard.Events.md:545-592 |
| `IKeyModifiers` | The keyboard modifiers applied. | DotNetBrowser.Input.Keyboard.Events.md:594-665 |
| `IKeyPressedEventArgs` | The event arguments for the `KeyPressed` event. | DotNetBrowser.Input.Keyboard.Events.md:667-681 |
| `IKeyReleasedEventArgs` | The event arguments for the `KeyReleased` event. | DotNetBrowser.Input.Keyboard.Events.md:683-696 |
| `IKeyTypedEventArgs` | The event arguments for the `KeyTyped` event. | DotNetBrowser.Input.Keyboard.Events.md:698-712 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `KeyCode` | The virtual key codes. | DotNetBrowser.Input.Keyboard.Events.md:714-1805 |
| `KeyLocation` | The key location on the keyboard. | DotNetBrowser.Input.Keyboard.Events.md:1807-1840 |

## DotNetBrowser.Input.Mouse

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `MouseExtensions` | The mouse input simulation service extension methods. | DotNetBrowser.Input.Mouse.md:19-102 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IMouse` | A service that can be used for mouse input simulation and handling. | DotNetBrowser.Input.Mouse.md:104-250 |

## DotNetBrowser.Input.Mouse.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `MouseButtonEventArgs` | Event arguments for the `IMouse` events associated with a mouse button. | DotNetBrowser.Input.Mouse.Events.md:93-183 |
| `MouseDraggedEventArgs` | The event arguments for the `Dragged` event. | DotNetBrowser.Input.Mouse.Events.md:185-256 |
| `MouseEnteredEventArgs` | The event arguments for the `Entered` event. | DotNetBrowser.Input.Mouse.Events.md:258-329 |
| `MouseEventArgs` |  | DotNetBrowser.Input.Mouse.Events.md:331-439 |
| `MouseExitedEventArgs` | The event arguments for the `Exited` event. | DotNetBrowser.Input.Mouse.Events.md:441-512 |
| `MouseModifiers` |  | DotNetBrowser.Input.Mouse.Events.md:514-627 |
| `MouseMovedEventArgs` | The event arguments for the `Moved` event. | DotNetBrowser.Input.Mouse.Events.md:629-700 |
| `MousePressedEventArgs` | The event arguments for the `Pressed` event. | DotNetBrowser.Input.Mouse.Events.md:702-741 |
| `MouseReleasedEventArgs` | The event arguments for the `Released` event. | DotNetBrowser.Input.Mouse.Events.md:743-782 |
| `MouseWheelMovedEventArgs` | The event arguments for the `WheelMoved` event. | DotNetBrowser.Input.Mouse.Events.md:784-893 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IMouseButtonEventArgs` | Event arguments for the `IMouse` events associated with a mouse button. | DotNetBrowser.Input.Mouse.Events.md:895-958 |
| `IMouseDraggedEventArgs` | The event arguments for the `Dragged` event. | DotNetBrowser.Input.Mouse.Events.md:960-1011 |
| `IMouseEnteredEventArgs` | The event arguments for the `Entered` event. | DotNetBrowser.Input.Mouse.Events.md:1013-1064 |
| `IMouseEventArgs` | The base interface for all `IMouse` event arguments. | DotNetBrowser.Input.Mouse.Events.md:1066-1101 |
| `IMouseExitedEventArgs` | The event arguments for the `Exited` event. | DotNetBrowser.Input.Mouse.Events.md:1103-1154 |
| `IMouseModifiers` | The mouse modifiers indicating which mouse buttons are currently pressed. | DotNetBrowser.Input.Mouse.Events.md:1156-1227 |
| `IMouseMovedEventArgs` | The event arguments for the `Moved` event. | DotNetBrowser.Input.Mouse.Events.md:1229-1280 |
| `IMousePressedEventArgs` | The event arguments for the `Pressed` event. | DotNetBrowser.Input.Mouse.Events.md:1282-1296 |
| `IMouseReleasedEventArgs` | The event arguments for the `Released` event. | DotNetBrowser.Input.Mouse.Events.md:1298-1312 |
| `IMouseWheelMovedEventArgs` | The event arguments for the `WheelMoved` event. | DotNetBrowser.Input.Mouse.Events.md:1314-1377 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `MouseButton` | The mouse buttons. | DotNetBrowser.Input.Mouse.Events.md:1379-1430 |
| `MouseScrollType` | Scroll type. | DotNetBrowser.Input.Mouse.Events.md:1432-1453 |

## DotNetBrowser.Input.Touch

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `ITouch` | A service that can be used for touch input handling. | DotNetBrowser.Input.Touch.md:13-100 |

## DotNetBrowser.Input.Touch.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `TouchCanceledEventArgs` |  | DotNetBrowser.Input.Touch.Events.md:33-113 |
| `TouchEndedEventArgs` |  | DotNetBrowser.Input.Touch.Events.md:115-195 |
| `TouchEventArgs` |  | DotNetBrowser.Input.Touch.Events.md:197-304 |
| `TouchMovedEventArgs` |  | DotNetBrowser.Input.Touch.Events.md:306-386 |
| `TouchPoint` |  | DotNetBrowser.Input.Touch.Events.md:388-580 |
| `TouchStartedEventArgs` |  | DotNetBrowser.Input.Touch.Events.md:582-662 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `ITouchEventArgs` | Event arguments for the `ITouch` events associated with a surface touch. | DotNetBrowser.Input.Touch.Events.md:664-699 |
| `ITouchPoint` | A single contact point on a touch-sensitive device. | DotNetBrowser.Input.Touch.Events.md:701-803 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `TouchState` | The possible states of the touch point. | DotNetBrowser.Input.Touch.Events.md:805-850 |

## DotNetBrowser.Js

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `JsException` | Thrown when an exception is raised in JavaScript. | DotNetBrowser.Js.md:55-95 |
| `JsonExtensions` | Contains methods for working with JSON strings | DotNetBrowser.Js.md:97-219 |
| `PropertyUpdateException` | Thrown when a property update fails. | DotNetBrowser.Js.md:221-263 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IJsFunction` | A JavaScript function that can be passed between .NET and JavaScript as a method argument or a return value. The function lifetime is bound to the lifetime of the frame this function belongs to. Wh... | DotNetBrowser.Js.md:265-478 |
| `IJsObject` | Represents a JavaScript object. Provides access to the object's properties and functions. The JavaScript object is alive until its JavaScript execution context exist. Once execution context is disp... | DotNetBrowser.Js.md:480-709 |
| `IJsObjectPropertyCollection` | The JavaScript object properties. | DotNetBrowser.Js.md:711-1078 |
| `IJsPromise` | The JavaScript Promise. | DotNetBrowser.Js.md:1080-1322 |
| `IJsSymbol` | Represent a JavaScript "Symbol". JavaScript symbols are unique and immutable primitive values that may be used as the key of an object property. Symbols are often used to add unique property keys t... | DotNetBrowser.Js.md:1324-1356 |

## DotNetBrowser.Js.Collections

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IJsArray` | A JavaScript array. | DotNetBrowser.Js.Collections.md:21-151 |
| `IJsArrayBuffer` | A JavaScript array buffer. | DotNetBrowser.Js.Collections.md:153-211 |
| `IJsMap` | A JavaScript map. | DotNetBrowser.Js.Collections.md:213-406 |
| `IJsSet` | A JavaScript set. | DotNetBrowser.Js.Collections.md:408-608 |

## DotNetBrowser.Logging

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `LoggerProvider` | Provides access to different DotNetBrowser Loggers which are used to log Browser, IPC and Chromium process messages. | DotNetBrowser.Logging.md:10-146 |

## DotNetBrowser.Media

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `MediaDevice` | The details of the media input device (audio/video). | DotNetBrowser.Media.md:36-97 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IAudio` | Allows controlling audio on the loaded web page and receive notifications when audio has been started or stopped playing. | DotNetBrowser.Media.md:99-199 |
| `IMediaDevices` | An engine service that allows accessing all the available media input devices. | DotNetBrowser.Media.md:201-297 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `MediaDeviceType` | The media device types. | DotNetBrowser.Media.md:299-326 |
| `MediaType` | List of the known media types. It's used in `ShowContextMenuParameters`. | DotNetBrowser.Media.md:328-379 |

## DotNetBrowser.Media.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `AudioEventArgs` | The base class for `IAudio` related events. | DotNetBrowser.Media.Events.md:17-64 |
| `AudioPlaybackStartedEventArgs` | Event arguments for the `AudioPlaybackStarted` event. | DotNetBrowser.Media.Events.md:66-95 |
| `AudioPlaybackStoppedEventArgs` | Event arguments for the `AudioPlaybackStopped` event. | DotNetBrowser.Media.Events.md:97-126 |

## DotNetBrowser.Media.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `SelectMediaDeviceParameters` | The parameters of the `SelectMediaDeviceHandler`. | DotNetBrowser.Media.Handlers.md:13-75 |
| `SelectMediaDeviceResponse` | A response to the `SelectMediaDeviceHandler`. | DotNetBrowser.Media.Handlers.md:77-172 |

## DotNetBrowser.Navigation

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `LoadUrlParameters` | The parameters of the load url request. | DotNetBrowser.Navigation.md:39-134 |
| `NavigationResult` | The result of the navigation occurred. | DotNetBrowser.Navigation.md:136-212 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `INavigation` | Allows loading resources in the browser instance and working with the navigation history. | DotNetBrowser.Navigation.md:214-1036 |
| `INavigationEntry` | The navigation history entry. | DotNetBrowser.Navigation.md:1038-1121 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `LoadResult` | The loading result. | DotNetBrowser.Navigation.md:1123-1174 |
| `PageType` | Represents a navigation page type. | DotNetBrowser.Navigation.md:1176-1197 |

## DotNetBrowser.Navigation.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `FrameDocumentLoadFinishedEventArgs` | Event arguments for the `FrameDocumentLoadFinished` event. | DotNetBrowser.Navigation.Events.md:54-85 |
| `FrameLoadFailedEventArgs` | Event arguments for the `FrameLoadFailed` event. | DotNetBrowser.Navigation.Events.md:87-144 |
| `FrameLoadFinishedEventArgs` | Event arguments for the `FrameLoadFinished` event. | DotNetBrowser.Navigation.Events.md:146-191 |
| `FrameNavigationEventArgs` | The base class for all the `INavigation` event arguments containing `IFrame`. | DotNetBrowser.Navigation.Events.md:193-244 |
| `LoadFinishedEventArgs` | Event arguments for the `LoadFinished` event. | DotNetBrowser.Navigation.Events.md:246-275 |
| `LoadProgressChangedEventArgs` | Event arguments for the `LoadProgressChanged` event. | DotNetBrowser.Navigation.Events.md:277-319 |
| `LoadStartedEventArgs` | Event arguments for the `LoadStarted` event. | DotNetBrowser.Navigation.Events.md:321-350 |
| `NavigationEventArgs` | The base class for `INavigation` event arguments. | DotNetBrowser.Navigation.Events.md:352-414 |
| `NavigationFinishedEventArgs` | Event arguments for the `NavigationFinished` event. | DotNetBrowser.Navigation.Events.md:416-583 |
| `NavigationRedirectedEventArgs` | Event arguments for the `NavigationRedirected` event. | DotNetBrowser.Navigation.Events.md:585-628 |
| `NavigationStartedEventArgs` | The event arguments for the `NavigationStarted` event. | DotNetBrowser.Navigation.Events.md:630-697 |
| `NavigationStoppedEventArgs` | Event arguments for the `NavigationStopped` event. | DotNetBrowser.Navigation.Events.md:699-728 |

## DotNetBrowser.Navigation.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `NavigationParameters` | The base class for all `INavigation` handlers parameters. | DotNetBrowser.Navigation.Handlers.md:33-77 |
| `ShowHttpErrorPageParameters` | The parameters of the `ShowHttpErrorPageHandler`. | DotNetBrowser.Navigation.Handlers.md:79-130 |
| `ShowHttpErrorPageResponse` | A response to the `ShowHttpErrorPageHandler`. | DotNetBrowser.Navigation.Handlers.md:132-201 |
| `ShowNetErrorPageParameters` | The parameters of the `ShowNetErrorPageHandler`. | DotNetBrowser.Navigation.Handlers.md:203-254 |
| `ShowNetErrorPageResponse` | A response to the `ShowNetErrorPageHandler`. | DotNetBrowser.Navigation.Handlers.md:256-325 |
| `StartNavigationParameters` | The parameters of the `StartNavigationHandler`. | DotNetBrowser.Navigation.Handlers.md:327-427 |
| `StartNavigationResponse` | A response to the `StartNavigationHandler`. | DotNetBrowser.Navigation.Handlers.md:429-484 |

## DotNetBrowser.Net

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `BytesData` | The upload data as bytes. Can be empty if the form doesn't contain any data. | DotNetBrowser.Net.md:120-202 |
| `FileValue` |  | DotNetBrowser.Net.md:204-342 |
| `FormData` | The list of key-value pairs each representing a segment of a form data. Can be empty if the form doesn't contain any data. | DotNetBrowser.Net.md:344-404 |
| `HostPortPair` | A host/port pair of the URI. | DotNetBrowser.Net.md:406-501 |
| `HttpHeader` |  | DotNetBrowser.Net.md:503-574 |
| `MimeType` | The MIME type. | DotNetBrowser.Net.md:576-814 |
| `MultipartFormData` | The list of key-value pairs each representing a segment of a multi-part form data. Can be empty if the form doesn't contain any data. | DotNetBrowser.Net.md:816-876 |
| `MultipartFormDataKeyValuePair` | A key-value pair that represents a segment of a multi-part form data. Can contain values corresponding a form field content, an upload file content, etc. | DotNetBrowser.Net.md:878-1000 |
| `Scheme` | The scheme component of a URL. | DotNetBrowser.Net.md:1002-1110 |
| `TextData` | The upload data of the text/plain content type. | DotNetBrowser.Net.md:1112-1193 |
| `UploadData` | The base class for all upload data. | DotNetBrowser.Net.md:1195-1230 |
| `UrlRequest` | Represents the URL request received from the Chromium engine. | DotNetBrowser.Net.md:1232-1370 |
| `UrlRequestJob` | The URL request job for the intercepted URL request, which allows you to provide the response data for this URL request. | DotNetBrowser.Net.md:1372-1604 |
| `UrlRequestJobExtensions` | Provides extension methods for `UrlRequestJob`. | DotNetBrowser.Net.md:1606-1725 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IFileValue` | File data. | DotNetBrowser.Net.md:1727-1804 |
| `IHttpAuthPreferences` | The HTTP authorization preferences. | DotNetBrowser.Net.md:1806-1855 |
| `IHttpHeader` | Represents the single HTTP header with all its values. | DotNetBrowser.Net.md:1857-1892 |
| `INetwork` | Allows access and modifying to the network-level activities. | DotNetBrowser.Net.md:1894-2519 |
| `IUploadData` | The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`, `application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the ... | DotNetBrowser.Net.md:2521-2534 |
| `IUploadData<T>` | The upload data associated with a `UrlRequest`. The upload data can be in the `text/plain`, `application/x-www-form-urlencoded`, or `multipart/form-data` format.The upload data type depends on the ... | DotNetBrowser.Net.md:2536-2573 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `NetError` | The network errors. | DotNetBrowser.Net.md:2575-4242 |
| `RequestStatus` | The status of a URL request. | DotNetBrowser.Net.md:4244-4284 |
| `SslVersion` | The supported SSL connection versions. | DotNetBrowser.Net.md:4286-4343 |

## DotNetBrowser.Net.Certificates

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Certificate` | Provides information about the digital certificate. This certificate represents a X.509 certificate, which consists of a particular identity or end-entity certificate, such as an server identity or... | DotNetBrowser.Net.Certificates.md:26-303 |
| `CertificateVerificationError` | Provides information about an error found by Chromium when verifying an SSL certificate. | DotNetBrowser.Net.Certificates.md:305-397 |
| `ExtendedKeyUsage` | Defines how the certificate key can be used. | DotNetBrowser.Net.Certificates.md:399-555 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `CertificateVerificationStatus` | The status that indicates result of SSL certificate verification by default Chromium certificate verifier. | DotNetBrowser.Net.Certificates.md:557-673 |

## DotNetBrowser.Net.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `ConnectionTypeChangedEventArgs` | Event arguments for the `ConnectionTypeChanged` event. | DotNetBrowser.Net.Events.md:43-82 |
| `NetworkEventArgs` | The base class for `INetwork` event arguments. | DotNetBrowser.Net.Events.md:84-132 |
| `PacScriptErrorEventArgs` | Event arguments for the `PacScriptErrorOccurred` event. | DotNetBrowser.Net.Events.md:134-183 |
| `RedirectResponseCodeReceivedEventArgs` | Event arguments for the `RedirectResponseCodeReceived` event. | DotNetBrowser.Net.Events.md:185-238 |
| `RequestCompletedEventArgs` | Event arguments for the `RequestCompleted` event. | DotNetBrowser.Net.Events.md:240-318 |
| `RequestDestroyedEventArgs` | Event arguments for the `RequestDestroyed` event. | DotNetBrowser.Net.Events.md:320-347 |
| `ResponseBytesReceivedEventArgs` | Event arguments for the `ResponseBytesReceived` event. | DotNetBrowser.Net.Events.md:349-402 |
| `ResponseStartedEventArgs` | Event arguments for the `ResponseStarted` event. | DotNetBrowser.Net.Events.md:404-447 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `ConnectionType` | The network connection type. | DotNetBrowser.Net.Events.md:449-512 |

## DotNetBrowser.Net.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `AuthenticateParameters` | The parameters of the `AuthenticateHandler`. | DotNetBrowser.Net.Handlers.md:104-216 |
| `AuthenticateResponse` | A response for the `AuthenticateHandler`. | DotNetBrowser.Net.Handlers.md:218-310 |
| `CanAccessFileParameters` | The parameters of the `CanAccessFileHandler`. | DotNetBrowser.Net.Handlers.md:312-354 |
| `CanAccessFileResponse` | A response for the `CanAccessFileHandler`. | DotNetBrowser.Net.Handlers.md:356-411 |
| `CanGetCookiesParameters` | The parameters of the `CanGetCookiesHandler`. | DotNetBrowser.Net.Handlers.md:413-464 |
| `CanGetCookiesResponse` | A response for the `CanGetCookiesHandler`. | DotNetBrowser.Net.Handlers.md:466-523 |
| `CanSetCookieParameters` | The parameters of the `CanSetCookieHandler`. | DotNetBrowser.Net.Handlers.md:525-576 |
| `CanSetCookieResponse` | A response for the `CanSetCookieHandler`. | DotNetBrowser.Net.Handlers.md:578-634 |
| `InterceptRequestParameters` | The parameters of the scheme handler. | DotNetBrowser.Net.Handlers.md:636-689 |
| `InterceptRequestResponse` | A response for the scheme handler. | DotNetBrowser.Net.Handlers.md:691-755 |
| `NetworkParameters` | The base class for `INetwork`-related handlers parameters. | DotNetBrowser.Net.Handlers.md:757-804 |
| `ReceiveHeadersParameters` | The parameters of the `ReceiveHeadersHandler`. | DotNetBrowser.Net.Handlers.md:806-911 |
| `ReceiveHeadersResponse` | The response for the `ReceiveHeadersHandler`. | DotNetBrowser.Net.Handlers.md:913-988 |
| `SendUploadDataParameters` | The parameters of the `SendUploadDataHandler`. | DotNetBrowser.Net.Handlers.md:990-1035 |
| `SendUploadDataResponse` | The response for the `SendUploadDataHandler`. | DotNetBrowser.Net.Handlers.md:1037-1179 |
| `SendUrlRequestParameters` | The parameters of the `SendUrlRequestHandler`. | DotNetBrowser.Net.Handlers.md:1181-1222 |
| `SendUrlRequestResponse` | A response of the `SendUrlRequestHandler`. | DotNetBrowser.Net.Handlers.md:1224-1317 |
| `StartTransactionParameters` | The parameters of the `StartTransactionHandler`. | DotNetBrowser.Net.Handlers.md:1319-1360 |
| `StartTransactionResponse` | A response for the `StartTransactionHandler`. | DotNetBrowser.Net.Handlers.md:1362-1439 |
| `UrlRequestJobOptions` | The options needed to create the `UrlRequestJob`. | DotNetBrowser.Net.Handlers.md:1441-1490 |
| `UrlRequestParameters` | The base class for all the `INetwork`-related handlers parameters containing `UrlRequest`. | DotNetBrowser.Net.Handlers.md:1492-1541 |
| `VerifyCertificateParameters` | The parameters of the `VerifyCertificateHandler`. | DotNetBrowser.Net.Handlers.md:1543-1610 |
| `VerifyCertificateResponse` | A response for the `VerifyCertificateHandler` | DotNetBrowser.Net.Handlers.md:1612-1738 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `ResourceType` | The type of the resource being loaded. | DotNetBrowser.Net.Handlers.md:1740-1875 |

## DotNetBrowser.Net.Proxy

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `AutoDetectProxySettings` | With this proxy configuration the connection automatically detects proxy settings. | DotNetBrowser.Net.Proxy.md:48-74 |
| `CustomProxySettings` | Describes a user's proxy settings. | DotNetBrowser.Net.Proxy.md:76-210 |
| `DirectProxySettings` | With this proxy configuration the connection doesn't use a proxy server. | DotNetBrowser.Net.Proxy.md:212-237 |
| `PacProxySettings` | With this proxy configuration the connection uses proxy settings received from proxy auto-config (PAC) file which is located at the specific address. | DotNetBrowser.Net.Proxy.md:239-310 |
| `ProxySettings` | The base class for all proxy settings. | DotNetBrowser.Net.Proxy.md:312-358 |
| `SystemProxySettings` | The system proxy settings defined by the operating system. | DotNetBrowser.Net.Proxy.md:360-385 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IProxy` | The service that allows modifying the proxy configuration for the current engine. | DotNetBrowser.Net.Proxy.md:387-438 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `ProxyType` | Types of proxy settings. | DotNetBrowser.Net.Proxy.md:440-479 |

## DotNetBrowser.Passwords

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `PasswordRecord` | A record saved in the `IPasswordStore`. | DotNetBrowser.Passwords.md:32-143 |
| `PasswordRecord.Builder` | A builder for creating a new `PasswordRecord` instance. | DotNetBrowser.Passwords.md:145-222 |
| `PasswordStoreExtensions` | Provides extension methods for `IPasswordStore`. | DotNetBrowser.Passwords.md:224-278 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IPasswordStore` | A service that allows working with `PasswordRecord` logins and passwords saved in the Chromium password store. | DotNetBrowser.Passwords.md:280-437 |
| `IPasswords` | A service that allows managing passwords. | DotNetBrowser.Passwords.md:439-571 |

## DotNetBrowser.Passwords.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `SavePasswordParameters` | The parameters of the `SavePasswordHandler`. | DotNetBrowser.Passwords.Handlers.md:21-72 |
| `SavePasswordResponse` | A response to the `SavePasswordHandler`. | DotNetBrowser.Passwords.Handlers.md:74-140 |
| `UpdatePasswordParameters` | The parameters of the `UpdatePasswordHandler`. | DotNetBrowser.Passwords.Handlers.md:142-193 |
| `UpdatePasswordResponse` | A response to the `UpdatePasswordHandler`. | DotNetBrowser.Passwords.Handlers.md:195-246 |

## DotNetBrowser.Permissions

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IPermissions` | A service that allows managing permissions. | DotNetBrowser.Permissions.md:19-90 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `PermissionType` | Represents the permission types. | DotNetBrowser.Permissions.md:92-328 |

## DotNetBrowser.Permissions.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `RequestPermissionParameters` | The parameters of the `RequestPermissionHandler`. | DotNetBrowser.Permissions.Handlers.md:13-62 |
| `RequestPermissionResponse` | A response to the `RequestPermissionHandler`. | DotNetBrowser.Permissions.Handlers.md:64-119 |

## DotNetBrowser.Plugins

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Plugin` | The detailed information about the installed Chromium plugin. | DotNetBrowser.Plugins.md:29-127 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IPluginSettings` | The settings to configure the available Chromium `Plugins`. | DotNetBrowser.Plugins.md:129-183 |
| `IPlugins` | The engine service that provides the details about the available Chromium plugins. | DotNetBrowser.Plugins.md:185-286 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `PluginType` | The plugin types. | DotNetBrowser.Plugins.md:288-309 |

## DotNetBrowser.Plugins.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `AllowPluginParameters` | The parameters for the `AllowPluginHandler`. | DotNetBrowser.Plugins.Handlers.md:13-50 |
| `AllowPluginResponse` | A response to the `AllowPluginHandler`. | DotNetBrowser.Plugins.Handlers.md:52-107 |

## DotNetBrowser.Print

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Capabilities` | The capabilities of a printer. | DotNetBrowser.Print.md:113-198 |
| `PageMargins` | The page margins used for printing. | DotNetBrowser.Print.md:200-359 |
| `PageRange` | The page range to be printed. | DotNetBrowser.Print.md:361-466 |
| `PaperSize` | The paper size used for printing. | DotNetBrowser.Print.md:468-2619 |
| `PdfPrinter` | A printer that allows you to print to PDF. | DotNetBrowser.Print.md:2621-2645 |
| `PdfPrinter<TPrintSettings>` | A printer that allows you to print to PDF. | DotNetBrowser.Print.md:2647-2685 |
| `Printer<TPrintSettings>` | The base class for the printers. | DotNetBrowser.Print.md:2687-2771 |
| `Scaling` | The scaling used for printing. | DotNetBrowser.Print.md:2773-2884 |
| `SystemPrinter` | A local or network printer available in the system. | DotNetBrowser.Print.md:2886-2910 |
| `SystemPrinter<TPrintSettings>` | A local or network printer available in the system. | DotNetBrowser.Print.md:2912-2948 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IPrintJob<TPrintSettings>` | A printing operation that is currently in-progress. | DotNetBrowser.Print.md:2950-3024 |
| `IPrinters<TPrintSettings, TPdfPrintSettings>` | The collection of the available printers. | DotNetBrowser.Print.md:3026-3078 |
| `PdfPrinter.IHtmlSettings` | The print settings available when printing HTML content on the PDF printer. | DotNetBrowser.Print.md:3080-3125 |
| `PdfPrinter.IPdfSettings` | The print settings available when printing PDF content on the PDF printer. | DotNetBrowser.Print.md:3127-3153 |
| `PdfPrinter.ISettings<T>` | The print settings available when printing HTML or PDF content on the PDF printer. | DotNetBrowser.Print.md:3155-3186 |
| `SystemPrinter.IHtmlSettings` | Print settings available when printing HTML content on a physical printer. | DotNetBrowser.Print.md:3188-3240 |
| `SystemPrinter.IPdfSettings` | Print settings available when printing PDF content on a physical printer. | DotNetBrowser.Print.md:3242-3279 |
| `SystemPrinter.ISettings<T>` | Print settings available when printing HTML or PDF content on a physical printer. | DotNetBrowser.Print.md:3281-3321 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `ColorModel` | The color models used for printing. | DotNetBrowser.Print.md:3323-3590 |
| `DuplexMode` | The duplex modes used for printing. | DotNetBrowser.Print.md:3592-3625 |
| `Fit` | The content fit used for printing. | DotNetBrowser.Print.md:3627-3648 |
| `Orientation` | The page orientation values used for printing. | DotNetBrowser.Print.md:3650-3671 |
| `PagesPerSheet` | The pages per sheet values that Chromium supports. | DotNetBrowser.Print.md:3673-3718 |
| `PaperSize.Unit` | The measurement unit of the paper size. | DotNetBrowser.Print.md:3720-3747 |

## DotNetBrowser.Print.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `PageCountUpdatedEventArgs<TPrintSettings>` | Event arguments for the `PageCountUpdated` event. | DotNetBrowser.Print.Events.md:13-70 |
| `PrintCompletedEventArgs<TPrintSettings>` | Event arguments for the `PrintCompleted` event. | DotNetBrowser.Print.Events.md:72-129 |

## DotNetBrowser.Print.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `PrintContentParameters<TPrintSettings, TPdfPrintSettings>` | The base class for content printing handlers parameters. | DotNetBrowser.Print.Handlers.md:25-85 |
| `PrintHtmlContentParameters` | The parameters of the `PrintHtmlContentHandler`. | DotNetBrowser.Print.Handlers.md:87-113 |
| `PrintHtmlContentResponse` | A response for the `PrintHtmlContentHandler`. | DotNetBrowser.Print.Handlers.md:115-201 |
| `PrintPdfContentParameters` | The parameters of the `PrintPdfContentHandler`. | DotNetBrowser.Print.Handlers.md:203-229 |
| `PrintPdfContentResponse` | A response for the `PrintPdfContentHandler`. | DotNetBrowser.Print.Handlers.md:231-317 |

## DotNetBrowser.Print.Settings

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `CollateExtensions` | Extension methods for `ICollate` interface. | DotNetBrowser.Print.Settings.md:151-241 |
| `ColorModelExtensions` | Extension methods for `IColorModel` interface. | DotNetBrowser.Print.Settings.md:243-305 |
| `CopiesExtensions` | Extension methods for `ICopies` interface. | DotNetBrowser.Print.Settings.md:307-373 |
| `DuplexModeExtensions` | Extension methods for `IDuplexMode` interface. | DotNetBrowser.Print.Settings.md:375-437 |
| `FitExtensions` | Extension methods for `IFit` interface. | DotNetBrowser.Print.Settings.md:439-505 |
| `FooterTemplateExtensions` | Extension methods for `IFooterTemplate` interface. | DotNetBrowser.Print.Settings.md:507-569 |
| `HeaderTemplateExtensions` | Extension methods for `IHeaderTemplate` interface. | DotNetBrowser.Print.Settings.md:571-633 |
| `OrientationExtensions` | Extension methods for `IOrientation` interface. | DotNetBrowser.Print.Settings.md:635-697 |
| `PageMarginsExtensions` | Extension methods for `IPageMargins` interface. | DotNetBrowser.Print.Settings.md:699-765 |
| `PageRangesExtensions` | Extension methods for `IPageRanges` interface. | DotNetBrowser.Print.Settings.md:767-829 |
| `PagesPerSheetExtensions` | Extension methods for `IPagesPerSheet` interface. | DotNetBrowser.Print.Settings.md:831-893 |
| `PaperSizeExtensions` | Extension methods for `IPaperSize` interface. | DotNetBrowser.Print.Settings.md:895-957 |
| `PdfFilePathExtensions` | Extension methods for `IPdfFilePath` interface. | DotNetBrowser.Print.Settings.md:959-1025 |
| `PrintBackgroundsExtensions` | Extension methods for `IPrintBackgrounds` interface. | DotNetBrowser.Print.Settings.md:1027-1117 |
| `PrintHeaderFooterExtensions` | Extension methods for `IPrintHeaderFooter` interface. | DotNetBrowser.Print.Settings.md:1119-1209 |
| `PrintSelectionOnlyExtensions` | Extension methods for `IPrintSelectionOnly` interface. | DotNetBrowser.Print.Settings.md:1211-1301 |
| `PrintSettingsExtensions` | Extension methods for `IPrintSettings` interface. | DotNetBrowser.Print.Settings.md:1303-1363 |
| `ScalingExtensions` | Extension methods for `IScaling` interface. | DotNetBrowser.Print.Settings.md:1365-1431 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `ICollate<TPrintSettings>` | Allows configuring collate printing. | DotNetBrowser.Print.Settings.md:1433-1478 |
| `IColorModel<TPrintSettings>` | Allows configuring the color model for printing. | DotNetBrowser.Print.Settings.md:1480-1523 |
| `ICopies<TPrintSettings>` | Allows configuring the number of copies to print. | DotNetBrowser.Print.Settings.md:1525-1573 |
| `IDuplexMode<TPrintSettings>` | Allows configuring the duplex mode for printing. | DotNetBrowser.Print.Settings.md:1575-1619 |
| `IFit<TPrintSettings>` | Allows configuring the content fit for printing. | DotNetBrowser.Print.Settings.md:1621-1669 |
| `IFooterTemplate<TPrintSettings>` | Allows configuring the HTML template for the print footer. | DotNetBrowser.Print.Settings.md:1671-1743 |
| `IHeaderTemplate<TPrintSettings>` | Allows configuring the HTML template for the print header. | DotNetBrowser.Print.Settings.md:1745-1817 |
| `IOrientation<TPrintSettings>` | Allows configuring the page orientation. | DotNetBrowser.Print.Settings.md:1819-1863 |
| `IPageMargins<TPrintSettings>` | Allows configuring the page margins. | DotNetBrowser.Print.Settings.md:1865-1913 |
| `IPageRanges<TPrintSettings>` | Allows configuring the page ranges for printing. | DotNetBrowser.Print.Settings.md:1915-1959 |
| `IPagesPerSheet<TPrintSettings>` | Allows configuring the number of pages per sheet. | DotNetBrowser.Print.Settings.md:1961-2005 |
| `IPaperSize<TPrintSettings>` | Allows configuring the paper size for printing. | DotNetBrowser.Print.Settings.md:2007-2051 |
| `IPdfFilePath<TPrintSettings>` | Allows configuring the destination PDF file path. | DotNetBrowser.Print.Settings.md:2053-2101 |
| `IPrintBackgrounds<TPrintSettings>` | Allows configuring printing background graphics. | DotNetBrowser.Print.Settings.md:2103-2148 |
| `IPrintHeaderFooter<TPrintSettings>` | Allows configuring printing headers and footers. | DotNetBrowser.Print.Settings.md:2150-2195 |
| `IPrintSelectionOnly<TPrintSettings>` | Allows configuring printing only the selected content. | DotNetBrowser.Print.Settings.md:2197-2242 |
| `IPrintSettings` | The common interface for the concrete print job settings to implement. | DotNetBrowser.Print.Settings.md:2244-2284 |
| `IScaling<TPrintSettings>` | Allows configuring the scaling for printing. | DotNetBrowser.Print.Settings.md:2286-2334 |

## DotNetBrowser.Profile

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IProfile` | The Chromium profile. | DotNetBrowser.Profile.md:27-370 |
| `IProfilePreferences` | The preferences of a `IProfile`. | DotNetBrowser.Profile.md:372-504 |
| `IProfiles` | The collection of the Chromium profiles. | DotNetBrowser.Profile.md:506-617 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `CookieControlsMode` | The Chromium third-party cookies block mode. | DotNetBrowser.Profile.md:619-654 |
| `ProfileType` | The Chromium profile type. | DotNetBrowser.Profile.md:656-677 |

## DotNetBrowser.Search

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `FindOptions` | The find text options. | DotNetBrowser.Search.md:33-104 |
| `FindResult` | A result of the text search. | DotNetBrowser.Search.md:106-156 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `ITextFinder` | Allows finding text on the loaded web page. | DotNetBrowser.Search.md:158-251 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `Direction` | The search direction. | DotNetBrowser.Search.md:253-274 |
| `StopFindAction` | The stop find actions. | DotNetBrowser.Search.md:276-297 |

## DotNetBrowser.Search.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `FindResultReceivedParameters` | The parameters of the handler that is passed to the `Find` method and called when a find result is received. | DotNetBrowser.Search.Handlers.md:10-88 |

## DotNetBrowser.SpellCheck

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Language` | The language for which Chromium can perform spell checking. | DotNetBrowser.SpellCheck.md:37-650 |
| `LanguageNotAvailableException` | Thrown when the engine fails to configure the spellchecker to use the language passed to the `Add` method. | DotNetBrowser.SpellCheck.md:652-707 |
| `SpellCheckMenu` | A spell check menu in the context menu. | DotNetBrowser.SpellCheck.md:709-770 |
| `SpellCheckingResult` | The spell checking result that contains the bounds of a mis-spelled substring of the checked text. | DotNetBrowser.SpellCheck.md:772-823 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `ILanguages` | The collection of the languages used for spell checking. | DotNetBrowser.SpellCheck.md:825-941 |
| `ISpellCheckDictionary` | Provides functionality for working with a spell check dictionary. | DotNetBrowser.SpellCheck.md:943-1071 |
| `ISpellChecker` | Represents an engine service that provides functionality for configuring spell checking. | DotNetBrowser.SpellCheck.md:1073-1158 |

## DotNetBrowser.Ui

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Bitmap` | Represents a binary image that consists of an image size and a byte array that contains the pre-multiplied image pixels in the BGRA format. | DotNetBrowser.Ui.md:31-88 |
| `Color` | A numeric model of an RGB color. The components of the color instance are presented in the arithmetic notation. This means that each component accepts any fractional value from 0 to 1. | DotNetBrowser.Ui.md:90-332 |
| `Font` | A system font. | DotNetBrowser.Ui.md:334-409 |
| `FontSize` | The browser font size. | DotNetBrowser.Ui.md:411-540 |
| `Language` | The supported user interface languages. | DotNetBrowser.Ui.md:542-1288 |

## DotNetBrowser.Ui.Cursors

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `CursorType` | The cursor types. | DotNetBrowser.Ui.Cursors.md:9-342 |

## DotNetBrowser.UserData

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Address` | The user's address containing information about a street, city, state, etc. | DotNetBrowser.UserData.md:36-160 |
| `Address.Builder` | A builder for the `Address` class. | DotNetBrowser.UserData.md:162-276 |
| `UserDataProfile` | The collected data entered by the user to a form and persisted to `the user data store`. | DotNetBrowser.UserData.md:278-390 |
| `UserDataProfile.Builder` | A builder for creating a new `UserDataProfile` instance. | DotNetBrowser.UserData.md:392-493 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IUserDataProfileStore` | The data store for `the user data`. | DotNetBrowser.UserData.md:495-612 |
| `IUserDataProfiles` | A service that allows managing user data profiles. | DotNetBrowser.UserData.md:614-726 |

## DotNetBrowser.UserData.Handlers

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `SaveUserDataProfileParameters` | The parameters of the `SaveUserDataProfileHandler`. | DotNetBrowser.UserData.Handlers.md:21-60 |
| `SaveUserDataProfileResponse` | A response to the `SaveUserDataProfileHandler`. | DotNetBrowser.UserData.Handlers.md:62-113 |
| `UpdateUserDataProfileParameters` | The parameters of the `UpdateUserDataProfileHandler`. | DotNetBrowser.UserData.Handlers.md:115-166 |
| `UpdateUserDataProfileResponse` | A response to the `UpdateUserDataProfileHandler`. | DotNetBrowser.UserData.Handlers.md:168-219 |

## DotNetBrowser.WinForms

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `BitmapExtensions` | Extensions for `Bitmap` class. | DotNetBrowser.WinForms.md:19-65 |
| `BrowserView` | The WinForms-based implementation of browser view. | DotNetBrowser.WinForms.md:67-749 |

## DotNetBrowser.WinForms.Dialogs

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `ColorExtensions` | Extension methods for performing color conversion. | DotNetBrowser.WinForms.Dialogs.md:23-89 |
| `DefaultAuthenticationHandler` | Default WinForms authentication handler, which displays an authentication dialog. | DotNetBrowser.WinForms.Dialogs.md:91-161 |
| `DefaultStartDownloadHandler` | The default WinForms implementation of `StartDownloadHandler`, which displays a save file dialog to specify the path to store the downloaded file. | DotNetBrowser.WinForms.Dialogs.md:163-249 |
| `DialogHandlerBase` | The base class for all dialog handlers. | DotNetBrowser.WinForms.Dialogs.md:251-311 |

## DotNetBrowser.WinForms.Extensions

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DefaultOpenExtensionPopupHandler` | Default extension popup handler, which displays an extension popup as a separate window. | DotNetBrowser.WinForms.Extensions.md:9-68 |

## DotNetBrowser.WinUi3

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `BitmapExtensions` | Extensions for `Bitmap` class. | DotNetBrowser.WinUi3.md:21-88 |
| `BrowserView` | The WinUI3-based implementation of browser view. | DotNetBrowser.WinUi3.md:90-757 |

## DotNetBrowser.WinUi3.ContextMenu

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `MenuItemViewModel` | Represent the view model of a single menu item. | DotNetBrowser.WinUi3.ContextMenu.md:9-117 |

## DotNetBrowser.WinUi3.Dialogs

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DefaultAuthenticationHandler` | Default WinUI 3 authentication handler, which displays an authentication dialog. | DotNetBrowser.WinUi3.Dialogs.md:13-81 |
| `DialogHandlerBase` | The base class for all dialog handlers. | DotNetBrowser.WinUi3.Dialogs.md:83-142 |

## DotNetBrowser.WinUi3.Extensions

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DefaultOpenExtensionPopupHandler` | Default extension popup handler, which displays an extension popup as a separate window. | DotNetBrowser.WinUi3.Extensions.md:9-68 |

## DotNetBrowser.Wpf

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `BitmapExtensions` | Extensions for `Bitmap` class. | DotNetBrowser.Wpf.md:21-88 |
| `BrowserView` | The Wpf-based implementation of browser view. | DotNetBrowser.Wpf.md:90-998 |

## DotNetBrowser.Wpf.ContextMenu

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `MenuItemViewModel` |  | DotNetBrowser.Wpf.ContextMenu.md:7-91 |

## DotNetBrowser.Wpf.Dialogs

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `ColorExtensions` | Extension methods for performing color conversion. | DotNetBrowser.Wpf.Dialogs.md:22-88 |
| `DefaultAuthenticationHandler` | Default Wpf authentication handler, which displays an authentication dialog. | DotNetBrowser.Wpf.Dialogs.md:90-160 |
| `DefaultStartDownloadHandler` | The default Wpf implementation of `StartDownloadHandler`, which displays a save file dialog to specify the path to store the downloaded file. | DotNetBrowser.Wpf.Dialogs.md:162-247 |
| `DialogHandlerBase` | The base class for all dialog handlers. | DotNetBrowser.Wpf.Dialogs.md:249-309 |

## DotNetBrowser.Wpf.Extensions

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `DefaultOpenExtensionPopupHandler` | Default extension popup handler, which displays an extension popup as a separate window. | DotNetBrowser.Wpf.Extensions.md:9-68 |

## DotNetBrowser.Zoom

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `Level` | A zoom level of a web page. Provides a set of the pre-defined constants. Each constant name consists of the P prefix followed by a number. The number represents a zoom level in percents. For exampl... | DotNetBrowser.Zoom.md:32-309 |

### Interfaces

| Type | Summary | File and lines |
|---|---|---|
| `IZoom` | Allows zooming content of a web page. | DotNetBrowser.Zoom.md:311-469 |
| `IZoomLevels` | Allows configuring the default zoom levels and receive notifications about zoom changes. | DotNetBrowser.Zoom.md:471-546 |

### Enums

| Type | Summary | File and lines |
|---|---|---|
| `ZoomMode` | Defines how zoom settings are stored and applied. | DotNetBrowser.Zoom.md:548-569 |

## DotNetBrowser.Zoom.Events

### Classes

| Type | Summary | File and lines |
|---|---|---|
| `LevelChangedEventArgs` | The event arguments for the `LevelChanged` event. | DotNetBrowser.Zoom.Events.md:9-73 |
