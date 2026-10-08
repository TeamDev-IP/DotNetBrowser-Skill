# <a id="DotNetBrowser_Browser_IBrowser"></a> Interface IBrowser

Namespace: [DotNetBrowser.Browser](DotNetBrowser.Browser.md)  
Assembly: DotNetBrowser.dll  

A web browser control that allows loading a web page or a local HTML file, accessing DOM and
executing JavaScript on the loaded web page, getting notifications about loading progress,
dispatching keyboard and mouse events, etc.

```csharp
public interface IBrowser : IDisposable, IAutoDisposable
```

#### Implements

[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Remarks

<p>
    The <code>IBrowser</code> instance itself is running in a separate native process that allocates
    memory and system resources that must be released. So, when a <code>IBrowser</code> instance is no
    longer needed, it must be disposed through the <xref href="System.IDisposable.Dispose" data-throw-if-not-resolved="false"></xref> method to release all the
    allocated memory and system resources. For example:
</p>

<pre><code class="lang-csharp">IBrowser browser = engine.CreateBrowser();
...
browser.Dispose();</code></pre>

<p>
    Any attempt to use an already disposed <code>IBrowser</code> instance will lead to the
    <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    The <code>IBrowser</code> instance is disposed automatically when its <code> IEngine</code> is disposed or
    unexpectedly crashed. If the instance represents a popup window created by JavaScript via the
    <code>window.open()</code> function, then JavaScript can close the instance using the
    <code>window.close()</code> function.
</p>
<p>
    To get notifications that the <code>IBrowser</code> instance has been disposed please subscribe to
    the following event:
</p>

<pre><code class="lang-csharp">browser.Disposed += (s, e) =&gt; {
    // The Browser instance has been disposed.
};</code></pre>

## Properties

### <a id="DotNetBrowser_Browser_IBrowser_AllFrames"></a> AllFrames

Gets all the frames on the currently loaded web page.

```csharp
IEnumerable<IFrame> AllFrames { get; }
```

#### Property Value

 [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IFrame](DotNetBrowser.Frames.IFrame.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_Audio"></a> Audio

Gets the <xref href="DotNetBrowser.Media.IAudio" data-throw-if-not-resolved="false"></xref> instance that allows controlling audio on the loaded web page and receive
notifications when audio has been
started or stopped playing.

```csharp
IAudio Audio { get; }
```

#### Property Value

 [IAudio](DotNetBrowser.Media.IAudio.md)

### <a id="DotNetBrowser_Browser_IBrowser_Capture"></a> Capture

Gets the <xref href="DotNetBrowser.Capture.ICapture" data-throw-if-not-resolved="false"></xref> instance that can be used for listening and handling capture sessions.

```csharp
ICapture Capture { get; }
```

#### Property Value

 [ICapture](DotNetBrowser.Capture.ICapture.md)

### <a id="DotNetBrowser_Browser_IBrowser_Cast"></a> Cast

Gets the <xref href="DotNetBrowser.Cast.ICast" data-throw-if-not-resolved="false"></xref> instance that can be used for casting media on receivers.

```csharp
ICast Cast { get; }
```

#### Property Value

 [ICast](DotNetBrowser.Cast.ICast.md)

### <a id="DotNetBrowser_Browser_IBrowser_ConvertJsNameHandler"></a> ConvertJsNameHandler

Gets or sets a handler that is used for the JavaScript name converting.
Implement this handler to have control of how the names are converted
when binding or executing JavaScript.

```csharp
IHandler<ConvertJsNameParameters, ConvertJsNameResponse> ConvertJsNameHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[ConvertJsNameParameters](DotNetBrowser.Frames.Handlers.ConvertJsNameParameters.md), [ConvertJsNameResponse](DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.md)\>

#### Remarks

<p>
    The handler should be configured before registering .NET objects on the JavaScript side.
</p>
<p>
    The <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameParameters" data-throw-if-not-resolved="false"></xref> object contains information about the
    <xref href="System.Reflection.MemberInfo" data-throw-if-not-resolved="false"></xref> of the .NET object.
</p>
<p>
    Use the <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.NoConversion" data-throw-if-not-resolved="false"></xref> method to use the member name as is.
</p>
<p>
    Use the <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.CamelCase" data-throw-if-not-resolved="false"></xref> method to convert the first letter
    of the name to the lower case.
</p>
<p>
    Use the <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.PascalCase" data-throw-if-not-resolved="false"></xref> method to convert the first letter
    of the name to the upper case.
</p>
<p>
    Use the <xref href="DotNetBrowser.Frames.Handlers.ConvertJsNameResponse.ConvertTo(System.String)" data-throw-if-not-resolved="false"></xref> method for customizing the name.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_CreatePopupHandler"></a> CreatePopupHandler

Gets or sets a handler that is used when the browser decides whether a new popup instance can be created or not.

```csharp
IHandler<CreatePopupParameters, CreatePopupResponse> CreatePopupHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[CreatePopupParameters](DotNetBrowser.Browser.Handlers.CreatePopupParameters.md), [CreatePopupResponse](DotNetBrowser.Browser.Handlers.CreatePopupResponse.md)\>

#### Remarks

<p>Use the <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse.Create" data-throw-if-not-resolved="false"></xref> method to let the browser to create a new popup.</p>
<p>Use the <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse.Suppress" data-throw-if-not-resolved="false"></xref> method to suppress popup.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.CreatePopupResponse.Suppress" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_CreditCards"></a> CreditCards

Gets the <xref href="DotNetBrowser.Card.ICreditCards" data-throw-if-not-resolved="false"></xref> instance that can be used for working with credit cards
saved in the Chromium credit card store.

```csharp
ICreditCards CreditCards { get; }
```

#### Property Value

 [ICreditCards](DotNetBrowser.Card.ICreditCards.md)

### <a id="DotNetBrowser_Browser_IBrowser_DevTools"></a> DevTools

Gets the <xref href="DotNetBrowser.DevTools.IDevTools" data-throw-if-not-resolved="false"></xref> instance that allows working with Chromium Developer Tools for this browser.

```csharp
IDevTools DevTools { get; }
```

#### Property Value

 [IDevTools](DotNetBrowser.DevTools.IDevTools.md)

### <a id="DotNetBrowser_Browser_IBrowser_Dialogs"></a> Dialogs

Gets the <xref href="DotNetBrowser.Browser.Dialogs.IDialogs" data-throw-if-not-resolved="false"></xref> instance that can be used for configuring the dialogs that can be shown by
browser.

```csharp
IDialogs Dialogs { get; }
```

#### Property Value

 [IDialogs](DotNetBrowser.Browser.Dialogs.IDialogs.md)

### <a id="DotNetBrowser_Browser_IBrowser_DragAndDrop"></a> DragAndDrop

Gets the <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> instance that can be used for managing drag&amp;drop operations for the
browser.

```csharp
IDragAndDrop DragAndDrop { get; }
```

#### Property Value

 [IDragAndDrop](DotNetBrowser.Input.DragAndDrop.IDragAndDrop.md)

### <a id="DotNetBrowser_Browser_IBrowser_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Browser_IBrowser_Favicon"></a> Favicon

Gets the favicon of the currently loaded web page.

```csharp
Bitmap Favicon { get; }
```

#### Property Value

 [Bitmap](DotNetBrowser.Ui.Bitmap.md)

#### Remarks

Maximum favicon size is 16x16. If the actual favicon size is bigger, then it will be resized
to fit this constraint.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_FocusedFrame"></a> FocusedFrame

Gets the focused frame on the currently loaded web page.

```csharp
IFrame FocusedFrame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_FullScreen"></a> FullScreen

Gets the <xref href="DotNetBrowser.Browser.FullScreen.IFullScreen" data-throw-if-not-resolved="false"></xref> instance that can be used for controlling the browser's fullscreen mode.

```csharp
IFullScreen FullScreen { get; }
```

#### Property Value

 [IFullScreen](DotNetBrowser.Browser.FullScreen.IFullScreen.md)

### <a id="DotNetBrowser_Browser_IBrowser_InjectCssHandler"></a> InjectCssHandler

Gets or sets a handler that is used when the document element has been created and a custom stylesheet can
be injected into the document.

```csharp
IHandler<InjectCssParameters, InjectCssResponse> InjectCssHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[InjectCssParameters](DotNetBrowser.Browser.Handlers.InjectCssParameters.md), [InjectCssResponse](DotNetBrowser.Browser.Handlers.InjectCssResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse.Inject(System.String)" data-throw-if-not-resolved="false"></xref> method to inject a custom stylesheet into the
    document.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse.Proceed" data-throw-if-not-resolved="false"></xref> method to continue loading without injecting.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.InjectCssResponse.Proceed" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_InjectJsHandler"></a> InjectJsHandler

Gets or sets a handler that is used when the document element has been created and a custom JavaScript can
be injected into the document.

```csharp
IHandler<InjectJsParameters> InjectJsHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-1.md)<[InjectJsParameters](DotNetBrowser.Browser.Handlers.InjectJsParameters.md)\>

#### Remarks

<p>
    You can inject a custom JavaScript code using the <xref href="DotNetBrowser.Frames.IFrame.ExecuteJavaScript(System.String%2cSystem.Boolean)" data-throw-if-not-resolved="false"></xref>
    method.This callback is intended to give you an opportunity to inject a .NET object into
    JavaScript code or inject a custom JavaScript code for further execution before any scripts are
    executed in the particular frame. For example:

<pre><code class="lang-csharp">Browser.InjectJsHandler = new Handler&lt;InjectJsParameters&gt;(args =&gt;
{
    IJsObject window = args.Frame.ExecuteJavaScript&lt;IJsObject&gt;("window").Result;
    window["myObject"] = new MyObject();
});</code></pre>

</p>
<p>
    The MyObject class may look like this:

<pre><code class="lang-csharp">public class MyObject
{
    public string SayHelloTo(string firstName) =&gt; "Hello " + firstName + "!";
}</code></pre>

</p>
<p>
    When the property is set, you can call methods of the injected .NET object from JavaScript:

<pre><code class="lang-csharp">window.myObject.SayHelloTo('John');</code></pre>

</p>
<p>This handler may be invoked several times for the same frame.</p>
<p>
    <b>Important:</b> you should avoid executing a JavaScript code that modifies the DOM tree of
    the web page being loaded.You must not use DotNetBrowser DOM API to remove the frame for which this
    callback is invoked, otherwise the render process will crash.
</p>
<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_JsDialogs"></a> JsDialogs

Gets the <xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs" data-throw-if-not-resolved="false"></xref> instance that can be used for configuring the JavaScript dialogs that can be
shown by browser.

```csharp
IJsDialogs JsDialogs { get; }
```

#### Property Value

 [IJsDialogs](DotNetBrowser.Browser.Dialogs.IJsDialogs.md)

### <a id="DotNetBrowser_Browser_IBrowser_Keyboard"></a> Keyboard

Gets the <xref href="DotNetBrowser.Input.Keyboard.IKeyboard" data-throw-if-not-resolved="false"></xref> instance that can be used for listening and simulating keyboard input events.

```csharp
IKeyboard Keyboard { get; }
```

#### Property Value

 [IKeyboard](DotNetBrowser.Input.Keyboard.IKeyboard.md)

### <a id="DotNetBrowser_Browser_IBrowser_MainFrame"></a> MainFrame

The main frame on the currently loaded web page, if it exists.

```csharp
IFrame MainFrame { get; }
```

#### Property Value

 [IFrame](DotNetBrowser.Frames.IFrame.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_Mouse"></a> Mouse

Gets the <xref href="DotNetBrowser.Input.Mouse.IMouse" data-throw-if-not-resolved="false"></xref> instance that can be used for listening and simulating mouse input events.

```csharp
IMouse Mouse { get; }
```

#### Property Value

 [IMouse](DotNetBrowser.Input.Mouse.IMouse.md)

### <a id="DotNetBrowser_Browser_IBrowser_Navigation"></a> Navigation

Gets the <xref href="DotNetBrowser.Navigation.INavigation" data-throw-if-not-resolved="false"></xref> instance that can be used for controlling navigation in the current browser
instance.

```csharp
INavigation Navigation { get; }
```

#### Property Value

 [INavigation](DotNetBrowser.Navigation.INavigation.md)

### <a id="DotNetBrowser_Browser_IBrowser_OpenExtensionActionPopupHandler"></a> OpenExtensionActionPopupHandler

Gets or sets a handler that is used for handling the popups that are requested to be shown by the extension action.

```csharp
IHandler<OpenExtensionActionPopupParameters> OpenExtensionActionPopupHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-1.md)<[OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters.md)\>

#### Remarks

<p>
    The <xref href="DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters" data-throw-if-not-resolved="false"></xref> object contains the popup browser.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_OpenPopupHandler"></a> OpenPopupHandler

Gets or sets a handler that is used when a new popup browser instance should be opened.

```csharp
IHandler<OpenPopupParameters> OpenPopupHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-1.md)<[OpenPopupParameters](DotNetBrowser.Browser.Handlers.OpenPopupParameters.md)\>

#### Remarks

<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_Passwords"></a> Passwords

Gets the <xref href="DotNetBrowser.Passwords.IPasswords" data-throw-if-not-resolved="false"></xref> instance that can be used for working with logins and passwords
saved in the Chromium password store.

```csharp
IPasswords Passwords { get; }
```

#### Property Value

 [IPasswords](DotNetBrowser.Passwords.IPasswords.md)

### <a id="DotNetBrowser_Browser_IBrowser_PrintHtmlContentHandler"></a> PrintHtmlContentHandler

Gets or sets a handler that is used when the HTML content printing is initiated.

```csharp
IHandler<PrintHtmlContentParameters, PrintHtmlContentResponse> PrintHtmlContentHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[PrintHtmlContentParameters](DotNetBrowser.Print.Handlers.PrintHtmlContentParameters.md), [PrintHtmlContentResponse](DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.md)\>

#### Remarks

<p>
    In this callback you can configure the print settings. The workflow is the following:
</p>
<p>
    <ul><li>
            <returns>
                Find the required printer using the <xref href="DotNetBrowser.Print.IPrinters%602" data-throw-if-not-resolved="false"></xref>
                interface.
                You can obtain an instance of <code>Printers</code> using the
                <xref href="DotNetBrowser.Print.Handlers.PrintContentParameters%602.Printers" data-throw-if-not-resolved="false"></xref> property.
            </returns>
        </li><li>
            <returns>Get the current <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> from the printer.</returns>
        </li><li>
            <returns>
                Configure the required settings for the print job using the
                <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> interface provided by the
                <xref href="DotNetBrowser.Print.IPrintJob%601.Settings" data-throw-if-not-resolved="false"></xref> property.
            </returns>
        </li><li>
            <returns>
                Apply the configured settings using the
                <xref href="DotNetBrowser.Print.Settings.IPrintSettings.Apply" data-throw-if-not-resolved="false"></xref> method.
            </returns>
        </li><li>
            <returns>
                Tell the browser to proceed with the printing using the configured settings:
                <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.Print(DotNetBrowser.Print.SystemPrinter%7bDotNetBrowser.Print.SystemPrinter.IHtmlSettings%7d)" data-throw-if-not-resolved="false"></xref>.
            </returns>
        </li></ul>
</p>
<p>
    Use the <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.Print(DotNetBrowser.Print.SystemPrinter%7bDotNetBrowser.Print.SystemPrinter.IHtmlSettings%7d)" data-throw-if-not-resolved="false"></xref> method
    to continue printing using the selected printer.
</p>
<p>Use the <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel printing.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Print.Handlers.PrintHtmlContentResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p>
    If printing is initiated when the browser is loading a web page, this callback is not
    invoked.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_PrintPdfContentHandler"></a> PrintPdfContentHandler

Gets or sets a handler that is used when the PDF content printing is initiated.

```csharp
IHandler<PrintPdfContentParameters, PrintPdfContentResponse> PrintPdfContentHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[PrintPdfContentParameters](DotNetBrowser.Print.Handlers.PrintPdfContentParameters.md), [PrintPdfContentResponse](DotNetBrowser.Print.Handlers.PrintPdfContentResponse.md)\>

#### Remarks

<p>
    In this callback you can configure the print settings. The workflow is the following:
</p>
<p>
    <ul><li>
            <returns>
                Find the required printer using the <xref href="DotNetBrowser.Print.IPrinters%602" data-throw-if-not-resolved="false"></xref>
                interface.
                You can obtain an instance of <code>Printers</code> using the
                <xref href="DotNetBrowser.Print.Handlers.PrintContentParameters%602.Printers" data-throw-if-not-resolved="false"></xref> property.
            </returns>
        </li><li>
            <returns>Get the current <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> from the printer.</returns>
        </li><li>
            <returns>
                Configure the required settings for the print job using the
                <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> interface provided by the
                <xref href="DotNetBrowser.Print.IPrintJob%601.Settings" data-throw-if-not-resolved="false"></xref> property.
            </returns>
        </li><li>
            <returns>
                Apply the configured settings using the
                <xref href="DotNetBrowser.Print.Settings.IPrintSettings.Apply" data-throw-if-not-resolved="false"></xref> method.
            </returns>
        </li><li>
            <returns>
                Tell the browser to proceed with the printing using the configured settings:
                <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse.Print(DotNetBrowser.Print.SystemPrinter%7bDotNetBrowser.Print.SystemPrinter.IPdfSettings%7d)" data-throw-if-not-resolved="false"></xref>.
            </returns>
        </li></ul>
</p>
<p>
    Use the <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse.Print(DotNetBrowser.Print.SystemPrinter%7bDotNetBrowser.Print.SystemPrinter.IPdfSettings%7d)" data-throw-if-not-resolved="false"></xref> method
    to continue printing using the selected printer.
</p>
<p>Use the <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel printing.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Print.Handlers.PrintPdfContentResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p>
    If printing is initiated when the browser is loading a web page, this callback is not
    invoked.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_Profile"></a> Profile

Gets the <xref href="DotNetBrowser.Profile.IProfile" data-throw-if-not-resolved="false"></xref> instance associated with this browser.

```csharp
IProfile Profile { get; }
```

#### Property Value

 [IProfile](DotNetBrowser.Profile.IProfile.md)

### <a id="DotNetBrowser_Browser_IBrowser_RenderingMode"></a> RenderingMode

Gets the rendering mode of this browser.

```csharp
RenderingMode RenderingMode { get; }
```

#### Property Value

 [RenderingMode](DotNetBrowser.Engine.RenderingMode.md)

### <a id="DotNetBrowser_Browser_IBrowser_RequestPdfDocumentPasswordHandler"></a> RequestPdfDocumentPasswordHandler

Gets or sets a handler that is used when the frame requests the password for an encrypted PDF document.

```csharp
IHandler<RequestPdfDocumentPasswordParameters, RequestPdfDocumentPasswordResponse> RequestPdfDocumentPasswordHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[RequestPdfDocumentPasswordParameters](DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordParameters.md), [RequestPdfDocumentPasswordResponse](DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.Password(System.String)" data-throw-if-not-resolved="false"></xref> method to
    provide the password for the encrypted PDF document.
</p>
<p>
    Use the<xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.ShowPasswordDialog" data-throw-if-not-resolved="false"></xref> method to
    invoke the default PDF viewer password dialog.
</p>
<p>
    Use the<xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to
    cancel the request.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.RequestPdfDocumentPasswordResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_RequestPrintHandler"></a> RequestPrintHandler

Gets or sets a handler that is used when the printing is initiated.

```csharp
IHandler<RequestPrintParameters, RequestPrintResponse> RequestPrintHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[RequestPrintParameters](DotNetBrowser.Browser.Handlers.RequestPrintParameters.md), [RequestPrintResponse](DotNetBrowser.Browser.Handlers.RequestPrintResponse.md)\>

#### Remarks

<p>In this callback you can cancel or allow showing print preview dialog, or print the content programmatically.</p>
<p>By default, the printing is canceled if there is no browser view initialized from the browser.</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.ShowPrintPreview" data-throw-if-not-resolved="false"></xref> method to show the print preview.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.Print" data-throw-if-not-resolved="false"></xref> method to continue printing and configure it programmatically
    in <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref> and <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref>.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel printing.</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>
<p>
    <b>Important:</b> do not use <xref href="DotNetBrowser.Browser.Handlers.RequestPrintResponse.ShowPrintPreview" data-throw-if-not-resolved="false"></xref> if the browser is not
    displayed. In this case, the dialog will not be visible  - as a result, the end user will not be able to
    close it or confirm printing.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_SelectCertificateHandler"></a> SelectCertificateHandler

Gets or sets a handler that is used when the web server requires authorization via client certificate.

```csharp
IHandler<SelectCertificateParameters, SelectCertificateResponse> SelectCertificateHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SelectCertificateParameters](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateParameters.md), [SelectCertificateResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.md)\>

#### Remarks

<p>The <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateParameters" data-throw-if-not-resolved="false"></xref> object contains information about the authorization request.</p>
<p>
    To access the list of the certificates from the system storage that match the server criteria you
    can use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateParameters.Certificates" data-throw-if-not-resolved="false"></xref> property.
</p>
<p>
    You can use this handler to display a dialog with the list of the available certificates
    that allows the user to select the required certificate. Please note that it is not necessary to
    display a dialog in this handler.
</p>
<p>This handler itself is never called on the UI thread directly.</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the authorization.</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.Select(System.Int32)" data-throw-if-not-resolved="false"></xref> method to inform the browser to use
    the client certificate located by the passed index in the certificate list.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.Select(DotNetBrowser.Net.Certificates.Certificate)" data-throw-if-not-resolved="false"></xref> method to inform the
    browser to use the specified client certificate.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_Settings"></a> Settings

Gets the <xref href="DotNetBrowser.Browser.IBrowserSettings" data-throw-if-not-resolved="false"></xref> instance that can be used for modifying the settings of the browser.

```csharp
IBrowserSettings Settings { get; }
```

#### Property Value

 [IBrowserSettings](DotNetBrowser.Browser.IBrowserSettings.md)

### <a id="DotNetBrowser_Browser_IBrowser_ShowContextMenuHandler"></a> ShowContextMenuHandler

Gets or sets a handler that is used when the browser should show a context menu.

```csharp
IHandler<ShowContextMenuParameters, ShowContextMenuResponse> ShowContextMenuHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[ShowContextMenuParameters](DotNetBrowser.Browser.Handlers.ShowContextMenuParameters.md), [ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.md)\>

#### Remarks

<p>
    The passed <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuParameters" data-throw-if-not-resolved="false"></xref> object contains information about the context menu to show.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.Close" data-throw-if-not-resolved="false"></xref> method to close the context menu without choice.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.Select(DotNetBrowser.ContextMenu.ContextMenuItem)" data-throw-if-not-resolved="false"></xref> method to choose the context menu item.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.Close" data-throw-if-not-resolved="false"></xref> will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_Size"></a> Size

Gets or sets the browser size.

```csharp
Size Size { get; set; }
```

#### Property Value

 [Size](DotNetBrowser.Geometry.Size.md)

#### Remarks

<p>
    Setting this property updates the size of this Browser instance with the given width and height. Many web pages
    rely on the Browser's size and require that it's not empty. DOM document of a web page might not be loaded
    and displayed at all, because there's no sense in loading and rendering DOM document when it's empty.
</p>
<p>
    As a result, you should set the browser size programmatically when you don't need to display content of the
    loaded web page, but the web page must "think" it has been loaded in a browser instance
    with a non-empty size.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_StartDownloadHandler"></a> StartDownloadHandler

Gets or sets a handler that is used when the browser is about to start downloading the file.

```csharp
IHandler<StartDownloadParameters, StartDownloadResponse> StartDownloadHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[StartDownloadParameters](DotNetBrowser.Downloads.Handlers.StartDownloadParameters.md), [StartDownloadResponse](DotNetBrowser.Downloads.Handlers.StartDownloadResponse.md)\>

#### Remarks

<p>
    Use the <xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse.DownloadTo(System.String)" data-throw-if-not-resolved="false"></xref> method to
    confirm the download and specify the location to store the downloaded file.
</p>
<p>
    Use the<xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse.Cancel" data-throw-if-not-resolved="false"></xref> method if you do not need
    to download the file.
</p>
<p>
    If an exception occurs inside the handler implementation, the default behavior will be applied - the method
    <xref href="DotNetBrowser.Downloads.Handlers.StartDownloadResponse.Cancel" data-throw-if-not-resolved="false"></xref> will be used.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Downloads.IDownloads" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_TextFinder"></a> TextFinder

Gets the <xref href="DotNetBrowser.Search.ITextFinder" data-throw-if-not-resolved="false"></xref> instance that can be used for finding text on a web page loaded in the
browser.

```csharp
ITextFinder TextFinder { get; }
```

#### Property Value

 [ITextFinder](DotNetBrowser.Search.ITextFinder.md)

### <a id="DotNetBrowser_Browser_IBrowser_Title"></a> Title

Gets the title of the currently loaded web page.

```csharp
string Title { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_Touch"></a> Touch

Gets the <xref href="DotNetBrowser.Input.Touch.ITouch" data-throw-if-not-resolved="false"></xref> instance that can be used for listening touch input events.

```csharp
ITouch Touch { get; }
```

#### Property Value

 [ITouch](DotNetBrowser.Input.Touch.ITouch.md)

### <a id="DotNetBrowser_Browser_IBrowser_Url"></a> Url

Gets the URL of the currently loaded web page or an empty string if
the browser hasn't loaded any web page yet.

```csharp
string Url { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_UserAgent"></a> UserAgent

Gets or sets the <code>user-agent</code> of the current browser instance.

```csharp
string UserAgent { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_UserAgentMetadata"></a> UserAgentMetadata

Gets or sets the <code>user-agent metadata</code>, known as client hints, of the current browser instance.

```csharp
UserAgentMetadata UserAgentMetadata { get; set; }
```

#### Property Value

 [UserAgentMetadata](DotNetBrowser.Browser.UserAgentMetadata.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_UserDataProfiles"></a> UserDataProfiles

Gets the <xref href="DotNetBrowser.UserData.IUserDataProfiles" data-throw-if-not-resolved="false"></xref> instance that can be used for working with user data profiles
saved in the Chromium user data store.

```csharp
IUserDataProfiles UserDataProfiles { get; }
```

#### Property Value

 [IUserDataProfiles](DotNetBrowser.UserData.IUserDataProfiles.md)

### <a id="DotNetBrowser_Browser_IBrowser_Zoom"></a> Zoom

Gets the <xref href="DotNetBrowser.Zoom.IZoom" data-throw-if-not-resolved="false"></xref> instance that can be used for zooming content of a web page loaded in the current
browser instance.

```csharp
IZoom Zoom { get; }
```

#### Property Value

 [IZoom](DotNetBrowser.Zoom.IZoom.md)

## Methods

### <a id="DotNetBrowser_Browser_IBrowser_DisposeAsync_DotNetBrowser_Browser_BrowserDisposeOptions_"></a> DisposeAsync\(BrowserDisposeOptions\)

Asynchronously disposes the current browser instance according to the given options.

```csharp
Task<bool> DisposeAsync(BrowserDisposeOptions browserDisposeOptions)
```

#### Parameters

`browserDisposeOptions` [BrowserDisposeOptions](DotNetBrowser.Browser.BrowserDisposeOptions.md)

browser dispose options.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[bool](https://learn.microsoft.com/dotnet/api/system.boolean)\>

The task that represents the result of the asynchronous dispose process.
<code>True</code> indicates that the browser instance is successfully disposed without any dialogs,
<code>false</code> if the dispose process was canceled.
This may happen if the <xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.BeforeUnloadHandler" data-throw-if-not-resolved="false"></xref> handler was invoked and
the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.Stay" data-throw-if-not-resolved="false"></xref> response was sent.

#### Remarks

<p>
    If the currently loaded web page registers the <code>onbeforeunload</code> JavaScript event
    and the given options tell the browser to fire the <code>beforeunload</code>
    event, then this method will not dispose the browser right away.
</p>
<p>
    The <xref href="DotNetBrowser.Browser.Dialogs.IJsDialogs.BeforeUnloadHandler" data-throw-if-not-resolved="false"></xref> will be invoked
    in this case and if the handler tells the browser to stay on the web page, then the browser
    will not be disposed.
</p>
<p>
    The following example demonstrates how to dispose the browser instance as if a user
    manually clicking the close button of the tab/window.
</p>

<pre><code class="lang-csharp">browser.DisposeAsync(new BrowserDisposeOptions(){BeforeUnloadEventHandled = true});</code></pre>

<p>
    If the browser is already disposed, then this method does nothing.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_DownloadResource_System_String_"></a> DownloadResource\(string\)

Starts downloading the resource at the specified URL.

```csharp
void DownloadResource(string url)
```

#### Parameters

`url` [string](https://learn.microsoft.com/dotnet/api/system.string)

The URL of the resource to download.

#### Remarks

If the given URL is valid and points to a downloadable resource, then the
download process will be started. To control the download process, use
<xref href="DotNetBrowser.Browser.IBrowser.StartDownloadHandler" data-throw-if-not-resolved="false"></xref>.

<p>
    The method does nothing if the given URL is not well-formed or points to a resource
    that cannot be downloaded.
</p>

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">url</code> is null, empty, or consists only of white-space
characters.

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_Focus"></a> Focus\(\)

Tells the browser that it has focus and must be activated.

```csharp
void Focus()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_ReplaceMisspelledWord_System_String_"></a> ReplaceMisspelledWord\(string\)

Replaces misspelled word under cursor on the currently loaded web page with the given <code class="paramref">word</code>.
If there is no misspelled word under cursor, this method does nothing.

```csharp
void ReplaceMisspelledWord(string word)
```

#### Parameters

`word` [string](https://learn.microsoft.com/dotnet/api/system.string)

a string that represents the word for replacement

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">word</code> is null, empty, or consists only of white-space
characters.

### <a id="DotNetBrowser_Browser_IBrowser_SaveWebPage_System_String_System_String_DotNetBrowser_Browser_SavePageType_"></a> SaveWebPage\(string, string, SavePageType\)

Initiates the saving process of the currently loaded web page. The web page can be saved as a
single HTML file or the file with resources. Before saving a web page make sure that it is
not being loaded. It is recommended to completely loaded the web page and only then save it.

```csharp
bool SaveWebPage(string filePath, string resourcesPath, SavePageType saveType)
```

#### Parameters

`filePath` [string](https://learn.microsoft.com/dotnet/api/system.string)

an absolute path to a file in which the web page will be saved.

`resourcesPath` [string](https://learn.microsoft.com/dotnet/api/system.string)

an absolute path to a directory in which the resources (e.g. images, css)
of the web page will be saved. If the directory does not exist, it will
be created

`saveType` [SavePageType](DotNetBrowser.Browser.SavePageType.md)

determines how the web page will be saved: as an HTML file with all the
required resources (e.g. images, css etc.), a single HTML or MHTML file

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the saving process has been initialized successfully, <code>false</code> otherwise.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">filePath</code> is null, empty, or consists only of white-space
characters.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">resourcesPath</code> is null, empty, or consists only of
white-space characters.

### <a id="DotNetBrowser_Browser_IBrowser_SetPrivateKeyProviderPin_DotNetBrowser_Browser_CspParameters_"></a> SetPrivateKeyProviderPin\(CspParameters\)

Sets the key exchange PIN for the particular cryptographic
service provider (CSP) and the particular key container in it.
This functionality can be used to set the PIN that is requested when
trying to use a client certificate stored on the smart card.

```csharp
bool SetPrivateKeyProviderPin(CspParameters cspParameters)
```

#### Parameters

`cspParameters` [CspParameters](DotNetBrowser.Browser.CspParameters.md)

The parameters of the private key CSP container.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<code>true</code> if the PIN was set successfully, <code>false</code> otherwise.

#### Remarks

<p>
    This functionality is Windows-only. The implementation will
    return false in other environments.
</p>
<p>If the PIN was not set successfully, the actual error will be written to DotNetBrowser logs.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

The <code class="paramref">cspParameters</code> is null.

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

Any of the required parameters in <code class="paramref">cspParameters</code> is null, empty, or consists only of
white-space characters.

### <a id="DotNetBrowser_Browser_IBrowser_TakeImage"></a> TakeImage\(\)

Creates and returns an image of the currently loaded web page.

```csharp
Bitmap TakeImage()
```

#### Returns

 [Bitmap](DotNetBrowser.Ui.Bitmap.md)

a <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> that contains the image of the currently loaded web page.

#### Remarks

<p>
    The bitmap size depends on the size of the current browser instance and the device scale
    factor of the display where it is located at the moment. If the current browser size is
    empty, then the bitmap will be empty as well.
</p>
<p>
    For example, if the device scale factor of the display where the browser instance is
    located at the moment is 2.0 and the browser size is 100x100, then the size of the bitmap is
    expected to be 200x200.
</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

 [BitmapTimeoutException](DotNetBrowser.Browser.BitmapTimeoutException.md)

The <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> can not be retrieved within <code>10</code> seconds.

### <a id="DotNetBrowser_Browser_IBrowser_Unfocus"></a> Unfocus\(\)

Tells the browser that it does not have focus and must be deactivated.

```csharp
void Unfocus()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_IBrowser_BrowserBecameResponsive"></a> BrowserBecameResponsive

Occurs when the browser instance has become responsive.

```csharp
event EventHandler<BrowserBecameResponsiveEventArgs> BrowserBecameResponsive
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[BrowserBecameResponsiveEventArgs](DotNetBrowser.Browser.Events.BrowserBecameResponsiveEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_BrowserBecameUnresponsive"></a> BrowserBecameUnresponsive

Occurs when the browser instance has become unresponsive.

```csharp
event EventHandler<BrowserBecameUnresponsiveEventArgs> BrowserBecameUnresponsive
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[BrowserBecameUnresponsiveEventArgs](DotNetBrowser.Browser.Events.BrowserBecameUnresponsiveEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_ConsoleMessageReceived"></a> ConsoleMessageReceived

Occurs when the message was added to the console.

```csharp
event EventHandler<ConsoleMessageReceivedEventArgs> ConsoleMessageReceived
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[ConsoleMessageReceivedEventArgs](DotNetBrowser.Browser.Events.ConsoleMessageReceivedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_FaviconChanged"></a> FaviconChanged

Occurs when the web page favicon has changed.

```csharp
event EventHandler<FaviconChangedEventArgs> FaviconChanged
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FaviconChangedEventArgs](DotNetBrowser.Browser.Events.FaviconChangedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_FocusGained"></a> FocusGained

Occurs when the browser instance has gained the focus.

```csharp
event EventHandler<FocusGainedEventArgs> FocusGained
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FocusGainedEventArgs](DotNetBrowser.Browser.Events.FocusGainedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_FocusLost"></a> FocusLost

Occurs when the browser instance has lost the focus.

```csharp
event EventHandler<FocusLostEventArgs> FocusLost
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FocusLostEventArgs](DotNetBrowser.Browser.Events.FocusLostEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_FocusRequested"></a> FocusRequested

Occurs when JavaScript sends a request to focus the Browser instance by calling the
<code>window.focus()</code> method.

```csharp
event EventHandler<FocusRequestedEventArgs> FocusRequested
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FocusRequestedEventArgs](DotNetBrowser.Browser.Events.FocusRequestedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_FrameCreated"></a> FrameCreated

Occurs when the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> has been created.

```csharp
event EventHandler<FrameCreatedEventArgs> FrameCreated
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FrameCreatedEventArgs](DotNetBrowser.Browser.Events.FrameCreatedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_FrameDeleted"></a> FrameDeleted

Occurs when the <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref> has been deleted.

```csharp
event EventHandler<FrameDeletedEventArgs> FrameDeleted
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[FrameDeletedEventArgs](DotNetBrowser.Browser.Events.FrameDeletedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_MediaStreamCaptureStarted"></a> MediaStreamCaptureStarted

Occurs when the web page has started capturing an audio or video stream.

```csharp
event EventHandler<MediaStreamCaptureStartedEventArgs> MediaStreamCaptureStarted
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[MediaStreamCaptureStartedEventArgs](DotNetBrowser.Browser.Events.MediaStreamCaptureStartedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_MediaStreamCaptureStopped"></a> MediaStreamCaptureStopped

Occurs when the web page has stopped capturing an audio or video stream.

```csharp
event EventHandler<MediaStreamCaptureStoppedEventArgs> MediaStreamCaptureStopped
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[MediaStreamCaptureStoppedEventArgs](DotNetBrowser.Browser.Events.MediaStreamCaptureStoppedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_PdfDocumentLoadFailed"></a> PdfDocumentLoadFailed

Occurs when a PDF document failed to load in a frame.

```csharp
event EventHandler<PdfDocumentLoadFailedEventArgs> PdfDocumentLoadFailed
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PdfDocumentLoadFailedEventArgs](DotNetBrowser.Browser.Events.PdfDocumentLoadFailedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_PdfDocumentLoaded"></a> PdfDocumentLoaded

Occurs when a PDF document has been successfully loaded in a frame.

```csharp
event EventHandler<PdfDocumentLoadedEventArgs> PdfDocumentLoaded
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PdfDocumentLoadedEventArgs](DotNetBrowser.Browser.Events.PdfDocumentLoadedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_PrintPreviewClosed"></a> PrintPreviewClosed

Occurs when print preview dialog is closed.

```csharp
event EventHandler<PrintPreviewClosedEventArgs> PrintPreviewClosed
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PrintPreviewClosedEventArgs](DotNetBrowser.Browser.Events.PrintPreviewClosedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_PrintPreviewOpened"></a> PrintPreviewOpened

Occurs when print preview dialog is opened.

```csharp
event EventHandler<PrintPreviewOpenedEventArgs> PrintPreviewOpened
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[PrintPreviewOpenedEventArgs](DotNetBrowser.Browser.Events.PrintPreviewOpenedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_RenderProcessTerminated"></a> RenderProcessTerminated

Occurs when a render process has been terminated.

```csharp
event EventHandler<RenderProcessTerminatedEventArgs> RenderProcessTerminated
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[RenderProcessTerminatedEventArgs](DotNetBrowser.Browser.Events.RenderProcessTerminatedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_SpellCheckCompleted"></a> SpellCheckCompleted

Occurs when spell checking on the frame has been completed.

```csharp
event EventHandler<SpellCheckCompletedEventArgs> SpellCheckCompleted
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[SpellCheckCompletedEventArgs](DotNetBrowser.Browser.Events.SpellCheckCompletedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_StatusChanged"></a> StatusChanged

Occurs when the status text has been changed.

```csharp
event EventHandler<StatusChangedEventArgs> StatusChanged
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[StatusChangedEventArgs](DotNetBrowser.Browser.Events.StatusChangedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_TitleChanged"></a> TitleChanged

Occurs when the web page title has been changed.

```csharp
event EventHandler<TitleChangedEventArgs> TitleChanged
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[TitleChangedEventArgs](DotNetBrowser.Browser.Events.TitleChangedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_Browser_IBrowser_UpdateBoundsRequested"></a> UpdateBoundsRequested

Occurs when JavaScript requests to update bounds of the Browser instance.

```csharp
event EventHandler<UpdateBoundsRequestedEventArgs> UpdateBoundsRequested
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[UpdateBoundsRequestedEventArgs](DotNetBrowser.Browser.Events.UpdateBoundsRequestedEventArgs.md)\>

#### Remarks

JavaScript can request to update bounds of the Browser instance through the
following JavaScript functions:

<ul><li><span class="term">
            <code>window.moveTo()</code>
        </span>
            moves a window to the specified position.
        </li><li><span class="term">
            <code>window.moveBy()</code>
        </span>
            moves a window a specified number of pixels relative to its
            current coordinates.
        </li><li><span class="term">
            <code>window.resizeTo()</code>
        </span>
            resizes the window to the specified width and height.
        </li><li><span class="term">
            <code>window.resizeBy()</code>
        </span>
            resizes the window by the specified pixels.
        </li></ul>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

