# <a id="DotNetBrowser_Net_TextData"></a> Class TextData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The upload data of the <code>text/plain</code> content type.

```csharp
public sealed class TextData : UploadData, IUploadData<string>, IUploadData
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UploadData](DotNetBrowser.Net.UploadData.md) ← 
[TextData](DotNetBrowser.Net.TextData.md)

#### Implements

[IUploadData<string\>](DotNetBrowser.Net.IUploadData\-1.md), 
[IUploadData](DotNetBrowser.Net.IUploadData.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_TextData__ctor_System_String_"></a> TextData\(string\)

Creates a new instance containing the specified data.

```csharp
public TextData(string data)
```

#### Parameters

`data` [string](https://learn.microsoft.com/dotnet/api/system.string)

The upload data as a <code>string</code>.

## Properties

### <a id="DotNetBrowser_Net_TextData_Data"></a> Data

The upload data as a <code>string</code>.

```csharp
public string Data { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Operators

### <a id="DotNetBrowser_Net_TextData_op_Implicit_System_String__DotNetBrowser_Net_TextData"></a> implicit operator TextData\(string\)

Converts the specified data to a new instance of <xref href="DotNetBrowser.Net.BytesData" data-throw-if-not-resolved="false"></xref>.

```csharp
public static implicit operator TextData(string data)
```

#### Parameters

`data` [string](https://learn.microsoft.com/dotnet/api/system.string)

The upload data as a byte array.

#### Returns

 [TextData](DotNetBrowser.Net.TextData.md)

The new <xref href="DotNetBrowser.Net.TextData" data-throw-if-not-resolved="false"></xref>instance.

