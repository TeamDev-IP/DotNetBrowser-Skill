# <a id="DotNetBrowser_Input_Touch_Events_ITouchEventArgs"></a> Interface ITouchEventArgs

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

Event arguments for the <xref href="DotNetBrowser.Input.Touch.ITouch" data-throw-if-not-resolved="false"></xref> events associated with a surface touch.

```csharp
public interface ITouchEventArgs
```

## Properties

### <a id="DotNetBrowser_Input_Touch_Events_ITouchEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
IKeyModifiers KeyModifiers { get; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Touch_Events_ITouchEventArgs_TouchPoints"></a> TouchPoints

Gets the list of all detected touch points.

```csharp
IReadOnlyList<ITouchPoint> TouchPoints { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ITouchPoint](DotNetBrowser.Input.Touch.Events.ITouchPoint.md)\>

