
# Design

**Lead**
This document provides an overview of the design of the library as well as general rules to help you understand how to interact with it.


## Objects

All the library objects can be divided into the following categories: 
* service objects;
* immutable data objects.

Service objects allow performing some operations when data objects just hold the data. Service objects can use the data objects.

Objects like `IEngine`, `IBrowser`, `IProfile` `IBrowserSettings`, `IFrame`, `IDocument`, `IJsObject` instances are *service objects*. While `EngineOptions`, `Size`, `Rectangle` are *immutable data objects*.

### Instantiation

To create an immutable data object or a service object, use its constructor, builder, or one of its static methods. Here is an example of using the builder:


**C#**
```csharp
EngineOptions options = new EngineOptions.Builder 
{
    RenderingMode = RenderingMode.HardwareAccelerated,
    Language = Language.EnglishUs
}.Build();
IEngine engine = EngineFactory.Create(options);
```

**VB**
```vb
Dim options As EngineOptions = New EngineOptions.Builder With 
{
    .RenderingMode = RenderingMode.HardwareAccelerated,
    .Language = Language.EnglishUs
}.Build()
Dim engine As IEngine = EngineFactory.Create(options)
```




### Destruction

Every service object that must be disposed manually implements the `IDisposable` interface. To dispose a service object and release all allocated memory and resources, call the `IDisposable.Dispose()` method. For example:


**C#**
```csharp
engine.Dispose();
```

**VB**
```vb
engine.Dispose()
```



Some service objects such as `IFrame` can be disposed automatically, for example, when the web page is unloaded. These objects implement the `IAutoDisposable` interface.

**Important**
If you use an already disposed object, `ObjectDisposedException` occurs.


### Relationship

The lifecycle of a service object can depend on the lifecycle of another object. When the service object is disposed, all service objects depending on it are released automatically. For example: 
* When you dispose the `IEngine`, all its `IBrowser` instances are released automatically; 
* When you dispose the `IBrowser`, all its `IFrame` instances are disposed automatically.

## Methods

Methods that return `Task<T>` instance are executed asynchronously. If the method returns some value, it is executed synchronously blocking the current thread execution until the return value is received.

## Handlers

Each object that allows registering handlers has the properties of type `IHandler<in T>` or `IHandler<in T, out TResult>` interface. 
To register and unregister a handler, use the property setters and getters.

There are default implementations of the `IHandler<in T, out TResult>` interface:
 - `Handler<T, TResult>` class allows wrapping lambdas and method groups;
 - `AsyncHandler<T, TResult>` class allows wrapping async lambdas and method groups or lambdas and method groups that return `Task<TResult>`.
 
### Async
 
Example below demonstrates how to register an asynchronous handler that returns a `Task` to provide a response asynchronously:


**C#**
```csharp
browser.ShowContextMenuHandler =
    new AsyncHandler<ShowContextMenuParameters, ShowContextMenuResponse
    >(ShowContextMenu);

// An async method that is declared in the same class.
private async Task<ShowContextMenuResponse> ShowContextMenu(ShowContextMenuParameters p)
{
    // ...
}
```

**VB**
```vb
browser.ShowContextMenuHandler = 
    New AsyncHandler(Of ShowContextMenuParameters, ShowContextMenuResponse)(
        AddressOf ShowContextMenu)

' An async method that is declared in the same class.
Private Async Function ShowContextMenu(p As ShowContextMenuParameters) As Task(Of ShowContextMenuResponse)
    ' ...
End Function
```



The task result can be provided asynchronously from a different thread.

**Important**
Provide a response through the returned `Task` argument, otherwise `IEngine` waits for the response until termination.


### Sync

Example below demonstrates how to register and unregister a regular `Handler` that returns response through a return value:


**C#**
```csharp
browser.CreatePopupHandler =
    new Handler<CreatePopupParameters, CreatePopupResponse>(p =>
    {
        return CreatePopupResponse.Create();
    });
```

**VB**
```vb
browser.CreatePopupHandler = 
    New Handler(Of CreatePopupParameters, CreatePopupResponse)(Function(p)
        Return CreatePopupResponse.Create()
    End Function)
```



### How handlers run

When you implement a handler, keep in mind:

* Chromium waits for the response of a handler before it continues the
  request, the navigation, or the dialog that the handler answers, so a slow
  handler delays the operation it answers.
* Handlers are called on thread-pool threads, not on the UI thread. Several
  handlers can run at the same time, for example for parallel network
  requests, so the handler code must be thread safe.
* Keyboard, mouse, and touch handlers of `IBrowser.Keyboard`, `IBrowser.Mouse`,
  and `IBrowser.Touch` are an exception. In the off-screen rendering mode and
  on macOS, they run on the thread that delivers the input, which is usually
  the UI thread. Keep them fast, or the UI freezes.
* If a handler throws an exception, DotNetBrowser writes it to the
  [log](https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/logging/), which is disabled by default. Catch
  the exceptions inside the handler and return an explicit response.
* Some handlers block the browser or the engine until they return. Their API
  reference says that calling browser or engine methods inside the handler is
  not allowed. For example, `INavigation.StartNavigationHandler` does not allow
  browser method calls, and `INavigation.ShowHttpErrorPageHandler` does not
  allow engine method calls. Use only the handler parameters to decide on the
  response.

## Events

DotNetBrowser reports notifications through regular .NET events, for example
`IEngine.Disposed` or `INavigation.FrameLoadFinished`.

Event handlers run on internal event threads, not on the UI thread.
DotNetBrowser uses several event threads, for example one for the navigation
events of each browser. Each thread delivers its events one by one, so a slow
event handler delays the events queued after it on the same thread. Events from
different threads can run at the same time, even events of one object: for
example, `IBrowser.TitleChanged` and `IBrowser.FrameCreated` use different
threads. Synchronize access to data that several event handlers share.

The `Disposed` event of most objects is raised synchronously on the thread that
calls `Dispose()`. `IEngine.Disposed` is different: it is raised when the
Chromium main process exits, including after a crash, so it can arrive on any
thread.

## Thread safety

**Note**
The library is thread safe: one can safely use DotNetBrowser objects in different threads.


### Updating the UI from handlers and events

Handlers and events run on threads other than the UI thread, except for the
input handlers described above. A `Disposed` event can also run on
the thread that calls `Dispose()`, which can be the UI thread.
UI frameworks allow changing controls only on the UI thread. WPF and Avalonia
UI throw `InvalidOperationException` otherwise, and WinUI 3 throws
`COMException`. Windows Forms throws `InvalidOperationException` reliably only
under the debugger; without the debugger, the call can fail unpredictably. Post UI
updates to the UI thread with a non-blocking call:

* `Dispatcher.BeginInvoke()` in WPF;
* `Control.BeginInvoke()` in Windows Forms;
* `DispatcherQueue.TryEnqueue()` in WinUI 3;
* `Dispatcher.UIThread.Post()` in Avalonia UI.

For examples, see
[Cross-thread operation not valid](https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/common-exceptions/#cross-thread-operation-not-valid).

Do not block a handler while waiting for the UI thread, for example with
`Dispatcher.Invoke()` or `Control.Invoke()`. If the UI thread is waiting at that
moment for a DotNetBrowser call that cannot complete until the handler returns,
the two threads wait for each other. The UI freezes until the call times out and
throws `TimeoutException`. In an event handler, a blocking call also delays the
events queued after it until the UI thread becomes free.
