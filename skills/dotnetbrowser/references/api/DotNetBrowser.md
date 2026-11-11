# <a id="DotNetBrowser"></a> Namespace DotNetBrowser

### Namespaces

 [DotNetBrowser.AvaloniaUi](DotNetBrowser.AvaloniaUi.md)

 [DotNetBrowser.Browser](DotNetBrowser.Browser.md)

 [DotNetBrowser.Cache](DotNetBrowser.Cache.md)

 [DotNetBrowser.Capture](DotNetBrowser.Capture.md)

 [DotNetBrowser.Card](DotNetBrowser.Card.md)

 [DotNetBrowser.Cast](DotNetBrowser.Cast.md)

 [DotNetBrowser.Chromium](DotNetBrowser.Chromium.md)

 [DotNetBrowser.ContextMenu](DotNetBrowser.ContextMenu.md)

 [DotNetBrowser.Cookies](DotNetBrowser.Cookies.md)

 [DotNetBrowser.DevTools](DotNetBrowser.DevTools.md)

 [DotNetBrowser.Dom](DotNetBrowser.Dom.md)

 [DotNetBrowser.Downloads](DotNetBrowser.Downloads.md)

 [DotNetBrowser.Engine](DotNetBrowser.Engine.md)

 [DotNetBrowser.Extensions](DotNetBrowser.Extensions.md)

 [DotNetBrowser.Frames](DotNetBrowser.Frames.md)

 [DotNetBrowser.Geometry](DotNetBrowser.Geometry.md)

 [DotNetBrowser.Handlers](DotNetBrowser.Handlers.md)

 [DotNetBrowser.Input](DotNetBrowser.Input.md)

 [DotNetBrowser.Js](DotNetBrowser.Js.md)

 [DotNetBrowser.Logging](DotNetBrowser.Logging.md)

 [DotNetBrowser.Media](DotNetBrowser.Media.md)

 [DotNetBrowser.Navigation](DotNetBrowser.Navigation.md)

 [DotNetBrowser.Net](DotNetBrowser.Net.md)

 [DotNetBrowser.Passwords](DotNetBrowser.Passwords.md)

 [DotNetBrowser.Permissions](DotNetBrowser.Permissions.md)

 [DotNetBrowser.Plugins](DotNetBrowser.Plugins.md)

 [DotNetBrowser.Print](DotNetBrowser.Print.md)

 [DotNetBrowser.Profile](DotNetBrowser.Profile.md)

 [DotNetBrowser.Search](DotNetBrowser.Search.md)

 [DotNetBrowser.SpellCheck](DotNetBrowser.SpellCheck.md)

 [DotNetBrowser.Ui](DotNetBrowser.Ui.md)

 [DotNetBrowser.UserData](DotNetBrowser.UserData.md)

 [DotNetBrowser.WinForms](DotNetBrowser.WinForms.md)

 [DotNetBrowser.WinUi3](DotNetBrowser.WinUi3.md)

 [DotNetBrowser.Wpf](DotNetBrowser.Wpf.md)

 [DotNetBrowser.Zoom](DotNetBrowser.Zoom.md)

### Interfaces

 [IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

Represents the object which can be disposed by itself (without the explicit Dispose method call).

 [IAutoDisposable<TArgs\>](DotNetBrowser.md#DotNetBrowser_IAutoDisposable_1)

Represents the object which can be disposed by itself (without the explicit Dispose method call).

## <a id="DotNetBrowser_IAutoDisposable"></a> Interface IAutoDisposable

Namespace: [DotNetBrowser](DotNetBrowser.md)  
Assembly: DotNetBrowser.dll  

Represents the object which can be disposed by itself (without the explicit Dispose method call).

```csharp
public interface IAutoDisposable
```

### Properties

#### <a id="DotNetBrowser_IAutoDisposable_IsDisposed"></a> IsDisposed

Indicates if the object is already disposed.

```csharp
bool IsDisposed { get; }
```

##### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### <a id="DotNetBrowser_IAutoDisposable_Disposed"></a> Disposed

Occurs when the object has been disposed.

```csharp
event EventHandler Disposed
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler)

## <a id="DotNetBrowser_IAutoDisposable_1"></a> Interface IAutoDisposable<TArgs\>

Namespace: [DotNetBrowser](DotNetBrowser.md)  
Assembly: DotNetBrowser.dll  

Represents the object which can be disposed by itself (without the explicit Dispose method call).

```csharp
public interface IAutoDisposable<TArgs> : IAutoDisposable
```

##### Type Parameters

`TArgs` 

The type of the event arguments for the <xref href="DotNetBrowser.IAutoDisposable%601.Disposed" data-throw-if-not-resolved="false"></xref>
event.

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

#### <a id="DotNetBrowser_IAutoDisposable_1_Disposed"></a> Disposed

Occurs when the object has been disposed.

```csharp
event EventHandler<TArgs> Disposed
```

##### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<TArgs\>
