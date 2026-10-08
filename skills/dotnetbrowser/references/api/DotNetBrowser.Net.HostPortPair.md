# <a id="DotNetBrowser_Net_HostPortPair"></a> Class HostPortPair

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

A host/port pair of the URI.

```csharp
public sealed class HostPortPair
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[HostPortPair](DotNetBrowser.Net.HostPortPair.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_Net_HostPortPair_Host"></a> Host

Gets the host of the URI.

```csharp
public string Host { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Net_HostPortPair_Port"></a> Port

Gets the port of the URI.

```csharp
public int Port { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Methods

### <a id="DotNetBrowser_Net_HostPortPair_HasPort"></a> HasPort\(\)

Checks whether this host/port pair has a port.

```csharp
public bool HasPort()
```

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

true if the port of this host/port pair is greater than null.

### <a id="DotNetBrowser_Net_HostPortPair_Parse_System_String_"></a> Parse\(string\)

Converts a string representation of a host/port pair to the <xref href="DotNetBrowser.Net.HostPortPair" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static HostPortPair Parse(string hostPort)
```

#### Parameters

`hostPort` [string](https://learn.microsoft.com/dotnet/api/system.string)

The string representation of the host/port pair separated with the colon.

#### Returns

 [HostPortPair](DotNetBrowser.Net.HostPortPair.md)

the <xref href="DotNetBrowser.Net.HostPortPair" data-throw-if-not-resolved="false"></xref> instance.

### <a id="DotNetBrowser_Net_HostPortPair_ToString"></a> ToString\(\)

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

