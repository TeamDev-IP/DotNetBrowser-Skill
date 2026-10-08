# <a id="DotNetBrowser_Net_MultipartFormData"></a> Class MultipartFormData

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The list of key-value pairs each representing a segment of a multi-part form data.
Can be empty if the form doesn't contain any data.

```csharp
public sealed class MultipartFormData : UploadData, IUploadData<IReadOnlyCollection<MultipartFormDataKeyValuePair>>, IUploadData
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UploadData](DotNetBrowser.Net.UploadData.md) ← 
[MultipartFormData](DotNetBrowser.Net.MultipartFormData.md)

#### Implements

[IUploadData<IReadOnlyCollection<MultipartFormDataKeyValuePair\>\>](DotNetBrowser.Net.IUploadData\-1.md), 
[IUploadData](DotNetBrowser.Net.IUploadData.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Net_MultipartFormData__ctor_System_Collections_Generic_IReadOnlyCollection_DotNetBrowser_Net_MultipartFormDataKeyValuePair__"></a> MultipartFormData\(IReadOnlyCollection<MultipartFormDataKeyValuePair\>\)

Creates a new instance containing the specified key-value pairs.

```csharp
public MultipartFormData(IReadOnlyCollection<MultipartFormDataKeyValuePair> data)
```

#### Parameters

`data` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[MultipartFormDataKeyValuePair](DotNetBrowser.Net.MultipartFormDataKeyValuePair.md)\>

The key-value pairs that represent segments of the multi-part form data.

## Properties

### <a id="DotNetBrowser_Net_MultipartFormData_Data"></a> Data

The key-value pairs that represent segments of the multi-part form data.

```csharp
public IReadOnlyCollection<MultipartFormDataKeyValuePair> Data { get; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[MultipartFormDataKeyValuePair](DotNetBrowser.Net.MultipartFormDataKeyValuePair.md)\>

