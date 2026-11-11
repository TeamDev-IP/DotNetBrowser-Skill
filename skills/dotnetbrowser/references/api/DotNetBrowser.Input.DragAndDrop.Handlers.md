# <a id="DotNetBrowser_Input_DragAndDrop_Handlers"></a> Namespace DotNetBrowser.Input.DragAndDrop.Handlers

### Classes

 [DragAndDropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters)

The base class for all <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> handlers parameters.

 [DragEvent](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent)

Represents drag and drop event and provides access to the event data.

 [DropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DropParameters)

The parameters of the <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop.DropHandler" data-throw-if-not-resolved="false"></xref>.

 [EnterDragParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_EnterDragParameters)

The parameters of the <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop.EnterDragHandler" data-throw-if-not-resolved="false"></xref>.

## <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters"></a> Class DragAndDropParameters

Namespace: [DotNetBrowser.Input.DragAndDrop.Handlers](DotNetBrowser.Input.DragAndDrop.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for all <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> handlers parameters.

```csharp
public class DragAndDropParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DragAndDropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters)

##### Derived

[DropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DropParameters), 
[EnterDragParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_EnterDragParameters)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters_DragAndDrop"></a> DragAndDrop

Gets the <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> instance the handler is associated with.

```csharp
public IDragAndDrop DragAndDrop { get; }
```

##### Property Value

 [IDragAndDrop](DotNetBrowser.Input.DragAndDrop.md#DotNetBrowser_Input_DragAndDrop_IDragAndDrop)

#### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters_Event"></a> Event

Gets the drag and drop event.

```csharp
public DragEvent Event { get; }
```

##### Property Value

 [DragEvent](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent)

## <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent"></a> Class DragEvent

Namespace: [DotNetBrowser.Input.DragAndDrop.Handlers](DotNetBrowser.Input.DragAndDrop.Handlers.md)  
Assembly: DotNetBrowser.dll  

Represents drag and drop event and provides access to the event data.

```csharp
public sealed class DragEvent
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DragEvent](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent)

##### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

### Properties

#### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent_DataObject"></a> DataObject

Gets the Windows-specific representation of the drop data.

```csharp
public IDataObject DataObject { get; }
```

##### Property Value

 [IDataObject](https://learn.microsoft.com/dotnet/api/system.runtime.interopservices.comtypes.idataobject)

##### Remarks

This functionality is available for .NET Framework on Windows only when the "--enable-com-in-drag-drop" Chromium
switch is specified.

#### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent_DropData"></a> DropData

Gets the general representation  of the drop data.

```csharp
public IDropData DropData { get; }
```

##### Property Value

 IDropData

#### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent_Location"></a> Location

Gets the location of the mouse cursor in the browser's coordinate system at the time the
event occurred.

```csharp
public Point Location { get; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

#### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragEvent_ScreenLocation"></a> ScreenLocation

Gets the location of the mouse cursor in the screen's coordinate system at the time the
event occurred.

```csharp
public Point ScreenLocation { get; }
```

##### Property Value

 [Point](DotNetBrowser.Geometry.md#DotNetBrowser_Geometry_Point)

## <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DropParameters"></a> Class DropParameters

Namespace: [DotNetBrowser.Input.DragAndDrop.Handlers](DotNetBrowser.Input.DragAndDrop.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop.DropHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public class DropParameters : DragAndDropParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DragAndDropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters) ← 
[DropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DropParameters)

##### Inherited Members

[DragAndDropParameters.DragAndDrop](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters_DragAndDrop), 
[DragAndDropParameters.Event](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters_Event), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## <a id="DotNetBrowser_Input_DragAndDrop_Handlers_EnterDragParameters"></a> Class EnterDragParameters

Namespace: [DotNetBrowser.Input.DragAndDrop.Handlers](DotNetBrowser.Input.DragAndDrop.Handlers.md)  
Assembly: DotNetBrowser.dll  

The parameters of the <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop.EnterDragHandler" data-throw-if-not-resolved="false"></xref>.

```csharp
public sealed class EnterDragParameters : DragAndDropParameters
```

##### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DragAndDropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters) ← 
[EnterDragParameters](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_EnterDragParameters)

##### Inherited Members

[DragAndDropParameters.DragAndDrop](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters_DragAndDrop), 
[DragAndDropParameters.Event](DotNetBrowser.Input.DragAndDrop.Handlers.md#DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters_Event), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)
