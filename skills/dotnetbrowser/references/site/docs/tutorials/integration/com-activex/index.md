
# COM/ActiveX

DotNetBrowser does not support exposing its functionality as COM components or ActiveX controls out of the box. 

However, if you need to integrate DotNetBrowser with an application that is able to work only with OLE/COM/ActiveX, you can consider wrapping the functionality you need and then exposing these wrappers to that application. Both .NET Framework and the latest versions of .NET (starting from .NET Core 3.0) have support for interoperating with COM libraries. As a result, all the Chromium functionality provided by DotNetBrowser can be accessed in VB6, VBA, VBScript, etc.

Here is the general description of the idea:

1. Design and declare a set of COM interfaces that expose the functionality you need. These interfaces can be placed in a separate project. Use the `ComVisible` attribute to control the accessibility of the particular classes and interfaces.
2. In the implementations of these interfaces, initialize DotNetBrowser and perform all the actions you need.
3. If needed, customize the assembly registration by using `ComRegisterFunction` and `ComUnregisterFunction` attributes. This may appear to be necessary if you are planning to register an ActiveX control based on DotNetBrowser capabilities.
4. Build the assembly and register it using the assembly registration tool (`regasm.exe`).

After this, the corresponding entries will appear in the Windows registry, and the wrapper will become available for the COM clients.

The code of the example project that wraps DotNetBrowser functionality and exposes it to COM clients is available in the GitHub repository as Visual Studio projects: [C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/master/csharp/activex/ComWrapper), 
[VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/master/vbnet/activex/ComWrapper)

The following section goes through the implementation and explains the most important parts of the example.

## Implementation

### Declaring COM interfaces

There are a few ways to declare COM interfaces in .NET. For instance, you can consider using the `ClassInterface` attribute on a class to expose all its public methods, properties, fields, and events to COM clients. In the example, a different approach is used - the whole assembly is marked as `ComVisible`, and the interfaces are declared explicitly and made public. This approach can help to get a better control on what exactly is exposed to COM. The interface implementations are declared as internal classes. For example:

**Interface:**
```csharp
[Guid("D620EC2F-03E8-4C1A-9FF9-3A7B44590F54")]
[InterfaceType(ComInterfaceType.InterfaceIsIDispatch)]
public interface IComEngine
{
    [DispId(1)]
    void Initialize();

    [DispId(2)]
    void Dispose();

    [DispId(3)]
    IComBrowser CreateBrowser();
}
```
This example interface provides three methods - two of them can be used to control the lifetime of the wrapped `IEngine` instance, and the third one is used to create an `IBrowser` instance and return the corresponding COM wrapper to the client.

You can also consider applying the `ComVisible` attribute to the particular classes and interfaces instead of applying it to the whole assembly. In this case, only the classes and interfaces marked with this attribute will be available for COM clients. All other public types will not be exposed.

### Implementing COM interfaces

Here is an example implementation of the interface mentioned in the previous section:

**Implementation:**
```csharp
[Guid("DAE7A4AC-2D70-4830-81D8-3D7E5D8A7981")]
[ClassInterface(ClassInterfaceType.None)]
[ProgId("DotNetBrowser.ComWrapper.Engine")]
public class EngineWrapper : IComEngine
{
    private IEngine engine;
    private bool initialized;

    #region Methods

    public IComBrowser CreateBrowser() => new BrowserImpl(engine.CreateBrowser());

    public void Dispose()
    {
        if (initialized)
        {
            engine?.Dispose();
            engine = null;
            initialized = false;
        }
    }

    public void Initialize()
    {
        if (!initialized)
        {
            engine = EngineFactory.Create(new EngineOptions.Builder
            {
                RenderingMode = RenderingMode.OffScreen
            }.Build());
            initialized = true;
        }
    }

    #endregion
}
```
In this example, the implementation is public and has a ProgID specified - as a result, the corresponding coclass will be exposed to COM, and the ProgID will be used to reference it.

### Customizing assembly registration

The example project also provides the `ComBrowserView` class - a wrapper for the WinForms `BrowserView` that can be used as an independent ActiveX control. To make it recognizable as an ActiveX control, there is a need to add a few custom registry entries during the registration of the corresponding type. This can be done by defining two static methods in the `ComBrowserView` class and applying the `ComRegisterFunction` and `ComUnregisterFunction` attributes to them:

```csharp
public partial class ComBrowserView : UserControl, IComBrowserView
{
    // ...

    [EditorBrowsable(EditorBrowsableState.Never)]
    [ComRegisterFunction]
    private static void Register(Type t)
    {
        ControlRegistration.RegisterControl(t);
    }

    [EditorBrowsable(EditorBrowsableState.Never)]
    [ComUnregisterFunction]
    private static void Unregister(Type t)
    {
        ControlRegistration.UnregisterControl(t);
    }
}
```
The `ControlRegistration.RegisterControl` implementation adds a few subkeys to the corresponding `CLSID` registry key - the most significant of them is the `Control` key, which allows the custom control to show up in the ActiveX control container. The other subkeys define the control activation approach that should be used, the toolbox icon, the type library GUID, etc.

### Building the project and registering the assembly

To register the assembly during the build, the "Register for COM Interop" option is enabled in the example project.
This can appear to be useful for debugging the implementation.

As a result, the TLB is generated and registered automatically. Cleaning the project leads to unregistering all the components.

**Note**
Please check the bitness of the application you are trying to integrate with. If your application is 64-bit and the control is registered for 32-bit applications only (the registry entries are created under `HKEY_CLASSES_ROOT\WOW6432Node\` in this case), the control will be inaccessible for this application. The same can be observed if the application is 32-bit and the control is registered for 64-bit applications only.


## Summary

The described approach can appear to be useful for creating the solutions that provide the Chromium-based functionality to the applications which utilize COM objects or embed ActiveX controls.
