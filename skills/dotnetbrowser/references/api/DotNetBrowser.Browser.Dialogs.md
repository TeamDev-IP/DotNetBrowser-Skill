# <a id="DotNetBrowser_Browser_Dialogs"></a> Namespace DotNetBrowser.Browser.Dialogs

### Namespaces

 [DotNetBrowser.Browser.Dialogs.Handlers](DotNetBrowser.Browser.Dialogs.Handlers.md)

### Interfaces

 [IDialogs](DotNetBrowser.Browser.Dialogs.md#DotNetBrowser_Browser_Dialogs_IDialogs)

The browser dialogs.

 [IJsDialogs](DotNetBrowser.Browser.Dialogs.md#DotNetBrowser_Browser_Dialogs_IJsDialogs)

The JavaScript dialogs.

## <a id="DotNetBrowser_Browser_Dialogs_IDialogs"></a> Interface IDialogs

Namespace: [DotNetBrowser.Browser.Dialogs](DotNetBrowser.Browser.Dialogs.md)  
Assembly: DotNetBrowser.dll  

The browser dialogs.

```csharp
public interface IDialogs : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_OpenDirectoryHandler"></a> OpenDirectoryHandler

Gets or sets a handler that is used  when the browser requests to display a file chooser dialog to open a
directory.

```csharp
IHandler<OpenDirectoryParameters, OpenDirectoryResponse> OpenDirectoryHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[OpenDirectoryParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_OpenDirectoryParameters), [OpenDirectoryResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_OpenDirectoryResponse)\>

##### Remarks

<p>
    You can use this handler to display the directory chooser dialog, or provide the chosen
    directory without displaying any dialogs.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse.SelectDirectory(System.String)" data-throw-if-not-resolved="false"></xref> method to provide the selected directory
    to
    the browser.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the dialog.</p>
<p>If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be used.</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_OpenExternalAppHandler"></a> OpenExternalAppHandler

Gets or sets a handler that is used when the currently loaded web page wants to open a link in the
associated external application.

```csharp
IHandler<OpenExternalAppParameters, OpenExternalAppResponse> OpenExternalAppHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[OpenExternalAppParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_OpenExternalAppParameters), [OpenExternalAppResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_OpenExternalAppResponse)\>

##### Remarks

<p>
    You can display your own dialog with the localized message that you can get
    from the parameters.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse.Open" data-throw-if-not-resolved="false"></xref> method to tell the browser that the link should be opened
    in
    the associated external application. If the application is not running, the operating system
    should launch the application and open the link in it.
</p>
<p>
    If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be
    invoked.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_OpenFileHandler"></a> OpenFileHandler

Gets or sets a handler that is used  when the browser requests to display a file chooser dialog to open a
file.

```csharp
IHandler<OpenFileParameters, OpenFileResponse> OpenFileHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[OpenFileParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_OpenFileParameters), [OpenFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_OpenFileResponse)\>

##### Remarks

<p>
    You can use this handler to display the file chooser, or provide the file without
    displaying any dialogs.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse.SelectFile(System.String)" data-throw-if-not-resolved="false"></xref> method to provide the selected file to the
    browser.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the dialog.</p>
<p>If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be invoked.</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_OpenMultipleFilesHandler"></a> OpenMultipleFilesHandler

Gets or sets a handler that is used when the browser requests to display a file chooser dialog to open several
files.

```csharp
IHandler<OpenMultipleFilesParameters, OpenMultipleFilesResponse> OpenMultipleFilesHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[OpenMultipleFilesParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_OpenMultipleFilesParameters), [OpenMultipleFilesResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_OpenMultipleFilesResponse)\>

##### Remarks

<p>
    You can use this handler to display the file chooser, or provide the files without
    displaying any dialogs.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse.SelectFiles(System.String%5b%5d)" data-throw-if-not-resolved="false"></xref> method to provide the selected files to
    the browser.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the dialog.</p>
<p>
    If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be
    invoked.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_RepostFormHandler"></a> RepostFormHandler

Gets or sets a handler that is used when a web page with POST data is going to be reloaded and the user must
confirm that the POST data can be resubmitted.

```csharp
IHandler<RepostFormParameters, RepostFormResponse> RepostFormHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[RepostFormParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_RepostFormParameters), [RepostFormResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_RepostFormResponse)\>

##### Remarks

<p>
    You can use this handler to display a confirmation dialog where you ask the user whether the
    web page can be reloaded or not.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse.Repost" data-throw-if-not-resolved="false"></xref> method to allow resubmitting POST data.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the page reloading.
</p>
<p>
    If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse.Repost" data-throw-if-not-resolved="false"></xref> method
    method will be used.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_SaveAsPdfHandler"></a> SaveAsPdfHandler

Gets or sets a handler that is used when the browser requests to display a file chooser dialog to save
content as PDF.

```csharp
IHandler<SaveAsPdfParameters, SaveAsPdfResponse> SaveAsPdfHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SaveAsPdfParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_SaveAsPdfParameters), [SaveAsPdfResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_SaveAsPdfResponse)\>

##### Remarks

<p>
    You can use this handler to display the save dialog, or provide the full file path
    without displaying any dialogs.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveAsPdfResponse.SaveToFile(System.String)" data-throw-if-not-resolved="false"></xref> method to provide the selected files to
    the browser.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveAsPdfResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the dialog.</p>
<p>
    If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveAsPdfResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be
    invoked.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_SaveFileHandler"></a> SaveFileHandler

Gets or sets a handler that is used when the browser requests to display a file chooser dialog
to save the file.

```csharp
IHandler<SaveFileParameters, SaveFileResponse> SaveFileHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SaveFileParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_SaveFileParameters), [SaveFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_SaveFileResponse)\>

##### Remarks

<p>
    You can use this handler to display the save dialog, or provide the full file path
    without displaying any dialogs.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse.SaveToFile(System.String)" data-throw-if-not-resolved="false"></xref> method to provide the selected files to
    the browser.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the dialog.</p>
<p>
    If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse.Cancel" data-throw-if-not-resolved="false"></xref> method
    will be invoked.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_SelectColorHandler"></a> SelectColorHandler

Gets or sets a handler that is used when the user clicks an <code>&lt;input type='color'&gt;</code> HTML5 element.

```csharp
IHandler<SelectColorParameters, SelectColorResponse> SelectColorHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[SelectColorParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_SelectColorParameters), [SelectColorResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_SelectColorResponse)\>

##### Remarks

<p>
    You
    can use this handler to display your own color chooser dialog or set the required color
    programmatically without displaying any dialogs.
</p>
<p>
    Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse.SelectColor(DotNetBrowser.Ui.Color)" data-throw-if-not-resolved="false"></xref> method to provide the selected color to
    the browser.
</p>
<p>Use the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse.Cancel" data-throw-if-not-resolved="false"></xref> method to cancel the dialog.</p>
<p>
    If the handler throws an exception, the <xref href="DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse.Cancel" data-throw-if-not-resolved="false"></xref> method will be
    invoked.
</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

## <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs"></a> Interface IJsDialogs

Namespace: [DotNetBrowser.Browser.Dialogs](DotNetBrowser.Browser.Dialogs.md)  
Assembly: DotNetBrowser.dll  

The JavaScript dialogs.

```csharp
public interface IJsDialogs : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs_AlertHandler"></a> AlertHandler

Gets or sets a handler that is used when JavaScript alert dialog should be displayed.

```csharp
IHandler<AlertParameters> AlertHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_1)<[AlertParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_AlertParameters)\>

##### Remarks

<p>
    In this callback you
    can display standard modal dialog with the message that you can get from <xref href="DotNetBrowser.Browser.Dialogs.Handlers.AlertParameters" data-throw-if-not-resolved="false"></xref>.
</p>
<p>Please note that it is not necessary to display a dialog in this handler.</p>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs_BeforeUnloadHandler"></a> BeforeUnloadHandler

Gets or sets a handler that is used when the web page is about to be unloaded.

```csharp
IHandler<BeforeUnloadParameters, BeforeUnloadResponse> BeforeUnloadHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[BeforeUnloadParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_BeforeUnloadParameters), [BeforeUnloadResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_BeforeUnloadResponse)\>

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs_ConfirmHandler"></a> ConfirmHandler

Gets or sets a handler that is used when JavaScript confirmation dialog should be displayed.

```csharp
IHandler<ConfirmParameters, ConfirmResponse> ConfirmHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[ConfirmParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_ConfirmParameters), [ConfirmResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_ConfirmResponse)\>

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.

#### <a id="DotNetBrowser_Browser_Dialogs_IJsDialogs_PromptHandler"></a> PromptHandler

Gets or sets a handler that is used when JavaScript dialog prompting the user to input some text should be
displayed.

```csharp
IHandler<PromptParameters, PromptResponse> PromptHandler { get; set; }
```

##### Property Value

 [IHandler](DotNetBrowser.Handlers.md#DotNetBrowser_Handlers_IHandler_2)<[PromptParameters](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_PromptParameters), [PromptResponse](DotNetBrowser.Browser.Dialogs.Handlers.md#DotNetBrowser_Browser_Dialogs_Handlers_PromptResponse)\>

##### Remarks

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

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.md#DotNetBrowser_Engine_ConnectionClosedException)

The connection to the Chromium engine is closed.
