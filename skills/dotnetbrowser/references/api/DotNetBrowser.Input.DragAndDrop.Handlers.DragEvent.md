# <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent"></a> Class DragEvent

Namespace: [DotNetBrowser.Input.DragAndDrop.Handlers](DotNetBrowser.Input.DragAndDrop.Handlers.md)  
Assembly: DotNetBrowser.dll  

Represents drag and drop event and provides access to the event data.

```csharp
public sealed class DragEvent
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DragEvent](DotNetBrowser.Input.DragAndDrop.Handlers.DragEvent.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent_DataObject"></a> DataObject

Gets the Windows-specific representation of the drop data.

```csharp
public IDataObject DataObject { get; }
```

#### Property Value

 [IDataObject](https://learn.microsoft.com/dotnet/api/system.runtime.interopservices.comtypes.idataobject)

#### Remarks

This functionality is available for .NET Framework on Windows only when the "--enable-com-in-drag-drop" Chromium
switch is specified.

### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent_DropData"></a> DropData

Gets the general representation  of the drop data.

```csharp
public IDropData DropData { get; }
```

#### Property Value

 IDropData

### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent_Location"></a> Location

Gets the location of the mouse cursor in the browser's coordinate system at the time the
event occurred.

```csharp
public Point Location { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent_ScreenLocation"></a> ScreenLocation

Gets the location of the mouse cursor in the screen's coordinate system at the time the
event occurred.

```csharp
public Point ScreenLocation { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

