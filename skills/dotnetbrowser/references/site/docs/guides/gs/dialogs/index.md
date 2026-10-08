
# Dialogs

**Lead**
This guide shows how to handle the requests to display various dialogs.


By default, DotNetBrowser does not display dialogs if you use `Browser` without associated `BrowserView`. It is set to the silent mode where all the dialogs are automatically closed as if the user clicked the **Cancel** button in the dialog.

To change the default behavior, register your own implementation of the appropriate handler for a particular dialog. In your implementation, you decide how to display the dialog and provide the results to the engine. You can also create and display every dialog with given parameters.

## JavaScript dialogs

### Alert

The JavaScript alert dialog is displayed when the `window.alert()` function is called. We use the `AlertHandler` for this.

In this handler, you can obtain the dialog parameters such as title, message, and localized text of the "OK" action.


**C#**
```csharp
browser.JsDialogs.AlertHandler =
    new Handler<AlertParameters>(p =>
    {
        // Dialog title.
        string title = p.Title;
        // Dialog message.
        string message = p.Message;
        // The localized text of the "OK" Handler action.
        string okActionText = p.OkActionText;
        // Create and display the dialog if necessary.
        
        /* 
        Return execution from the handler 
        as soon as the dialog has been closed. 
        */
    });
```

**VB**
```vb
browser.JsDialogs.AlertHandler = 
    New Handler(Of AlertParameters)(Sub(p)
        ' Dialog title.
        Dim title As String = p.Title
        ' Dialog message.
        Dim message As String = p.Message
        ' The localized text of the "OK" Handler action.
        Dim okActionText As String = p.OkActionText
        ' Create and display the dialog if necessary.

        ' Return execution from the handler
        ' as soon as the dialog has been closed.
    End Sub)
```



JavaScript execution will be blocked until the **Alert** dialog is closed.

### Confirm

The JavaScript confirm dialog is displayed when the `window.confirm()` function is called. We use the `ConfirmHandler` for this.

In this handler, you can obtain the dialog parameters such as title, message, localized text of the "Yes" and "No" actions. See the code sample below:


**C#**
```csharp
browser.JsDialogs.ConfirmHandler =
    new Handler<ConfirmParameters, ConfirmResponse>(p =>
    {
        // Dialog title.
        string title = p.Title;
        // Dialog message.
        string message = p.Message;
        // The localized text of the "OK" action.
        string okActionText = p.OkActionText;
        // The localized text of the "Cancel" action.
        string cancelActionText = p.CancelActionText;
        // Create and display the dialog if necessary.

        // Return execution from the handler 
        // as soon as the dialog has been closed.
        return ConfirmResponse.Ok();
    });
```

**VB**
```vb
browser.JsDialogs.ConfirmHandler = 
    New Handler(Of ConfirmParameters, ConfirmResponse)(Function(p)
        ' Dialog title.
        Dim title As String = p.Title
        ' Dialog message.
        Dim message As String = p.Message
        ' The localized text of the "OK" action.
        Dim okActionText As String = p.OkActionText
        ' The localized text of the "Cancel" action.
        Dim cancelActionText As String = p.CancelActionText
        ' Create and display the dialog if necessary.

        ' Return execution from the handler
        ' as soon as the dialog has been closed.
        Return ConfirmResponse.Ok()
    End Function)
```



JavaScript execution will be blocked until the **Confirm** dialog is closed.

### Prompt

The JavaScript prompt dialog is displayed when the `window.prompt()` function is called. We use the `PromptHandler` for this.

In this handler, you can obtain the dialog parameters such as title, message, text, localized text of the "OK" and "Cancel" actions. See the code sample below:


**C#**
```csharp
browser.JsDialogs.PromptHandler =
    new Handler<PromptParameters, PromptResponse>(p =>
    {
        // Dialog title.
        string title = p.Title;
        // Dialog message.
        string message = p.Message;
        // The localized text of the "OK" action.
        string okActionText = p.OkActionText;
        // The localized text of the "Cancel" action.
        string cancelActionText = p.CancelActionText;
        // Create and display the dialog if necessary.

        // Return execution from the handler 
        // as soon as the dialog has been closed.
        return PromptResponse.SubmitText(responseText);
    });
```

**VB**
```vb
browser.JsDialogs.PromptHandler = 
    New Handler(Of PromptParameters, PromptResponse)(Function(p)
        ' Dialog title.
        Dim title As String = p.Title
        ' Dialog message.
        Dim message As String = p.Message
        ' The localized text of the "OK" action.
        Dim okActionText As String = p.OkActionText
        ' The localized text of the "Cancel" action.
        Dim cancelActionText As String = p.CancelActionText
        ' Create and display the dialog if necessary.

        ' Return execution from the handler 
        ' as soon as the dialog has been closed.
        Return PromptResponse.SubmitText(responseText)
    End Function)
```



JavaScript execution will be blocked until the **Prompt** dialog is closed.

### BeforeUnload

