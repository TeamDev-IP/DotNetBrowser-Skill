# <a id="DotNetBrowser_Browser_Dialogs_IDialogs"></a> Interface IDialogs

Namespace: [DotNetBrowser.Browser.Dialogs](DotNetBrowser.Browser.Dialogs.md)  
Assembly: DotNetBrowser.dll  

The browser dialogs.

```csharp
public interface IDialogs : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_OpenDirectoryHandler"></a> OpenDirectoryHandler

Gets or sets a handler that is used  when the browser requests to display a file chooser dialog to open a
directory.

```csharp
IHandler<OpenDirectoryParameters, OpenDirectoryResponse> OpenDirectoryHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[OpenDirectoryParameters](DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryParameters.md), [OpenDirectoryResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenDirectoryResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_OpenExternalAppHandler"></a> OpenExternalAppHandler

Gets or sets a handler that is used when the currently loaded web page wants to open a link in the
associated external application.

```csharp
IHandler<OpenExternalAppParameters, OpenExternalAppResponse> OpenExternalAppHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[OpenExternalAppParameters](DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppParameters.md), [OpenExternalAppResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenExternalAppResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_OpenFileHandler"></a> OpenFileHandler

Gets or sets a handler that is used  when the browser requests to display a file chooser dialog to open a
file.

```csharp
IHandler<OpenFileParameters, OpenFileResponse> OpenFileHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[OpenFileParameters](DotNetBrowser.Browser.Dialogs.Handlers.OpenFileParameters.md), [OpenFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenFileResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_OpenMultipleFilesHandler"></a> OpenMultipleFilesHandler

Gets or sets a handler that is used when the browser requests to display a file chooser dialog to open several
files.

```csharp
IHandler<OpenMultipleFilesParameters, OpenMultipleFilesResponse> OpenMultipleFilesHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[OpenMultipleFilesParameters](DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesParameters.md), [OpenMultipleFilesResponse](DotNetBrowser.Browser.Dialogs.Handlers.OpenMultipleFilesResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_RepostFormHandler"></a> RepostFormHandler

Gets or sets a handler that is used when a web page with POST data is going to be reloaded and the user must
confirm that the POST data can be resubmitted.

```csharp
IHandler<RepostFormParameters, RepostFormResponse> RepostFormHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[RepostFormParameters](DotNetBrowser.Browser.Dialogs.Handlers.RepostFormParameters.md), [RepostFormResponse](DotNetBrowser.Browser.Dialogs.Handlers.RepostFormResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_SaveAsPdfHandler"></a> SaveAsPdfHandler

Gets or sets a handler that is used when the browser requests to display a file chooser dialog to save
content as PDF.

```csharp
IHandler<SaveAsPdfParameters, SaveAsPdfResponse> SaveAsPdfHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SaveAsPdfParameters](DotNetBrowser.Browser.Dialogs.Handlers.SaveAsPdfParameters.md), [SaveAsPdfResponse](DotNetBrowser.Browser.Dialogs.Handlers.SaveAsPdfResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_SaveFileHandler"></a> SaveFileHandler

Gets or sets a handler that is used when the browser requests to display a file chooser dialog
to save the file.

```csharp
IHandler<SaveFileParameters, SaveFileResponse> SaveFileHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SaveFileParameters](DotNetBrowser.Browser.Dialogs.Handlers.SaveFileParameters.md), [SaveFileResponse](DotNetBrowser.Browser.Dialogs.Handlers.SaveFileResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Browser_Dialogs_IDialogs_SelectColorHandler"></a> SelectColorHandler

Gets or sets a handler that is used when the user clicks an <code>&lt;input type='color'&gt;</code> HTML5 element.

```csharp
IHandler<SelectColorParameters, SelectColorResponse> SelectColorHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SelectColorParameters](DotNetBrowser.Browser.Dialogs.Handlers.SelectColorParameters.md), [SelectColorResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectColorResponse.md)\>

#### Remarks

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

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

