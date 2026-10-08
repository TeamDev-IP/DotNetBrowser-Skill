# <a id="DotNetBrowser_Net_BytesData"></a> Class BytesData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The upload data as bytes.
Can be empty if the form doesn't contain any data.

```csharp
public sealed class BytesData : UploadData, IUploadData<IReadOnlyList<byte>>, IUploadData
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UploadData](DotNetBrowser.Net.UploadData.md) ← 
[BytesData](DotNetBrowser.Net.BytesData.md)

#### Implements

[IUploadData<IReadOnlyList<byte\>\>](DotNetBrowser.Net.IUploadData\-1.md), 
[IUploadData](DotNetBrowser.Net.IUploadData.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_BytesData__ctor_System_Byte___"></a> BytesData\(byte\[\]\)

Creates a new instance containing the specified data.

```csharp
public BytesData(byte[] data)
```

#### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The upload data as a byte array.

## Properties

### <a id="DotNetBrowser_Net_BytesData_Data"></a> Data

The upload data as a read-only list.

```csharp
public IReadOnlyList<byte> Data { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[byte](https://learn.microsoft.com/dotnet/api/system.byte)\>

## Operators

### <a id="DotNetBrowser_Net_BytesData_op_Implicit_System_Byte____DotNetBrowser_Net_BytesData"></a> implicit operator BytesData\(byte\[\]\)

Converts the specified data to a new instance of <xref href="DotNetBrowser.Net.BytesData" data-throw-if-not-resolved="false"></xref>.

```csharp
public static implicit operator BytesData(byte[] data)
```

#### Parameters

`data` [byte](https://learn.microsoft.com/dotnet/api/system.byte)\[\]

The upload data as a byte array.

#### Returns

 [BytesData](DotNetBrowser.Net.BytesData.md)

The new <xref href="DotNetBrowser.Net.BytesData" data-throw-if-not-resolved="false"></xref> instance.

