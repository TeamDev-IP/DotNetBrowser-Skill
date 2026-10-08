
# How to deploy Chromium binaries over network

**Note**
This tutorial describes a custom approach that the application implements
itself. It is not a built-in DotNetBrowser feature. For the comparison with the
built-in ways of supplying the Chromium runtime, see
[Deployment](https://teamdev.com/dotnetbrowser/docs/guides/gs/deployment/#distribution-modes).


In some cases, it is required to make the installer or the deployment package as small as possible - for instance, there can be a restriction of the service where the application is published.

On the other hand, DotNetBrowser works with its own Chromium engine, and the binaries must be deployed in the target environment. The most straightforward approach is to supply the binaries as a part of the installer, however, this will lead to the increased size of the installer itself.

One of the possible solutions is to provide the Chromium binaries over the network as soon as DotNetBrowser tries to locate them. DotNetBrowser uses the default .NET assembly loading logic to locate and load the binaries DLL, so it is possible to use the [AppDomain.AssemblyResolve](https://learn.microsoft.com/en-us/dotnet/api/system.appdomain.assemblyresolve) event to customize the overall process and provide the DLL in a non-standard way.

Here is the general description of the idea:

1. Register a custom handler of the AppDomain.AssemblyResolve event.
2. In this handler, filter out the attempts related to the DotNetBrowser binaries.
3. When the corresponding AssemblyResolve event is received, use the fully-qualified assembly name to prepare a network request.
4. Perform the request and obtain the DLL as array of bytes.
5. Load DLL from bytes and return it from the handler.

The code of the example application that performs the described actions to load the binaries DLL is available in the GitHub repository as Visual Studio projects: [C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/csharp/wpf/ChromiumBinariesResolver), 
[VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/vbnet/wpf/ChromiumBinariesResolver)

The example itself is a WPF application, but the approach is not WPF-specific and can be used in WinForms and console applications as well.

The following section goes through the implementation and explains the most important parts of the example.

## Implementation

### BinariesResolverBase class

The `BinariesResolverBase` abstract class provides a general implementation of the binaries resolver. The constructor of the class initializes the `RequestUri` property, which can later be used for preparing requests, creates a `HttpClient` instance for making these requests and subscribes to the `AssemblyResolve` event of the application domain.

```csharp
protected BinariesResolverBase(string requestUri, AppDomain domain = null)
{
    if (domain == null)
    {
        domain = AppDomain.CurrentDomain;
    }

    RequestUri = requestUri;
    client = new HttpClient();
    domain.AssemblyResolve += Resolve;
}
```

The `Resolve(object sender, ResolveEventArgs args)` method handles the `AssemblyResolve` events and filters out the requests for the assemblies with names starting with "DotNetBrowser.Chromium". For these assemblies, it calls a private `Resolve` method overload for the further processing.

```csharp
public Assembly Resolve(object sender, ResolveEventArgs args)
    => args.Name.StartsWith("DotNetBrowser.Chromium") ? Resolve(args.Name).GetAwaiter().GetResult() : null;
```

The `Resolve(string binariesAssemblyName)` method overload creates an `AssemblyName` instance and passes it to the abstract `PrepareRequest(AssemblyName assemblyName)` method to prepare the URL request string. After that, the URL request string is used to perform the actual request via the `HttpClient`. The response stream is expected to contain the bytes of the Chromium binaries assembly. These bytes are then passed to the abstract `ProcessResponse(Stream responseBody, AssemblyName assemblyName)` method which returns the assembly itself.

```csharp
private async Task<Assembly> Resolve(string binariesAssemblyName)
{
    //Note: assemblies are usually resolved in the background thread of the UI application.
    try
    {
        //Construct a request using the fully-qualified assembly name.
        AssemblyName assemblyName = new AssemblyName(binariesAssemblyName);
        string request = PrepareRequest(assemblyName);

        //Perform the request and download the response.
        OnStatusUpdated("Downloading Chromium binaries...");
        Debug.WriteLine($"Downloading {request}");
        HttpResponseMessage response = await client.GetAsync(request);

        response.EnsureSuccessStatusCode();
        OnStatusUpdated("Chromium binaries package downloaded");
        Stream responseBody = await response.Content.ReadAsStreamAsync();

        //Process the response bytes and load the assembly.
        return ProcessResponse(responseBody, assemblyName);
    }
    catch (Exception e)
    {
        Debug.WriteLine("Exception caught: {0} ", e);
    }

    return null;
}
```
The `OnStatusUpdated` method raises the `StatusUpdated` event with a particular message, which can then be used to be informed about the progress in the other parts of the application.

The `BinariesResolverBase` abstract implementation is then extended by the `BinariesResolver` class that provides the implementations of `PrepareRequest` and `ProcessResponse` methods.

### BinariesResolver class

The `BinariesResolver` resolves the Chromium binaries assembly by downloading the DotNetBrowser distribution archive and extracting the required assembly from it on the fly. This class is derived from `BinariesResolverBase` and provides the implementations of its abstract members.

Here is the `PrepareRequest` implementation:

```csharp
protected override string PrepareRequest(AssemblyName assemblyName)
{
    //Use only the major and minor version components if the build component is 0.
    int fieldCount = assemblyName.Version.Build == 0 ? 2 : 3;
    return string.Format(RequestUri, assemblyName.Version.ToString(fieldCount));
}

```

This implementation reuses the `RequestUri` property to prepare the direct reference to the distribution archive depending on the DotNetBrowser version. The `RequestUri` in this case is set to `UriTemplate` which looks as shown below:

```csharp
private const string UriTemplate =
    "https://teamdev.download/downloads/"
    +"dotnetbrowser/{0}/dotnetbrowser-net45-{0}.zip";
```

After the distribution archive is received as a stream, the `ProcessResponse` method is called. The implementation of this method extracts the DLL from it on the fly and loads it directly into the current application domain. The loaded assembly is then used as a return value.

```csharp
protected override Assembly ProcessResponse(Stream responseBody, AssemblyName assemblyName)
{
    // The downloaded bytes represent a ZIP archive. Locate the DLL we need in this archive.
    ZipArchive archive = new ZipArchive(responseBody);
    ZipArchiveEntry binariesDllEntry 
        = archive.Entries
                .FirstOrDefault(entry => entry.FullName.EndsWith(".dll")
                                        && entry.FullName.Contains(assemblyName.Name));
    if (binariesDllEntry == null)
    {
        return null;
    }

    // Unzip the found entry and load the DLL.
    OnStatusUpdated("Unzipping Chromium binaries");
    Stream unzippedEntryStream;
    using (unzippedEntryStream = binariesDllEntry.Open())
    {
        using (MemoryStream memoryStream = new MemoryStream())
        {
            unzippedEntryStream.CopyTo(memoryStream);
            OnStatusUpdated("Loading Chromium binaries assembly");
            Assembly assembly = Assembly.Load(memoryStream.ToArray());
            OnStatusUpdated("Chromium binaries assembly loaded.", true);
            return assembly;
        }
    }
}
```
After loading the DLL into the application domain, DotNetBrowser unpacks the binaries from this DLL to the directory configured via the `EngineOptions.Builder.ChromiumDirectory` and then launches the Chromium process as usual.

**Note**
The DotNetBrowser distribution archive here is used only as an example. If you are planning to implement the similar approach in your application, you should consider implementing your own service that provides the required DLL to avoid the excessive memory usage and decrease the initialization time.


## Advantages

The main advantage of the suggested approach is minimizing the size of the distributed application package - there is no need to supply the DotNetBrowser.Chromium DLLs as a part of the installer or the distribution package.

## Disadvantages

1. Increased initialization time. When the Chromium binaries are supplied over network, the initialization will include downloading the binaries DLL, and this usually takes some time even with the good connection. If the connection is poor, a few retries may appear to be required, and the initialization time will grow significantly.
2. The Internet connection is required. If there is no Internet connection at all, it is not possible to download the binaries and initialize the DotNetBrowser engine. 
3. Memory usage is increased. If the DotNetBrowser.Chromium DLLs are loaded from the array of bytes, DotNetBrowser unpacks the binaries in-memory, and the memory usage will increase during the initialization. This can even lead to out of memory issues in 32-bit environments if the memory usage is already high enough.


## Summary

The described approach can appear to be useful for the particular types of solutions, however, it is necessary to consider its pros and cons thoroughly before making a final decision.
