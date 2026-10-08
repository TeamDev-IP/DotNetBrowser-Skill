
# VSTO

**Lead**
This tutorial shows how to create a VSTO add-in and embed DotNetBrowser into Microsoft Outlook.


DotNetBrowser provides a WinForms `BrowserView` control that can be used with VSTO add-ins to add the Chromium-based browser as an integral part of a Microsoft Office application. In this tutorial, we will show how to embed a `BrowserView` control into the Microsoft Outlook inspector.

## Implementation
### Adding DotNetBrowser to Add-in project

In Visual Studio, create a sample add-in project for Microsoft Outlook. You can find the corresponding project template in the __"VSTO Add-ins"__ section:

![Create Add-in Project](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-1.webp)

Add all the necessary references to our project. To do so, in the __Solution Explorer__, right-click the __References__ node and select __Add Reference...__:

![Add Reference](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-2.webp)

Select all the required DotNetBrowser assemblies and click __Add__: 

![Select Referenced Assemblies](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-3.webp)

**Note**
 Make sure that the DotNetBrowser license is also configured as described in this [article](https://teamdev.com/dotnetbrowser/docs/guides/installation/license/).


To make the add-in debugging more convenient, configure DotNetBrowser logging during add-in initialization and specify the location to store the log file as shown below: 

![Configure Logging](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-5-logging.webp)

### Creating form region

Add a form region which is used to replace or customize the standard Outlook forms. To do so, right-click the project node in the __Solution Explorer__ and select __Add New Item__:

![Add Form Region](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-6.webp)

Specify how the Outlook form region is created. To do so, select the __Design a new form region__ option and click __Next__.

![Design New Form Region](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-7.webp)

Select the form region type. In this tutorial, we create this form region as a _separate_ page on the form.

![Select Form Region Type](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-8.webp)

Type the form region name and select the inspector types where this form region appears and click __Next__.

![Specify Form Region Name](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-9.webp)

Select the message classes to specify the Outlook item types for which the form region should be available and click __Finish__. For example, selecting `IPM.Note` makes the form region available for the email messages.

![Select Message Classes](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-10.webp)

### Adding BrowserView control to the Toolbox

After the form region is created, the form region designer opens. To make it more convenient, add the `BrowserView` control to the Visual Studio __Toolbox__. There are a few ways to do this, and the most straightforward of them is to add it from the assembly manually. To do so, right-click the __Toolbox__ and select __Choose Items...__:

![Choose Toolbox Items](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-11-toolbox.webp)

The __Choose Toolbox Items__ dialog appears. Click the __Browse__ button to add the `BrowserView` control to the list:

![Browse Toolbox Items](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-12-toolbox.webp)

In the file chooser, select the `DotNetBrowser.WinForms` assembly that contains the `BrowserView` control:

![Select Toolbox Item Assembly](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-13-toolbox.webp)

Make sure that the `BrowserView` control is now listed and selected, and click __OK__.

![Select Framework Component](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-14-toolbox.webp)

The `BrowserView` control appears in the Visual Studio __Toolbox__:

![BrowserView In Toolbox](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-15-toolbox.webp)

### Adding BrowserView to the form region

Add the `BrowserView` control to the form region from the __Toolbox__ and adjust its layout. For example, you can specify its `Dock` property as `Fill` to fill the whole form region with the control:

![Designer With BrowserView](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-16.webp)

Create an `IBrowser` instance and initialize `BrowserView` before the region is displayed.

![BrowserView Initialization](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-17.webp)

### Building and running the project

Build and run the project to launch Microsoft Outlook with the sample add-in configured. In the Outlook window, click the __New Email__ button.

![New Email](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-18.webp)

Microsoft Outlook form appears. In the form ribbon, you can notice the __BrowserFormRegion__ button.

![BrowserView In Toolbox](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-19.webp)

Click the __BrowserFormRegion__ button, to display the sample form region with the embedded `BrowserView`.

![BrowserView In Toolbox](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/vsto/addin-20.webp)
