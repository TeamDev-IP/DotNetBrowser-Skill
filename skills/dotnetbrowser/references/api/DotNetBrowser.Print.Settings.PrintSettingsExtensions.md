# <a id="DotNetBrowser_Print_Settings_PrintSettingsExtensions"></a> Class PrintSettingsExtensions

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Extension methods for <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> interface.

```csharp
public static class PrintSettingsExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PrintSettingsExtensions](DotNetBrowser.Print.Settings.PrintSettingsExtensions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Print_Settings_PrintSettingsExtensions_Apply__1___0_System_Action___0__"></a> Apply<TPrintSettings\>\(TPrintSettings, Action<TPrintSettings\>\)

Performs the action with the print settings and then applies the changes.

```csharp
public static void Apply<TPrintSettings>(this TPrintSettings printSettings, Action<TPrintSettings> action) where TPrintSettings : class, IPrintSettings
```

#### Parameters

`printSettings` TPrintSettings

The print settings to work with. Cannot be null.

`action` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<TPrintSettings\>

The action to perform with these print settings. Cannot be null.

#### Type Parameters

`TPrintSettings` 

The type of print settings that can be applied.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

The print settings were not applied properly.

