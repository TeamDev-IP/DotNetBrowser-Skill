# <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters"></a> Class DragAndDropParameters

Namespace: [DotNetBrowser.Input.DragAndDrop.Handlers](DotNetBrowser.Input.DragAndDrop.Handlers.md)  
Assembly: DotNetBrowser.dll  

The base class for all <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> handlers parameters.

```csharp
public class DragAndDropParameters
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DragAndDropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.DragAndDropParameters.md)

#### Derived

[DropParameters](DotNetBrowser.Input.DragAndDrop.Handlers.DropParameters.md), 
[EnterDragParameters](DotNetBrowser.Input.DragAndDrop.Handlers.EnterDragParameters.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters_DragAndDrop"></a> DragAndDrop

Gets the <xref href="DotNetBrowser.Input.DragAndDrop.IDragAndDrop" data-throw-if-not-resolved="false"></xref> instance the handler is associated with.

```csharp
public IDragAndDrop DragAndDrop { get; }
```

#### Property Value

 [IDragAndDrop](DotNetBrowser.Input.DragAndDrop.IDragAndDrop.md)

### <a id="DotNetBrowser_Input_DragAndDrop_Handlers_DragAndDropParameters_Event"></a> Event

Gets the drag and drop event.

```csharp
public DragEvent Event { get; }
```

#### Property Value

 [DragEvent](DotNetBrowser.Input.DragAndDrop.Handlers.DragEvent.md)