The `onbeforeunload` event is fired when the web page is about to be unloaded. This event allows you to display a message in a confirmation dialog to inform the user whether they want to stay on the current page or leave it.

To display the confirmation dialog, use the `BeforeUnloadHandler`.

**Note**
This handler will not be invoked when closing `IBrowser` instance.


In this handler, you can obtain the dialog parameters such as title, message, localized text of the "Stay" and "Leave" actions. See the code sample below:


**C#**
```csharp
browser.JsDialogs.BeforeUnloadHandler =
    new Handler<BeforeUnloadParameters, BeforeUnloadResponse>(p =>
    {
        // Dialog title.
        string title = p.Title;
        // Dialog message.
        string message = p.Message;
        // The localized text of the "Stay" action.
        string stayActionText = p.StayActionText;
        // The localized text of the "Leave" action.
        string leaveActionText = p.LeaveActionText;
        // Create and display the dialog if necessary.
        // ...
        // The "Stay" action has been selected.
        return BeforeUnloadResponse.Stay();
    });
```

**VB**
```vb
browser.JsDialogs.BeforeUnloadHandler = 
    New Handler(Of BeforeUnloadParameters, BeforeUnloadResponse)(Function(p)
        ' Dialog title.
        Dim title As String = p.Title
        ' Dialog message.
        Dim message As String = p.Message
        ' The localized text of the "Stay" action.
        Dim stayActionText As String = p.StayActionText
        ' The localized text of the "Leave" action.
        Dim leaveActionText As String = p.LeaveActionText
        ' Create and display the dialog if necessary.
        ' ...
        ' The "Stay" action has been selected.
        Return BeforeUnloadResponse.Stay()
    End Function)
```



## Select a color

The dialog can be displayed when the user clicks the `input` element with the `color` type. We use the `SelectColorHandler` for this as shown in the code sample below:

```html
<input type="color" value="#ff0000">
```

In this handler, you can obtain the dialog parameters such as default color. For example:


**C#**
```csharp
browser.Dialogs.SelectColorHandler = 
    new Handler<SelectColorParameters, SelectColorResponse>(p =>
    {
        Color defaultColor = p.DefaultColor;
        return SelectColorResponse.SelectColor(new Color(1, 0, 0));
    });
```

**VB**
```vb
browser.Dialogs.SelectColorHandler = 
    New Handler(Of SelectColorParameters, SelectColorResponse)(Function(p)
        Dim defaultColor As Color = p.DefaultColor
        Return SelectColorResponse.SelectColor(New Color(1, 0, 0))
    End Function)
```



## Open file

When a web page wants a user to choose a file from their device storage, the `OpenFileHandler` is used. It happens when the user clicks the `input` element with the `file` type:

```html
<input type="file" accept="image/png, image/jpeg">
```

In this handler, you can obtain the dialog parameters such as default file name, acceptable file extensions, and description of the acceptable file extensions.  For example:


**C#**
```csharp
browser.Dialogs.OpenFileHandler =
    new Handler<OpenFileParameters, OpenFileResponse>(parameters =>
    {
        // The suggested directory.
        string initialDirectory = parameters.InitialDirectory;
        // Acceptable extensions.
        IEnumerable<string> acceptableExtensions = parameters.AcceptableExtensions;
        // ...
        // The given file should be opened.
        return OpenFileResponse.SelectFile(Path.GetFullPath("<path-to-selected-file>"));
    });
```

**VB**
```vb
browser.Dialogs.OpenFileHandler = 
    New Handler(Of OpenFileParameters, OpenFileResponse)(Function(parameters)
            ' The suggested directory.
            Dim initialDirectory As String = parameters.InitialDirectory
            ' Acceptable extensions.
            Dim acceptableExtensions As IEnumerable(Of String) = 
                parameters.AcceptableExtensions
            ' ...
            ' The given file should be opened.
        Return OpenFileResponse.SelectFile(Path.GetFullPath("<path-to-selected-file>"))
    End Function)
```



## Open files

When a web page asks a user to choose multiple files from the device storage, the `OpenMultipleFilesHandler` is used. It happens when the user clicks the `input` element with the `file` type and the `multiple` attribute:

```html
<input type="file" accept="image/png, image/jpeg" multiple>
```

In this handler, you can obtain the dialog parameters such as default file name, acceptable file extensions, and description of the acceptable file extensions. See the code sample below:


**C#**
```csharp
browser.Dialogs.OpenMultipleFilesHandler =
    new Handler<OpenMultipleFilesParameters, OpenMultipleFilesResponse>(parameters =>
    {
        // Acceptable extensions.
        IEnumerable<string> acceptableExtensions = parameters.AcceptableExtensions;
        // ...
        string file1 = Path.GetFullPath("<path-to-selected-file1>");
        string file2 = Path.GetFullPath("<path-to-selected-file2>");
        return OpenMultipleFilesResponse.SelectFiles(file1, file2);
    });
```

