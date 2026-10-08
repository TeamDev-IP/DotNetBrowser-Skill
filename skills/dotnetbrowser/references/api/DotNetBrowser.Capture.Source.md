# <a id="DotNetBrowser_Capture_Source"></a> Class Source

Namespace: [DotNetBrowser.Capture](DotNetBrowser.Capture.md)  
Assembly: DotNetBrowser.dll  

The source for the content capture session.

```csharp
public sealed class Source
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Source](DotNetBrowser.Capture.Source.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Capture_Source_Name"></a> Name

Gets the name of the capture source.

```csharp
public string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Capture_Source_Thumbnail"></a> Thumbnail

Gets the <xref href="DotNetBrowser.Ui.Bitmap" data-throw-if-not-resolved="false"></xref> instance that contains the image of the capture source.

```csharp
public Bitmap Thumbnail { get; }
```

#### Property Value

 [Bitmap](DotNetBrowser.Ui.Bitmap.md)

### <a id="DotNetBrowser_Capture_Source_Type"></a> Type

Gets the type of this capture source.

```csharp
public SourceType Type { get; }
```

#### Property Value

 [SourceType](DotNetBrowser.Capture.SourceType.md)

