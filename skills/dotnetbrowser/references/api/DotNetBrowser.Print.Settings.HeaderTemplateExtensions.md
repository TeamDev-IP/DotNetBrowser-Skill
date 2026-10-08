# <a id="DotNetBrowser_Print_Settings_HeaderTemplateExtensions"></a> Class HeaderTemplateExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IHeaderTemplate%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class HeaderTemplateExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[HeaderTemplateExtensions](DotNetBrowser.Print.Settings.HeaderTemplateExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_HeaderTemplateExtensions_SetHeaderTemplate__1_DotNetBrowser_Print_Settings_IHeaderTemplate___0__System_String_"></a> SetHeaderTemplate<TPrintSettings\>\(IHeaderTemplate<TPrintSettings\>, string\)

Sets the HTML to be displayed in the header.

```csharp
public static TPrintSettings SetHeaderTemplate<TPrintSettings>(this IHeaderTemplate<TPrintSettings> obj, string headerTemplate) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IHeaderTemplate](DotNetBrowser.Print.Settings.IHeaderTemplate\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IHeaderTemplate%601" data-throw-if-not-resolved="false"></xref> implementation.

`headerTemplate` [string](https://learn.microsoft.com/dotnet/api/system.string)

The HTML to be displayed in the header. Cannot be null.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The specified header template is null.

