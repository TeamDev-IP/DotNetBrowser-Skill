
# Installing License

**Lead**
This article describes how to configure DotNetBrowser license.
 

You can obtain an evaluation license and start using your 30-day trial by filling in [web form](https://teamdev.com/dotnetbrowser#evaluate).

If the license is missing, not valid or not installed properly, the following error message is shown:


**Note**
Unable to find a valid DotNetBrowser License. Please make sure you have set up your license correctly. To do so, follow the instructions here:
https://links.teamdev.com/dotnetbrowser-installing-license



To solve it add a proper license key to your project using one of the following ways:

* Set the license key through the API. 
* Create the `dotnetbrowser.license` file with your license key and add it as **Embedded Resource**.
* Put the `dotnetbrowser.license` file with your license key in the application directory of your .NET application.

## Installing key through the API

To install your license key use the following API:


**C#**
```csharp
IEngine engine = EngineFactory.Create(new EngineOptions.Builder
{
    LicenseKey = "your_license_key"
}.Build());
```

**VB**
```vb
Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
{
    .LicenseKey = "your_license_key"
}.Build())
```



**Note**
This approach overrides the license key [added as **Embedded Resource**](https://teamdev.com/dotnetbrowser/docs/guides/installation/license/#embedded-resource) or [copied to the application directory](https://teamdev.com/dotnetbrowser/docs/guides/installation/license/#application-directory).


## Installing key through a license file

The license file (`dotnetbrowser.license`) is a simple text file containing the license key. If you have a license key only and need to have the `dotnetbrowser.license` file, you can create this file in a text editor, such as Notepad or Notepad++, and insert your license key into this file:

![Notepad++](https://teamdev.com/dotnetbrowser/img/articles/installation/licensing/notepad.webp)

### Embedded Resource

In **Solution Explorer**, right-click your project, select **Add > Existing Item...** and add `dotnetbrowser.license` file:

![Add Item](https://teamdev.com/dotnetbrowser/img/articles/installation/licensing/add-item.webp)

In **Solution Explorer**, right-click `dotnetbrowser.license` and select **Properties**. In the **Properties** panel which opens, select **Embedded Resource** as **Build Action**:

![Properties](https://teamdev.com/dotnetbrowser/img/articles/installation/licensing/properties.webp)

### Application directory
You can copy the `dotnetbrowser.license` file to the application directory of your .NET application. The process of adding the file is similar to the first approach described above. However, you need to specify the **Build Action** setting as **None** and **Copy to Output Directory** as **Copy Always** in the **Properties** section:

![Copy to Output Directory](https://teamdev.com/dotnetbrowser/img/articles/installation/licensing/working-directory.webp)

DotNetBrowser looks for the file in `AppContext.BaseDirectory`, the directory
that contains the application assemblies. This is not necessarily the current
working directory of the process: an application started from another folder,
for example by a shortcut or a service manager, still finds the file.

## Adding a license file to the demo application
To launch DotNetBrowser demo application, add the `dotnetbrowser.license` file to the directory with `DotNetBrowser.Wpf.Demo.exe` and `DotNetBrowser.WinForms.Demo.exe` executables. To do so:

1. Download DotNetBrowser distribution archive.
2. Extract the archive into, for example, `C:\Downloads\DotNetBrowser-x.x\` directory. 
3. [Create the `dotnetbrowser.license` file](https://teamdev.com/dotnetbrowser/docs/guides/installation/license/#installing-key-through-a-license-file) in a text editor, such as Notepad or Notepad++. Insert your license key into this file.
4. Navigate to the `Library` subfolder and copy/move the license file there:

![DotNetBrowser Demo](https://teamdev.com/dotnetbrowser/img/articles/installation/licensing/demo-license.webp)
