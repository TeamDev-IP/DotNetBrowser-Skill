# <a id="DotNetBrowser_Input_Touch_ITouch"></a> Interface ITouch

Namespace: [DotNetBrowser.Input.Touch](DotNetBrowser.Input.Touch.md)  
Assembly: DotNetBrowser.dll  

A service that can be used for touch input handling.

```csharp
public interface ITouch : IAutoDisposable
```

#### Implements

[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Properties

### <a id="DotNetBrowser_Input_Touch_ITouch_Canceled"></a> Canceled

Occurs when the touch has been canceled.

```csharp
IInterceptableInputEvent<ITouchEventArgs, TouchCanceledEventArgs> Canceled { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.ITouchEventArgs.md), [TouchCanceledEventArgs](DotNetBrowser.Input.Touch.Events.TouchCanceledEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Touch_ITouch_Ended"></a> Ended

Occurs when the touch has been ended.

```csharp
IInterceptableInputEvent<ITouchEventArgs, TouchEndedEventArgs> Ended { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.ITouchEventArgs.md), [TouchEndedEventArgs](DotNetBrowser.Input.Touch.Events.TouchEndedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Touch_ITouch_Moved"></a> Moved

Occurs when the touch has moved.

```csharp
IInterceptableInputEvent<ITouchEventArgs, TouchMovedEventArgs> Moved { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.ITouchEventArgs.md), [TouchMovedEventArgs](DotNetBrowser.Input.Touch.Events.TouchMovedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

### <a id="DotNetBrowser_Input_Touch_ITouch_Started"></a> Started

Occurs when the touch has been started.

```csharp
IInterceptableInputEvent<ITouchEventArgs, TouchStartedEventArgs> Started { get; }
```

#### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.IInterceptableInputEvent\-2.md)<[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.ITouchEventArgs.md), [TouchStartedEventArgs](DotNetBrowser.Input.Touch.Events.TouchStartedEventArgs.md)\>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

