# <a id="DotNetBrowser_Engine_IEngine"></a> Interface IEngine

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Provides access to the Chromium engine functionality.

```csharp
public interface IEngine : IDisposable, IAutoDisposable<EngineDisposedEventArgs>, IAutoDisposable
```

#### Implements

[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAutoDisposable<EngineDisposedEventArgs\>](DotNetBrowser.IAutoDisposable\-1.md), 
[IAutoDisposable](DotNetBrowser.IAutoDisposable.md)

## Remarks

<p>
    To perform operations with the engine, a license key is required. The license key represents
    a string that can be set via the <code>dotnetbrowser.license</code> file or individually for every
    <code>IEngine</code> using the <xref href="DotNetBrowser.Engine.EngineOptions.LicenseKey?text=LicenseKey" data-throw-if-not-resolved="false"></xref> property. If you
    set the license key via configuring the license file, then please make sure that you set it
    before creating an <code>IEngine</code> instance.
</p>
<p>
    The Chromium engine is running in a separate native process. Communication between the native
    and .NET process is done through the Inter-Process Communication (IPC) layer that allows
    transferring data between two processes on a local machine.
</p>
<p>
    The native process allocates memory and system resources that must be released. So, when the
    engine is no longer needed, it must be disposed through the <xref href="System.IDisposable.Dispose" data-throw-if-not-resolved="false"></xref> method to
    shutdown the native process and free all the allocated memory and system resources. For example:
</p>

<pre><code class="lang-csharp">IEngine engine = EngineFactory.Create(engineOptions);
//...
engine.Dispose();</code></pre>

<p>
    Any attempt to use an already disposed engine or any of its services will lead to the
    <xref href="System.ObjectDisposedException" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    To get notifications that the <code>IEngine</code> instance has been disposed subscribe to the
    following event:
</p>

<pre><code class="lang-csharp">engine.Disposed += (s, e) =&gt; {
// The engine has been disposed or unexpectedly crashed.
};</code></pre>

<p>To get notifications that the <code>IEngine</code> instance has been unexpectedly crashed use:</p>

<pre><code class="lang-csharp">engine.Disposed += (s, e) =&gt; {
    long exitCode = e.ExitCode;
    // The engine has been crashed if this exit code is non-zero.
};</code></pre>

<example>

    <pre><code class="lang-cs">string dataDir = Path.Combine(Path.GetTempPath(), Guid.NewGuid().ToString());
Directory.CreateDirectory(dataDir);

EngineOptions engineOptions = new EngineOptions.Builder
    {
        UserDataDirectory = dataDir
    }
   .Build();
IEngine engine = EngineFactory.Create(engineOptions);</code></pre>

</example>

## Properties

### <a id="DotNetBrowser_Engine_IEngine_MediaDevices"></a> MediaDevices

Gets the service that allows managing media stream devices.

```csharp
IMediaDevices MediaDevices { get; }
```

#### Property Value

 [IMediaDevices](DotNetBrowser.Media.IMediaDevices.md)

### <a id="DotNetBrowser_Engine_IEngine_Options"></a> Options

Gets the options that were used to initialize this <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref>.

```csharp
EngineOptions Options { get; }
```

#### Property Value

 [EngineOptions](DotNetBrowser.Engine.EngineOptions.md)

### <a id="DotNetBrowser_Engine_IEngine_Profiles"></a> Profiles

Gets the live collection of the Chromium profiles available in this engine.

```csharp
IProfiles Profiles { get; }
```

#### Property Value

 [IProfiles](DotNetBrowser.Profile.IProfiles.md)

### <a id="DotNetBrowser_Engine_IEngine_Theme"></a> Theme

Gets or sets the current Chromium theme.

```csharp
Theme Theme { get; set; }
```

#### Property Value

 [Theme](DotNetBrowser.Engine.Theme.md)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

### <a id="DotNetBrowser_Engine_IEngine_Widevine"></a> Widevine

Gets the service that allows activating the Widevine component for DRM content playback.

```csharp
IWidevine Widevine { get; }
```

#### Property Value

 [IWidevine](DotNetBrowser.Engine.IWidevine.md)

## Methods

### <a id="DotNetBrowser_Engine_IEngine_CreateBrowser"></a> CreateBrowser\(\)

Creates a new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance with the initial "about:blank" web page.

```csharp
IBrowser CreateBrowser()
```

#### Returns

 [IBrowser](DotNetBrowser.Browser.IBrowser.md)

The new <xref href="DotNetBrowser.Browser.IBrowser" data-throw-if-not-resolved="false"></xref> instance.

#### Remarks

This browser instance will be bound to the default Chromium profile.

