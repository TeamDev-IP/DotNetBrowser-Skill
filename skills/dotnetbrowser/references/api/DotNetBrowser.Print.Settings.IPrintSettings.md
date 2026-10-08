# <a id="DotNetBrowser_Print_Settings_IPrintSettings"></a> Interface IPrintSettings

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

The common interface for the concrete print job settings to implement.

```csharp
public interface IPrintSettings
```

#### Extension Methods

[PrintSettingsExtensions.Apply<IPrintSettings\>\(IPrintSettings, Action<IPrintSettings\>\)](DotNetBrowser.Print.Settings.PrintSettingsExtensions.md\#DotNetBrowser\_Print\_Settings\_PrintSettingsExtensions\_Apply\_\_1\_\_\_0\_System\_Action\_\_\_0\_\_)

## Methods

### <a id="DotNetBrowser_Print_Settings_IPrintSettings_Apply"></a> Apply\(\)

Applies the configured print settings. You should call this method to regenerate the internal
print preview using the configured settings and update the total page count to be printed.

```csharp
void Apply()
```

#### Remarks

This method is invoked automatically when you choose to proceed in the <xref href="DotNetBrowser.Browser.IBrowser.PrintHtmlContentHandler" data-throw-if-not-resolved="false"></xref>
or <xref href="DotNetBrowser.Browser.IBrowser.PrintPdfContentHandler" data-throw-if-not-resolved="false"></xref>. If the settings cannot be applied at this point, the printing operation
is canceled.

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Print.IPrintJob%601" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

The print settings were not applied properly.