**VB**
```vb
browser.Dialogs.OpenMultipleFilesHandler = 
    New Handler(Of OpenMultipleFilesParameters, 
                    OpenMultipleFilesResponse)(Function(parameters)
            ' Acceptable extensions.
            Dim acceptableExtensions As IEnumerable(Of String) = 
                parameters.AcceptableExtensions
            ' ...
            Dim file1 As String = Path.GetFullPath("<path-to-selected-file1>")
            Dim file2 As String = Path.GetFullPath("<path-to-selected-file2>")
        Return OpenMultipleFilesResponse.SelectFiles(file1, file2)
    End Function)
```



## Open a folder

When Chromium wants a user to choose a folder from their device storage, the `OpenDirectoryHandler` is used.

If necessary, you can create and display a dialog where the user can choose the folder. When the dialog is closed, the `OpenDirectoryResponse` instance must be returned. See the code sample below:


**C#**
```csharp
browser.Dialogs.OpenDirectoryHandler =
    new Handler<OpenDirectoryParameters, OpenDirectoryResponse>(parameters =>
    {
        // ...
        string directory = Path.GetFullPath("<path-to-directory>");
        return OpenDirectoryResponse.SelectDirectory(directory);
    });
```

**VB**
```vb
browser.Dialogs.OpenDirectoryHandler = 
    New Handler(Of OpenDirectoryParameters, OpenDirectoryResponse)(Function(parameters)
        ' ...
        Dim directory As String = Path.GetFullPath("<path-to-directory>")
        Return OpenDirectoryResponse.SelectDirectory(directory)
    End Function)
```



## Save as PDF

When saving a web page as a PDF document through the [Print Preview](https://teamdev.com/dotnetbrowser/docs/guides/gs/printing/#print-preview) dialog, the `SaveAsPdfHandler` is used.

In this handler, you can obtain the dialog parameters, such as a default file name. See the code sample below:


**C#**
```csharp
browser.Dialogs.SaveAsPdfHandler =
    new Handler<SaveAsPdfParameters, SaveAsPdfResponse>(parameters =>
    {
        // ...
        // The given file should be saved.
        string pdfFile = Path.GetFullPath("<path-to-file>");
        return SaveAsPdfResponse.SaveToFile(pdfFile);
    });
```

**VB**
```vb
browser.Dialogs.SaveAsPdfHandler = 
    New Handler(Of SaveAsPdfParameters, SaveAsPdfResponse)(Function(parameters)
        ' ...
        ' The given file should be saved.
        Dim pdfFile As String = Path.GetFullPath("<path-to-file>")
        Return SaveAsPdfResponse.SaveToFile(pdfFile)
    End Function)
```



## Select a client certificate

When Chromium wants the user to select a client SSL certificate from the list of available certificates, the `SelectCertificateHandler` is used.

In this handler, you can obtain the dialog parameters such as dialog title, message, the list of available certificates. See the code sample below:


**C#**
```csharp
browser.SelectCertificateHandler = 
    new Handler<SelectCertificateParameters, SelectCertificateResponse>(p =>
    {
        // The dialog title.
        string title = p.Title;
        // The dialog message.
        string message = p.Message;
        // Available SSL certificates.
        IEnumerable<Certificate> certificates = p.Certificates;
        // ...
        // The last certificate in the list has been selected.
        return SelectCertificateResponse.Select(p.Certificates.Count() - 1);
    });
```

**VB**
```vb
browser.SelectCertificateHandler = 
    New Handler(Of SelectCertificateParameters, SelectCertificateResponse)(Function(p)
        ' The dialog title.
        Dim title As String = p.Title
        ' The dialog message.
        Dim message As String = p.Message
        ' Available SSL certificates.
        Dim certificates As IEnumerable(Of Certificate) = p.Certificates
        ' ...
        ' The last certificate in the list has been selected.
        Return SelectCertificateResponse.Select(p.Certificates.Count() - 1)
    End Function)
```



## Open external application

When a user navigates to a URL with a scheme associated with the application installed in the operating system, Chromium tries to open the link in this external application. DotNetBrowser routes every
external-protocol request to this callback, including
script-initiated requests and `mailto:` links.

In this handler, you can obtain the dialog parameters, such as the localized title, message, and the text for the "Open.." and "Cancel" actions.

For example, here is how to cancel opening the link without displaying any dialogs:


**C#**
```csharp
browser.Dialogs.OpenExternalAppHandler =
    new Handler<OpenExternalAppParameters, OpenExternalAppResponse>(p =>
    {
        if (IsTrusted(p.Url))
        {
            return OpenExternalAppResponse.Open();
        }

        return OpenExternalAppResponse.Cancel();
    });
```

**VB**
```vb
browser.Dialogs.OpenExternalAppHandler = 
    New Handler(Of OpenExternalAppParameters, OpenExternalAppResponse)(Function(p)
        If IsTrusted(p.Url) Then
            Return OpenExternalAppResponse.Open()
        End If

        Return OpenExternalAppResponse.Cancel()
    End Function)
```


