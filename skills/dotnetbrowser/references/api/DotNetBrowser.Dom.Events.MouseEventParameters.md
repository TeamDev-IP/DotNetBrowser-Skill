# <a id="DotNetBrowser_Dom_Events_MouseEventParameters"></a> Class MouseEventParameters

Namespace: [DotNetBrowser.Dom.Events](DotNetBrowser.Dom.Events.md)  
Assembly: DotNetBrowser.dll  

Represents the DOM mouse event parameters.

```csharp
public class MouseEventParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MouseEventParameters](DotNetBrowser.Dom.Events.MouseEventParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Dom_Events_MouseEventParameters_Button"></a> Button

Gets or sets the number of the mouse button that was pressed to trigger the event.

```csharp
public uint Button { get; set; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

### <a id="DotNetBrowser_Dom_Events_MouseEventParameters_ClickCount"></a> ClickCount

Gets or sets the click count.

```csharp
public uint ClickCount { get; set; }
```

#### Property Value

 [uint](https://learn.microsoft.com/dotnet/api/system.uint32)

### <a id="DotNetBrowser_Dom_Events_MouseEventParameters_ClientLocation"></a> ClientLocation

Gets or sets the location of the mouse cursor in the component's coordinate system at the time the event
occurred.

```csharp
public Point ClientLocation { get; set; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Dom_Events_MouseEventParameters_ScreenLocation"></a> ScreenLocation

Gets or sets the location of the mouse cursor in the screen's coordinate
system at the time the event occurred.

```csharp
public Point ScreenLocation { get; set; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Dom_Events_MouseEventParameters_UiEventModifierParameters"></a> UiEventModifierParameters

Gets or sets the DOM UI event parameters with the key modifiers.

```csharp
public UiEventModifierParameters UiEventModifierParameters { get; set; }
```

#### Property Value

 [UiEventModifierParameters](DotNetBrowser.Dom.Events.UiEventModifierParameters.md)

