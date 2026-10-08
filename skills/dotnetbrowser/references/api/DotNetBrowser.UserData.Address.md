# <a id="DotNetBrowser_UserData_Address"></a> Class Address

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

The user's address containing information about a street, city, state, etc.

```csharp
public sealed class Address
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Address](DotNetBrowser.UserData.Address.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_UserData_Address_City"></a> City

Gets the city from the address.

```csharp
public string City { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_CountryCode"></a> CountryCode

Gets the <a href="https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes">ISO 3166</a>
2-letter country code.

```csharp
public string CountryCode { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_DependentLocality"></a> DependentLocality

Gets the subdivision of a city, e.g. inner-city district or suburb.

```csharp
public string DependentLocality { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_State"></a> State

Gets the name of the state.

```csharp
public string State { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_Street"></a> Street

Gets the whole street name.

```csharp
public string Street { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_Zip"></a> Zip

Gets the ZIP code entered by the user.

```csharp
public string Zip { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_UserData_Address_Equals_System_Object_"></a> Equals\(object\)

```csharp
public override bool Equals(object obj)
```

#### Parameters

`obj` [object](https://learn.microsoft.com/dotnet/api/system.object)

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="DotNetBrowser_UserData_Address_GetHashCode"></a> GetHashCode\(\)

```csharp
public override int GetHashCode()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

