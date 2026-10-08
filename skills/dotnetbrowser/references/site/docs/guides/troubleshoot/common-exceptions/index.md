
# Common Exceptions

**Lead**
This guide describes the common exceptions that can be thrown when working with the DotNetBrowser library.


## Initialization exceptions

### License exceptions

These exceptions are thrown when the license check fails for some reason.

* `NoLicenseException` is thrown when the license is missing. It usually happens when no license key is set in the `EngineOptions`, and DotNetBrowser cannot locate a `dotnetbrowser.license` file containing the license key. To troubleshoot this case, check if the license is [added to the project](https://teamdev.com/dotnetbrowser/docs/guides/installation/license/).
* `InvalidLicenseException` is thrown when the license is configured properly, but the license check fails. The exact reason of the license check failure is provided as the exception message. For instance, this exception can be thrown when the license is expired, or the product binding in the license does not match any of the namespaces.

For example, one of the possible `InvalidLicenseException` messages: `DotNetBrowser license check failed. Reason: This product version is incompatible with the license.`
It means that the license key specified in the project is incompatible with the referenced DotNetBrowser version. You need to make sure that the correct and valid key is used. 

Otherwise, feel free to contact our Sales team at [https://teamdev.com/contacts](https://teamdev.com/contacts/) to get the updated license.

### Chromium binaries exceptions

The `ChromiumBinariesMissingException` is thrown when DotNetBrowser cannot launch the bound Chromium engine because the Chromium binaries are missing and cannot be restored. The actual reason of the exception is provided as the exception message. For instance, this exception can be thrown when no compatible Chromium binaries are found in the [Chromium binaries directory](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#chromium-binaries-directory), and DotNetBrowser cannot find an assembly containing the compatible binaries.

#### Failed to extract the Chromium binaries in the separate process

This exception is thrown when the Chromium binaries were found in the assembly, however, there was an issue with extracting them to the Chromium binaries directory.

In most cases, the binaries extraction from the DLL is performed via `GZipCompress.exe`, a utility that is a part of DotNetBrowser. This utility may fail to extract the binaries for some reason. For example, if it is blocked by a third-party application (antivirus or firewall) or there is a lack of permissions for this operation. The following exception message is observed in this case: `Failed to extract the Chromium binaries in the separate process. GZipCompress.exe has exited with code <exit_code>`.

When this exception occurs, the detailed output of the `GZipCompress.exe` is written to [DotNetBrowser logs](https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/logging/). Examining the logs usually helps to understand the actual cause of the failure.

### Other engine initialization exceptions

The `EngineInitializationException` is thrown when something goes wrong during initializing the `IEngine` instance.

#### User data directory is already in use

It is not allowed to create two or more `IEngine` instances pointing to the same [user data directory](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#user-data-directory), even if those `IEngine` instances are created in separate .NET processes. Such use case is not supported by Chromium itself and leads to unpredictable behavior and sudden crashes of the engine.

As a result, when such case is detected, the `EngineInitializationException` is thrown with the following message:
`The user data directory is already in use: <path>`

There are a few possible solutions:

1. Create multiple `IBrowser` instances using the same `IEngine`:

**C#**
```csharp
IEngine engine = EngineFactory.Create(engineOptions);

IBrowser browser1 = engine.CreateBrowser();
IBrowser browser2 = engine.CreateBrowser();
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(engineOptions)

Dim browser1 As IBrowser = engine.CreateBrowser()
Dim browser2 As IBrowser = engine.CreateBrowser()
```



2. Create separate `IEngine` instances using different user data directories:

**C#**
```csharp
IEngine engine1 = EngineFactory.Create(new EngineOptions.Builder
{
    UserDataDirectory = @"C:\Users\Me\DotNetBrowser1"
}.Build());

IEngine engine2 = EngineFactory.Create(new EngineOptions.Builder
{
    UserDataDirectory = @"C:\Users\Me\DotNetBrowser2"
}.Build());

IBrowser browser1 = engine1.CreateBrowser();
IBrowser browser2 = engine2.CreateBrowser();
```

**VB**
```vb
Dim engine1 As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .UserDataDirectory = "C:\Users\Me\DotNetBrowser1"
}.Build())

Dim engine2 As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .UserDataDirectory = "C:\Users\Me\DotNetBrowser2"
}.Build())

Dim browser1 As IBrowser = engine1.CreateBrowser()
Dim browser2 As IBrowser = engine2.CreateBrowser()
```



## Runtime exceptions

### ObjectDisposedException

The `ObjectDisposedException` is thrown when there is an attempt to use an object which is already disposed. For example, this exception is thrown when working with:
* some previously cached DOM element or JavaScript object after loading a different web page;
* some frame that does not exist anymore in the browser;
* `IEngine` instance, any `IBrowser` instances created by this engine, or any other objects related to those instances after [the `IEngine.Dispose()` is called](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#engine-dispose);
* `IEngine` instance, any `IBrowser` instances created by this engine, or any other objects related to those instances after the [Chromium crash](https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/unexpected-termination/).

### ConnectionClosedException

The `ConnectionClosedException` is thrown when the connection to the Chromium engine appears to be closed. This exception is usually related to [`IEngine.Dispose()` method call](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#engine-dispose) or a [Chromium crash](https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/unexpected-termination/).

### Cross-thread operation not valid

When you try to modify UI on the DotNetBrowser event, you can see `System.InvalidOperationException` with the following description: `Cross-thread operation not valid: Control accessed from a thread other than the thread it was created on.`.

DotNetBrowser events may run on threads other than the main UI thread. To modify UI on the DotNetBrowser event, post the execution to the main UI thread using `BeginInvoke` in WinForms or `Dispatcher.BeginInvoke` in WPF. Avoid the blocking `Invoke` and `Dispatcher.Invoke` calls; see [Updating the UI from handlers and events](https://teamdev.com/dotnetbrowser/docs/guides/design/#updating-the-ui-from-handlers-and-events). The `Control.InvokeRequired` property in WinForms or the `Dispatcher.CheckAccess()` call in WPF can be used to check if it is necessary to pass the execution.

The code samples below demonstrate how to get access to UI from another thread.

#### WinForms


**C#**
```csharp
browser.Navigation.FrameLoadFinished += (s, e) =>
{
    if (e.Frame.IsMain)
    {
        if (InvokeRequired)
        {
            BeginInvoke(new Action(() =>
            {
                this.Text = e.Browser.Url;
            }));
        }
        else
        {
            this.Text = e.Browser.Url;
        }
    }
};
browser.Navigation.LoadUrl("https://www.teamdev.com");
```

**VB**
```vb
AddHandler browser.Navigation.FrameLoadFinished, Sub(s, e)
    If e.Frame.IsMain Then
        If InvokeRequired Then
            BeginInvoke(New Action(Sub()
                Me.Text = e.Browser.Url
            End Sub))
        Else
            Me.Text = e.Browser.Url
        End If
    End If
End Sub
browser.Navigation.LoadUrl("https://www.teamdev.com")
```



#### WPF


**C#**
```csharp
browser.Navigation.FrameLoadFinished += (s, e) =>
{
    if (e.Frame.IsMain)
    {
        if (!Dispatcher.CheckAccess())
        {
            Dispatcher.BeginInvoke(new Action(() =>
            {
                this.Title = e.Browser.Url;
            }));
        }
        else
        {
            this.Title = e.Browser.Url;
        }
    }
};
browser.Navigation.LoadUrl("https://www.teamdev.com");
```

**VB**
```vb
AddHandler browser.Navigation.FrameLoadFinished, Sub(s, e)
    If e.Frame.IsMain Then
        If Not Dispatcher.CheckAccess() Then
            Dispatcher.BeginInvoke(New Action(Sub()
                Me.Title = e.Browser.Url
            End Sub))
        Else
            Me.Title = e.Browser.Url
        End If
    End If
End Sub
browser.Navigation.LoadUrl("https://www.teamdev.com")
```



#### Avalonia UI

**C#**
```csharp
browser.Navigation.FrameLoadFinished += (s, e) =>
{
    if (e.Frame.IsMain)
    {
        if (!Dispatcher.UIThread.CheckAccess())
        {
            Dispatcher.UIThread.InvokeAsync(new Action(() =>
            {
                this.Title = e.Browser.Url;
            }));
        }
        else
        {
            this.Title = e.Browser.Url;
        }
    }
};
browser.Navigation.LoadUrl("https://www.teamdev.com");
```

**VB**
```vb
AddHandler browser.Navigation.FrameLoadFinished, Sub(s, e)
    If e.Frame.IsMain Then
        If Not Dispatcher.UIThread.CheckAccess() Then
            Dispatcher.UIThread.InvokeAsync(New Action(Sub()
                Me.Title = e.Browser.Url
            End Sub))
        Else
            Me.Title = e.Browser.Url
        End If
    End If
End Sub
browser.Navigation.LoadUrl("https://www.teamdev.com")
```

