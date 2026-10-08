# <a id="DotNetBrowser_Print_Settings_FooterTemplateExtensions"></a> Class FooterTemplateExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IFooterTemplate%601" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class FooterTemplateExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[FooterTemplateExtensions](DotNetBrowser.Print.Settings.FooterTemplateExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_FooterTemplateExtensions_SetFooterTemplate__1_DotNetBrowser_Print_Settings_IFooterTemplate___0__System_String_"></a> SetFooterTemplate<TPrintSettings\>\(IFooterTemplate<TPrintSettings\>, string\)

Sets the HTML to be displayed in the footer.

```csharp
public static TPrintSettings SetFooterTemplate<TPrintSettings>(this IFooterTemplate<TPrintSettings> obj, string footerTemplate) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`obj` [IFooterTemplate](DotNetBrowser.Print.Settings.IFooterTemplate\-1.md)<TPrintSettings\>

The <xref href="DotNetBrowser.Print.Settings.IFooterTemplate%601" data-throw-if-not-resolved="false"></xref> implementation.

`footerTemplate` [string](https://learn.microsoft.com/dotnet/api/system.string)

The HTML to be displayed in the footer. Cannot be null.

#### Returns

 TPrintSettings

The current print settings instance.

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The specified header template is null.

