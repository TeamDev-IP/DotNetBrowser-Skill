# <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs"></a> Interface IJsDialogs

Namespace: [DotNetBrowser.Browser.Dialogs](DotNetBrowser.Browser.Dialogs.md)  
Assembly: DotNetBrowser.dll  

The JavaScript dialogs.

```csharp
public interface IJsDialogs : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs_AlertHandler"></a> AlertHandler

Gets or sets a handler that is used when JavaScript alert dialog should be displayed.

```csharp
IHandler<AlertParameters> AlertHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-1.md)<[AlertParameters](DotNetBrowser.Browser.Dialogs.Handlers.AlertParameters.md)\>

#### Remarks

<p>
    In this callback you
    can display standard modal dialog with the message that you can get from <xref href="DotNetBrowser.Browser.Dialogs.Handlers.AlertParameters" data-throw-if-not-resolved="false"></xref>.
</p>
<p>Please note that it is not necessary to display a dialog in this handler.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs_BeforeUnloadHandler"></a> BeforeUnloadHandler

Gets or sets a handler that is used when the web page is about to be unloaded.

```csharp
IHandler<BeforeUnloadParameters, BeforeUnloadResponse> BeforeUnloadHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[BeforeUnloadParameters](DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadParameters.md), [BeforeUnloadResponse](DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.md)\>

#### Remarks

<p>
    Some web pages may override the <code>window.onbeforeunload</code> JavaScript function, so that a
    confirmation dialog will be shown every time when the user tries to reload a web page or navigate
    to another web page. You can use this callback to display an appropriate confirmation message
    dialog to ask the user if they really want to leave or reload the web page. To find out whether
    the web page is going to be reloaded you can check the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadParameters.Cause" data-throw-if-not-resolved="false"></xref>
    property.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.Stay" data-throw-if-not-resolved="false"></xref> method to stay on the current web page.
</p>
<p>Use the  <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.Leave" data-throw-if-not-resolved="false"></xref> method to reload or navigate to another web page.</p>
<p>If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.BeforeUnloadResponse.Leave" data-throw-if-not-resolved="false"></xref> method will be used.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs_ConfirmHandler"></a> ConfirmHandler

Gets or sets a handler that is used when JavaScript confirmation dialog should be displayed.

```csharp
IHandler<ConfirmParameters, ConfirmResponse> ConfirmHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[ConfirmParameters](DotNetBrowser.Browser.Dialogs.Handlers.ConfirmParameters.md), [ConfirmResponse](DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse.md)\>

#### Remarks

<p>
    In this
    handler you can display standard modal dialog with the message that you can get from
    <xref href="DotNetBrowser.Browser.Dialogs.Handlers.ConfirmParameters" data-throw-if-not-resolved="false"></xref>. Please note that it is not necessary to display a dialog in this
    handler.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse.Ok" data-throw-if-not-resolved="false"></xref> to notify that the JavaScript dialog is closed
    with the "OK" action.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to dismiss the dialog.</p>
<p>If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.ConfirmResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be used.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs_PromptHandler"></a> PromptHandler

Gets or sets a handler that is used when JavaScript dialog prompting the user to input some text should be
displayed.

```csharp
IHandler<PromptParameters, PromptResponse> PromptHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[PromptParameters](DotNetBrowser.Browser.Dialogs.Handlers.PromptParameters.md), [PromptResponse](DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse.md)\>

#### Remarks

<p>
    The passed <xref href="DotNetBrowser.Browser.Dialogs.Handlers.PromptParameters" data-throw-if-not-resolved="false"></xref> object contains the text of the prompt message and the default
    response text. You can use this information to display standard modal dialog to obtain a
    prompt response from user. Please note that it is not necessary to display a dialog in this
    callback.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse.SubmitText(System.String)" data-throw-if-not-resolved="false"></xref> method to close the dialog and pass the text value passed
    as a parameter to the engine.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the dialog.</p>
<p>If the callback throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.PromptResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be used.</p>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

