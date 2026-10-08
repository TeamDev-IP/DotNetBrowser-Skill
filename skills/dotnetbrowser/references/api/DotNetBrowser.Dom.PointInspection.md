# <a id="DotNetBrowser_Dom_PointInspection"></a> Class PointInspection

Namespace: [DotNetBrowser.Dom](DotNetBrowser.Dom.md)  
Assembly: DotNetBrowser.dll  

Provides information about a DOM node at the specified point inside the loaded document.

```csharp
public sealed class PointInspection
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PointInspection](DotNetBrowser.Dom.PointInspection.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Dom_PointInspection_AbsoluteImageUrl"></a> AbsoluteImageUrl

Gets the absolute URL of the image located at the point.

```csharp
public string AbsoluteImageUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Dom_PointInspection_AbsoluteLinkUrl"></a> AbsoluteLinkUrl

Gets the absolute URL of the link DOM element at the specified point.
Returns an empty string if there is no link at the point.

```csharp
public string AbsoluteLinkUrl { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Dom_PointInspection_LocalPoint"></a> LocalPoint

Gets the coordinates of the point relative to the node.

```csharp
public Point LocalPoint { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

### <a id="DotNetBrowser_Dom_PointInspection_Node"></a> Node

Gets the node at the specified point.

```csharp
public INode Node { get; }
```

#### Property Value

 [INode](DotNetBrowser.Dom.INode.md)

### <a id="DotNetBrowser_Dom_PointInspection_UrlNode"></a> UrlNode

Gets the link node when a link is located at the point.

```csharp
public INode UrlNode { get; }
```

#### Property Value

 [INode](DotNetBrowser.Dom.INode.md)

