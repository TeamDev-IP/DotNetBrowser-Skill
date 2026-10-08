# <a id="DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs"></a> Class TouchMovedEventArgs

Namespace: [DotNetBrowser.Input.Touch.Events](DotNetBrowser.Input.Touch.Events.md)  
Assembly: DotNetBrowser.dll  

```csharp
public sealed class TouchMovedEventArgs : TouchEventArgs, ITouchEventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[TouchEventArgs](DotNetBrowser.Input.Touch.Events.TouchEventArgs.md) ← 
[TouchMovedEventArgs](DotNetBrowser.Input.Touch.Events.TouchMovedEventArgs.md)

#### Implements

[ITouchEventArgs](DotNetBrowser.Input.Touch.Events.ITouchEventArgs.md)

#### Inherited Members

[TouchEventArgs.KeyModifiers](DotNetBrowser.Input.Touch.Events.TouchEventArgs.md\#DotNetBrowser\_Input\_Touch\_Events\_TouchEventArgs\_KeyModifiers), 
[TouchEventArgs.TouchPoints](DotNetBrowser.Input.Touch.Events.TouchEventArgs.md\#DotNetBrowser\_Input\_Touch\_Events\_TouchEventArgs\_TouchPoints), 
[TouchEventArgs.Equals\(object\)](DotNetBrowser.Input.Touch.Events.TouchEventArgs.md\#DotNetBrowser\_Input\_Touch\_Events\_TouchEventArgs\_Equals\_System\_Object\_), 
[TouchEventArgs.GetHashCode\(\)](DotNetBrowser.Input.Touch.Events.TouchEventArgs.md\#DotNetBrowser\_Input\_Touch\_Events\_TouchEventArgs\_GetHashCode), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs__ctor_DotNetBrowser_Input_Touch_Events_TouchPoint___"></a> TouchMovedEventArgs\(params TouchPoint\[\]\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchMovedEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchMovedEventArgs(params TouchPoint[] points)
```

#### Parameters

`points` [TouchPoint](DotNetBrowser.Input.Touch.Events.TouchPoint.md)\[\]

The touch points to add.

#### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">points</code> is null.

### <a id="DotNetBrowser_Input_Touch_Events_TouchMovedEventArgs__ctor_System_Collections_Generic_IEnumerable_DotNetBrowser_Input_Touch_Events_TouchPoint__"></a> TouchMovedEventArgs\(IEnumerable<TouchPoint\>\)

Initializes a new instance of the <xref href="DotNetBrowser.Input.Touch.Events.TouchMovedEventArgs" data-throw-if-not-resolved="false"></xref> with the specified touch points.

```csharp
public TouchMovedEventArgs(IEnumerable<TouchPoint> points)
```

#### Parameters

`points` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[TouchPoint](DotNetBrowser.Input.Touch.Events.TouchPoint.md)\>

The touch points to add.

#### Exceptions

 [InvalidEnumArgumentException](https://learn.microsoft.com/dotnet/api/system.componentmodel.invalidenumargumentexception)

No touch points with the required state are passed.

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The <code class="paramref">points</code> is null.

