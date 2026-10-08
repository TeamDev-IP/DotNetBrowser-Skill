# <a id="DotNetBrowser_Browser_Events_CursorChangedEventArgs"></a> Class CursorChangedEventArgs

Namespace: [DotNetBrowser.Browser.Events](DotNetBrowser.Browser.Events.md)  
Assembly: DotNetBrowser.dll  

The <xref href="DotNetBrowser.Browser.IOffScreenRenderProvider.CursorChanged" data-throw-if-not-resolved="false"></xref> event data which can be used to update the cursor for the off-screen
view.

```csharp
public sealed class CursorChangedEventArgs : EventArgs
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs) ← 
[CursorChangedEventArgs](DotNetBrowser.Browser.Events.CursorChangedEventArgs.md)

#### Inherited Members

[EventArgs.Empty](https://learn.microsoft.com/dotnet/api/system.eventargs.empty), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Browser_Events_CursorChangedEventArgs_Bitmap"></a> Bitmap

The cursor image. Available for custom cursors only.

```csharp
public Bitmap Bitmap { get; }
```

#### Property Value

 [Bitmap](DotNetBrowser.Ui.Bitmap.md)

### <a id="DotNetBrowser_Browser_Events_CursorChangedEventArgs_CursorType"></a> CursorType

The cursor type. If set to <xref href="DotNetBrowser.Ui.Cursors.CursorType.Custom" data-throw-if-not-resolved="false"></xref>, the cursor image and hotspot are provided in the
corresponding fields.

```csharp
public CursorType CursorType { get; }
```

#### Property Value

 [CursorType](DotNetBrowser.Ui.Cursors.CursorType.md)

### <a id="DotNetBrowser_Browser_Events_CursorChangedEventArgs_Hotspot"></a> Hotspot

The cursor hotspot. Available for custom cursors only.

```csharp
public Point Hotspot { get; }
```

#### Property Value

 [Point](DotNetBrowser.Geometry.Point.md)

