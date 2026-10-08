# <a id="DotNetBrowser_UserData_Address_Builder"></a> Class Address.Builder

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

A builder for the <xref href="DotNetBrowser.UserData.Address" data-throw-if-not-resolved="false"></xref> class.

```csharp
public sealed class Address.Builder
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Address.Builder](DotNetBrowser.UserData.Address.Builder.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_UserData_Address_Builder_City"></a> City

Gets or sets the city from the address.

```csharp
public string City { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_Builder_CountryCode"></a> CountryCode

Gets or sets the <a href="https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes">ISO 3166</a>
country code.

```csharp
public string CountryCode { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_Builder_DependentLocality"></a> DependentLocality

Gets or sets the subdivision of a city, e.g. inner-city district or suburb.

```csharp
public string DependentLocality { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_Builder_State"></a> State

Gets or sets the name of the state.

```csharp
public string State { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_Builder_Street"></a> Street

Gets or sets the whole street name.

```csharp
public string Street { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_Address_Builder_Zip"></a> Zip

Gets or sets the ZIP code entered by the user.

```csharp
public string Zip { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_UserData_Address_Builder_Build"></a> Build\(\)

Builds a new <xref href="DotNetBrowser.UserData.Address" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public Address Build()
```

#### Returns

 [Address](DotNetBrowser.UserData.Address.md)

A new <xref href="DotNetBrowser.UserData.Address" data-throw-if-not-resolved="false"></xref> instance.

