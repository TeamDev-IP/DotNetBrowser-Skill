# <a id="DotNetBrowser_DevTools_IDevTools"></a> Interface IDevTools

Namespace: [DotNetBrowser.DevTools](DotNetBrowser.DevTools.md)  
Assembly: DotNetBrowser.dll  

Allows working with Chromium Developer Tools and access the remote debugging URL of the currently
loaded web page in the browser instance associated with this DevTools instance.

```csharp
public interface IDevTools : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_DevTools_IDevTools_RemoteDebuggingUrl"></a> RemoteDebuggingUrl

Gets the remote debugging URL of the currently loaded web page in the browser instance associated with this
DevTools
instance.

```csharp
string RemoteDebuggingUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

## Methods

### <a id="DotNetBrowser_DevTools_IDevTools_Hide"></a> Hide\(\)

Closes the Chromium Developer Tools window if any is shown.

```csharp
void Hide()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

### <a id="DotNetBrowser_DevTools_IDevTools_Show"></a> Show\(\)

Opens the Chromium Developer Tools panel in a new window. This method does nothing if the DevTools window is
already shown.

```csharp
void Show()
```

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> has already been disposed.

