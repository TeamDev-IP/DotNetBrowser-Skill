# <a id="DotNetBrowser_Input_Touch"></a> Namespace DotNetBrowser.Input.Touch

### Namespaces

 [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)

### Interfaces

 [ITouch](DotNetBrowser.Input.Touch.md#DotNetBrowser_Input_Touch_ITouch)

A service that can be used for touch input handling.

## <a id="DotNetBrowser_Input_Touch_ITouch"></a> Interface ITouch

Namespace: [DotNetBrowser.Input.Touch](DotNetBrowser.Input.Touch.md)  
Assembly: DotNetBrowser.dll  

A service that can be used for touch input handling.

```csharp
public interface ITouch : IAutoDisposable
```

##### Implements

[IAutoDisposable](DotNetBrowser.md#DotNetBrowser_IAutoDisposable)

### Properties

#### <a id="DotNetBrowser_Input_Touch_ITouch_Canceled"></a> Canceled

Occurs when the touch has been canceled.

```csharp
IInterceptableInputEvent<ITouchEventArgs, TouchCanceledEventArgs> Canceled { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs), [TouchCanceledEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchCanceledEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Input_Touch_ITouch_Ended"></a> Ended

Occurs when the touch has been ended.

```csharp
IInterceptableInputEvent<ITouchEventArgs, TouchEndedEventArgs> Ended { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs), [TouchEndedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchEndedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Input_Touch_ITouch_Moved"></a> Moved

Occurs when the touch has moved.

```csharp
IInterceptableInputEvent<ITouchEventArgs, TouchMovedEventArgs> Moved { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs), [TouchMovedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.

#### <a id="DotNetBrowser_Input_Touch_ITouch_Started"></a> Started

Occurs when the touch has been started.

```csharp
IInterceptableInputEvent<ITouchEventArgs, TouchStartedEventArgs> Started { get; }
```

##### Property Value

 [IInterceptableInputEvent](DotNetBrowser.Input.md#DotNetBrowser_Input_IInterceptableInputEvent_2)<[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_ITouchEventArgs), [TouchStartedEventArgs](DotNetBrowser.Input.Touch.Events.md#DotNetBrowser_Input_Touch_Events_TouchStartedEventArgs)\>

##### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> object has already been disposed.
