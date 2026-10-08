
# Migrating from 2.2 to 2.3

**Lead**
In DotNetBrowser 2.3 the Chromium engine has been upgraded to version 84. This Chromium version has several breaking changes in the source code that affect the public API of product. In this migration guide we describe what API has been removed/changed in 2.3 and what alternatives you should use instead.


## Removed API

### Network

#### Overriding HTTP request readers

The `SendHeadersHandler` and `SendProxyHeadersHandler` have been removed in Chromium 84.

**v2.2**


**C#**
```csharp
network.SendHeadersHandler =
    new Handler<SendHeadersParameters, SendHeadersResponse>((parameters) =>
    {
        IEnumerable<IHttpHeader> headers = parameters.Headers;
        List<HttpHeader> newHttpHeaders = headers.Cast<HttpHeader>().ToList();
        newHttpHeaders.Add(new HttpHeader("<header-name>", "<header-value>"));
        return SendHeadersResponse.OverrideHeaders(newHttpHeaders);
    });

// ...

network.SendProxyHeadersHandler =
    new Handler<SendProxyHeadersParameters, SendProxyHeadersResponse>(p =>
    {
        IEnumerable<IHttpHeader> headers = p.Headers;
        List<HttpHeader> newHttpHeaders = headers.Cast<HttpHeader>().ToList();
        newHttpHeaders.Add(new HttpHeader("<header-name>", "<header-value>"));
        return SendProxyHeadersResponse.OverrideHeaders(newHttpHeaders);
    });
```

**VB**
```vb
network.SendHeadersHandler = 
    New Handler(Of SendHeadersParameters, SendHeadersResponse)(Function(parameters)
        Dim headers As IEnumerable(Of IHttpHeader) = parameters.Headers
        Dim newHttpHeaders As List(Of HttpHeader) = headers.Cast(Of HttpHeader)().ToList()
        newHttpHeaders.Add(New HttpHeader("<header-name>", "<header-value>"))
        Return SendHeadersResponse.OverrideHeaders(newHttpHeaders)
End Function)

' ...

network.SendProxyHeadersHandler = 
    New Handler(Of SendProxyHeadersParameters, SendProxyHeadersResponse)(Function(p)
        Dim headers As IEnumerable(Of IHttpHeader) = p.Headers
        Dim newHttpHeaders As List(Of HttpHeader) = headers.Cast(Of HttpHeader)().ToList()
        newHttpHeaders.Add(New HttpHeader("<header-name>", "<header-value>"))
        Return SendProxyHeadersResponse.OverrideHeaders(newHttpHeaders)
End Function)
```



**v2.3**

To override the HTTP headers before they will be sent to a web server use the `INetwork.StartTransactionHandler` API:


**C#**
```csharp
INetwork.StartTransactionHandler = 
    new Handler<StartTransactionParameters, StartTransactionResponse>(p =>
    {
        IEnumerable<IHttpHeader> headers = p.Headers;
        List<HttpHeader> newHttpHeaders = headers.Cast<HttpHeader>().ToList();
        newHttpHeaders.Add(new HttpHeader("<header-name>", "<header-value>"));
        return StartTransactionResponse.OverrideHeaders(newHttpHeaders);
    });
```

**VB**
```vb
INetwork.StartTransactionHandler = 
    New Handler(Of StartTransactionParameters, StartTransactionResponse)(Function(p)
        Dim headers As IEnumerable(Of IHttpHeader) = p.Headers
        Dim newHttpHeaders As List(Of HttpHeader) = headers.Cast(Of HttpHeader)().ToList()
        newHttpHeaders.Add(New HttpHeader("<header-name>", "<header-value>"))
        Return StartTransactionResponse.OverrideHeaders(newHttpHeaders)
End Function)
```



#### Filtering resources

The `LoadResourceHandler` handler has been removed in Chromium 84.

**v2.2**


**C#**
```csharp
engine.Network.LoadResourceHandler =
    new Handler<LoadResourceParameters, LoadResourceResponse>(p =>
    {
        if (p.ResourceType == ResourceType.Image)
        {
            return LoadResourceResponse.Cancel();
        }
        return LoadResourceResponse.Continue();
    });
```

**VB**
```vb
engine.Network.LoadResourceHandler = 
    New Handler(Of LoadResourceParameters, LoadResourceResponse)(Function(p)
        If p.ResourceType = ResourceType.Image Then
            Return LoadResourceResponse.Cancel()
        End If
        Return LoadResourceResponse.Continue()
End Function)
```



**v2.3**

The `SendUrlRequestHandler` should be used instead. In DotNetBrowser 2.3, it also provides an ability to cancel the request:


**C#**
```csharp
engine.Network.SendUrlRequestHandler =
    new Handler<SendUrlRequestParameters, SendUrlRequestResponse>(p =>
    {
        if (p.ResourceType == ResourceType.Image)
        {
            return SendUrlRequestResponse.Cancel();
        }
        return SendUrlRequestResponse.Continue();
    });
```

**VB**
```vb
engine.Network.SendUrlRequestHandler = 
    New Handler(Of SendUrlRequestParameters, SendUrlRequestResponse)(Function(p)
        If p.ResourceType = ResourceType.Image Then
            Return SendUrlRequestResponse.Cancel()
        End If
        Return SendUrlRequestResponse.Continue()
End Function)
```



#### The RequestCompleted event

The `RequestCompletedEventArgs.IsStarted` property has been removed because now the URL Request cannot be completed if it hasn’t been started. So, there’s no sense in this property because it always returns `true`.

### Navigation

#### The FrameLoadFailed event

The `FrameLoadFailedEventArgs.ErrorDescription` property has been removed. It is no longer supported in Chromium 84.

## Added or updated API

### URL Request

