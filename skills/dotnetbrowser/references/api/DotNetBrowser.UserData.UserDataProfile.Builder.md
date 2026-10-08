# <a id="DotNetBrowser_UserData_UserDataProfile_Builder"></a> Class UserDataProfile.Builder

Namespace: [DotNetBrowser.UserData](DotNetBrowser.UserData.md)  
Assembly: DotNetBrowser.dll  

A builder for creating a new <xref href="DotNetBrowser.UserData.UserDataProfile" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public sealed class UserDataProfile.Builder
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UserDataProfile.Builder](DotNetBrowser.UserData.UserDataProfile.Builder.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_Address"></a> Address

Gets or sets the address entered by the user.

```csharp
public Address Address { get; set; }
```

#### Property Value

 [Address](DotNetBrowser.UserData.Address.md)

### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_CompanyName"></a> CompanyName

Gets or sets the name of the company entered by the user.

```csharp
public string CompanyName { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_Email"></a> Email

Gets or sets the email entered by the user.

```csharp
public string Email { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_FullName"></a> FullName

Gets or sets the full name entered by the user.

```csharp
public string FullName { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_PhoneNumber"></a> PhoneNumber

Gets or sets the phone number entered by the user.

```csharp
public string PhoneNumber { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_UserData_UserDataProfile_Builder_Build"></a> Build\(\)

Builds a new <xref href="DotNetBrowser.UserData.UserDataProfile" data-throw-if-not-resolved="false"></xref> instance with the properties set in the builder.

```csharp
public UserDataProfile Build()
```

#### Returns

 [UserDataProfile](DotNetBrowser.UserData.UserDataProfile.md)

A new <xref href="DotNetBrowser.UserData.UserDataProfile" data-throw-if-not-resolved="false"></xref> instance.

