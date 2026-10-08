
# Migrating to DotNetBrowser version 1.7+

**Lead**
In DotNetBrowser 1.7, several changes to public API have been introduced. These changes may require adjustments to your application’s source code. This guide shows how to change your application’s source code written with the previous version of API (for example, DotNetBrowser 1.6.4) to the new API introduced in DotNetBrowser version 1.7.


## Frames IDs

**1.6.4**<br>
The `Browser.GetFramesIds()` method returns IDs of all frames on the currently loaded web page. It does not allow to get IDs of the frames located inside another frame. 

**C#**<br>
```csharp
var framesIds = browser.GetFramesIds();
```

**VB.NET**<br>
```vb
Dim framesIds = browser.GetFramesIds()
```

**1.7**<br>
Now, the `Browser.GetFramesIds()` method returns IDs of the main frame only. To get IDs of frames located inside other frames, the `Browser.GetFramesIds(long frameId)` method has been introduced.

**C#**<br>
```csharp
List<long> framesIds = browser.GetFramesIds();

foreach (long framesId in framesIds) {
    List<long> subFramesIds = browser.GetFramesIds(framesId);
}
```

**VB.NET**<br>
```vb
Dim framesIds As List(Of Long) = browser.GetFramesIds()

For Each framesId As Long In framesIds
    Dim subFramesIds As List(Of Long) = browser.GetFramesIds(framesId)
Next
```

## Working with BrowserFunction

**1.6.4**<br>
To register a global JavaScript function, the `Browser.RegisterFunction(String functionName, BrowserFunction function)` method is used. Every time when the web page is loaded, DotNetBrowser creates a function with the functionName and attaches it to the window JavaScript global object.

**C#**<br>
```csharp
public class MyFunction: BrowserFunction{
            public JSValue invoke(params JSValue[] args)
            {
                    return JSValue.CreateNull();
            }
}
// Usage
browser.RegisterFunction("save", new MyrFunction());
```

**VB.NET**<br>
```vb
Public Class MyFunction
    Implements BrowserFunction

    Public Function invoke(ParamArray args As JSValue()) As JSValue _
        Implements BrowserFunction.invoke
        Return JSValue.CreateNull()
    End Function
End Class

'Usage'
browser.RegisterFunction("save", New MyrFunction())
```

The function will be injected into JavaScript of each loaded web page until you un-register it using the `Browser.UnregisterFunction(String functionName)` method.

**1.7**<br>
BrowserFunction API has become a part of JSObject class. Now, to register global JavaScript function, you need to use the following code sample:

**C#**<br>
```csharp
    public class SaveObject
        {
            public void Save(String firstName, String lastName)
            {
                Console.Out.WriteLine("firstName = " + firstName);
                Console.Out.WriteLine("lastName = " + lastName);
            }
        }

// Usage

browser.FinishLoadingFrameEvent += delegate(object sender, FinishLoadingEventArgs e)
            {
                if (e.IsMainFrame)
                {
                    JSValue value = browser.ExecuteJavaScriptAndReturnValue("window");
                    value.AsObject().SetProperty("save", new SaveObject());
                }
            };
```

**VB.NET**<br>
```vb
Public Class SaveObject
    Public Sub Save(ByVal firstName As String, ByVal lastName As String)
        Console.Out.WriteLine("firstName = " & firstName)
        Console.Out.WriteLine("lastName = " & lastName)
    End Sub
End Class

'Usage'
AddHandler browser.FinishLoadingFrameEvent sub(ByVal sender As Object, ByVal e As FinishLoadingEventArgs)

    If e.IsMainFrame Then
        Dim value As JSValue = browser.ExecuteJavaScriptAndReturnValue("window")
        value.AsObject().SetProperty("save", New SaveObject())
    End If
End sub
```

Every time when you load/reload the web page, you must inject the object into JavaScript. The object will be removed automatically when another web page is loaded, or an existing page is reloaded.

## Print to PDF

**1.6.4**<br>
To print currently loaded web page to PDF document, in DotNetBrowser version 1.6.4, the `Browser.PrintToPDF()` method is used. This method prints a web page to a PDF document with predefined settings. The code sample below demonstrates how to print a web page to a PDF file and get a notification when printing is complete:

**C#**<br>
```csharp
browser.PrintToPDF("web_page.pdf", delegate(object sender, PrintJobEventArgs e)
{
    //This handler will be invoked when printing is finished.
});
```

**VB.NET**<br>
```vb
browser.PrintToPDF("web_page.pdf", sub(ByVal sender As Object, ByVal e As PrintJobEventArgs)
    'This handler will be invoked when printing is finished.'
End sub)
```

**1.7**<br>
In DotNetBrowser version 1.7, we extended Printing API and added functionality that allows to decide whether web page should be printed using a printer device or saved as a PDF document. We removed `Browser.PrintToPDF()` method. Now, you must decide in your `PrintHandler` implementation whether the web page is saved as a PDF or printed using a printer device. The code sample below demonstrates how to handle printing, tell Chromium to save the web page as PDF document with the given print settings, and get a notification when printing is complete:

**C#**<br>
```csharp
class MyPDFPrintHandler : PrintHandler
{
    Func<PrintSettings, PrintSettings> func;

    public MyPDFPrintHandler(Func<PrintSettings, PrintSettings> func)
    {
        this.func = func;
    }

    public PrintStatus OnPrint(PrintJob printJob)
    {
        PrintSettings printSettings = func(printJob.PrintSettings);
        printSettings.PrintToPDF = true;
        printSettings.Landscape = true;
        printSettings.PrintBackgrounds = true;
        printSettings.PageMargins = new PageMargins(20, 40, 40, 20);
        printJob.PrintJobEvent += (s, e) =>
        {
            //This handler will be invoked when printing is finished.
        };
        return PrintStatus.CONTINUE;
    }
}

// Usage

browser.PrintHandler = new MyPDFPrintHandler((printSettings) =>
{
    printSettings.PDFFilePath = fileName;
    return printSettings;
});

browser.Print();
```

**VB.NET**<br>
```vb
Class MyPDFPrintHandler
    Implements PrintHandler

    Private func As Func(Of PrintSettings, PrintSettings)

    Public Sub New(ByVal func As Func(Of PrintSettings, PrintSettings))
        Me.func = func
    End Sub

    Public Function OnPrint(ByVal printJob As PrintJob) As PrintStatus _
        Implements PrintHandler.OnPrint
        Dim printSettings As PrintSettings = func(printJob.PrintSettings)
        printSettings.PrintToPDF = True
        printSettings.Landscape = True
        printSettings.PrintBackgrounds = True
        printSettings.PageMargins = New PageMargins(20, 40, 40, 20)
        AddHandler printJob.PrintJobEvent, sub(s, e)
            'This handler will be invoked when printing is finished.'
        End sub

        Return PrintStatus.CONTINUE
    End Function
End Class

'Usage'
browser.PrintHandler = New MyPDFPrintHandler(Function(printSettings)
    printSettings.PDFFilePath = fileName
    Return printSettings
End Function)
browser.Print()
```