The `UrlRequest` class has been extended with the `Browser`, `ResourceType`, `SslVersion` properties.  All these properties can be used to obtain more information about this URL request, including the browser that initiated this request, the type of the requested resource, and the SSL version used to perform this request. 

As a result, it is now possible to obtain the bound `IBrowser` instance in `InterceptRequestHandler` :


**C#**
```csharp
Engine.Network.InterceptRequestHandler =
    new Handler<InterceptRequestParameters, InterceptRequestResponse>(data =>
    {
        //Access the browser bound to the URL request.
        IBrowser browser = data.UrlRequest.Browser;
        //Tell the Chromium engine to handle this request.
        return InterceptRequestResponse.Proceed();
    });
```

**VB**
```vb
Engine.Network.InterceptRequestHandler = 
    New Handler(Of InterceptRequestParameters, InterceptRequestResponse)(Function(data)
        ' Access the browser bound to the URL request.
        Dim browser As IBrowser = data.UrlRequest.Browser
        ' Tell the Chromium engine to handle this request.
        Return InterceptRequestResponse.Proceed()
End Function)
```



### Save as PDF

The `SuggestedFileName` and `SuggestedDirectory`properties were added to the `SaveAsPdfParameters`.


**C#**
```csharp
browser.Dialogs.SaveAsPdfHandler =
    new Handler<SaveAsPdfParameters, SaveAsPdfResponse>(p =>
    {
        // The given file should be saved.
        string pdfFile = Path.Combine(p.SuggestedDirectory, p.SuggestedFileName);
        return SaveAsPdfResponse.SaveToFile(pdfFile);
    });
```

**VB**
```vb
browser.Dialogs.SaveAsPdfHandler = 
    New Handler(Of SaveAsPdfParameters, SaveAsPdfResponse)(Function(p)
        ' The given file should be saved.
        Dim pdfFile As String = Path.Combine(p.SuggestedDirectory, p.SuggestedFileName)
        Return SaveAsPdfResponse.SaveToFile(pdfFile)
End Function)
```



### Drag and Drop

The `EnterDragHandler` and `DropHandler` are added to `IDragAndDrop`. These handlers can be used to intercept the corresponding drag and drop events on the web page in the hardware-accelerated rendering mode. For example:


**C#**
```csharp
browser.DragAndDrop.EnterDragHandler = new Handler<EnterDragParameters>(OnDragEnter);
browser.DragAndDrop.DropHandler = new Handler<DropParameters>(OnDrop);

// ...

private void OnDragEnter(EnterDragParameters arg)
{
    if (arg.Event.DropData != null)
    {
        //Write file names to debug output.
        foreach (IFileValue file in arg.Event.DropData.Files)
        {
            Debug.WriteLine($"OnDragEnter: File = {file?.FileName}");
        }
    }
}
private void OnDrop(DropParameters arg)
{
    if (arg.Event.DropData != null)
    {
        //Write file names to debug output.
        foreach (IFileValue file in arg.Event.DropData.Files)
        {
            Debug.WriteLine($"OnDrop: File = {file?.FileName}");
        }
    }
}
```

**VB**
```vb
browser.DragAndDrop.EnterDragHandler = New Handler(Of EnterDragParameters)(OnDragEnter)
browser.DragAndDrop.DropHandler = New Handler(Of DropParameters)(OnDrop)

' ...

Private Sub OnDragEnter(ByVal arg As EnterDragParameters)
    If arg.Event.DropData IsNot Nothing Then
        ' Write file names to debug output.
        For Each file As IFileValue In arg.Event.DropData.Files
            Debug.WriteLine($"OnDragEnter: File = {file?.FileName}")
        Next file
    End If
End Sub
Private Sub OnDrop(ByVal arg As DropParameters)
    If arg.Event.DropData IsNot Nothing Then
        ' Write file names to debug output.
        For Each file As IFileValue In arg.Event.DropData.Files
            Debug.WriteLine($"OnDrop: File = {file?.FileName}")
        Next file
    End If
End Sub
```



In .NET Framework, it is also possible to work with the `IDataObject` instance in the scope of these handlers to receive and process the platform-specific representation of the dragged and dropped data. This functionality becomes available when the `--enable-com-in-drag-drop` [Chromium switch](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#chromium-switches) is specified. For example:


**C#**
```csharp
private void OnDragEnter(EnterDragParameters arg)
{
    System.Runtime.InteropServices.ComTypes.IDataObject dataObject = arg.Event.DataObject;
    if (dataObject != null)
    {
        //Process IDataObject contents.
    }
}
private void OnDrop(DropParameters arg)
{
    System.Runtime.InteropServices.ComTypes.IDataObject dataObject = arg.Event.DataObject;
    if (dataObject != null)
    {
        //Process IDataObject contents.
    }
}
```

**VB**
```vb
Private Sub OnDragEnter(ByVal arg As EnterDragParameters)
    Dim dataObject As System.Runtime.InteropServices.ComTypes.IDataObject = 
        arg.Event.DataObject
    If dataObject IsNot Nothing Then
        ' Process IDataObject contents.
    End If
End Sub
Private Sub OnDrop(ByVal arg As DropParameters)
    Dim dataObject As System.Runtime.InteropServices.ComTypes.IDataObject = 
        arg.Event.DataObject
    If dataObject IsNot Nothing Then
        ' Process IDataObject contents.
    End If
End Sub
```



### DOM

#### DOM key events

The `DomKeyCode` enumeration is introduced and used in DOM key events instead of the existing `KeyCode` enumeration. The previous implementation of obtaining the key code relied on the obsolete DOM API, and appeared to work improperly in some cases.

The `Character` property is also added to DOM key events to provide an actuat character when it is available for the DOM event.
