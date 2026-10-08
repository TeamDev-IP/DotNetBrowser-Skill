# <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs"></a> Class TouchEventArgs

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public abstract class TouchEventArgs : ITouchEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[TouchEventArgs](DotNetBrowser.Input.Touch.Events.TouchEventArgs.md)

#### Derived

[TouchCanceledEventArgs](DotNetBrowser.Input.Touch.Events.TouchCanceledEventArgs.md), 
[TouchEndedEventArgs](DotNetBrowser.Input.Touch.Events.TouchEndedEventArgs.md), 
[TouchMovedEventArgs](DotNetBrowser.Input.Touch.Events.TouchMovedEventArgs.md), 
[TouchStartedEventArgs](DotNetBrowser.Input.Touch.Events.TouchStartedEventArgs.md)

#### Implements

[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.ITouchEventArgs.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs__ctor_System_Collections_Generic_IEnumerable_DotNetBrowser_Input_Touch_Events_TouchPoint__"></a> TouchEventArgs\(IEnumerable<TouchPoint\>\)

Initializes a new instance of <xref href="DotNetBrowser.Input.Touch.Events.TouchEventArgs" data-throw-if-not-resolved="false"></xref>.

```csharp
protected TouchEventArgs(IEnumerable<TouchPoint> touchPoints)
```

#### Parameters

`touchPoints` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[TouchPoint](DotNetBrowser.Input.Touch.Events.TouchPoint.md)\>

The touch points to add.

#### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

## Properties

### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs_KeyModifiers"></a> KeyModifiers

Gets the keyboard modifiers.

```csharp
public IKeyModifiers KeyModifiers { get; set; }
```

#### Property Value

 [IKeyModifiers](DotNetBrowser.Input.Keyboard.Events.IKeyModifiers.md)

### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs_TouchPoints"></a> TouchPoints

Gets the list of all detected touch points.

```csharp
public IReadOnlyList<ITouchPoint> TouchPoints { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[ITouchPoint](DotNetBrowser.Input.Touch.Events.ITouchPoint.md)\>

## Methods

### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_Input_Touch_Events_TouchEventArgs_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

