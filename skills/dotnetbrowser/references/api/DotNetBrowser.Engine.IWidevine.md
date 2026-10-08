# <a id="DotNetBrowser_Engine_IWidevine"></a> Interface IWidevine

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The Widevine DRM (Digital Rights Management) component.

```csharp
public interface IWidevine
```

## Remarks

<p>
    Widevine is used to protect digital content and ensure that it is accessed and used in
    compliance with licensing agreements.
</p>
<p>
    To use Widevine, you must activate it every time you create a new
    <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance. By default, Widevine is not activated. Once activated, you can play protected
    content such as Netflix, Amazon Prime Video, etc. in the browsers of the engine.
</p>
<p>The Widevine component files are stored in the user data directory of the engine.</p>
<p>
    On Windows and macOS, you can activate Widevine without specifying a custom user data
    directory. There's no need to restart the engine after first activation or update, as the changes
    are applied automatically.
</p>
<p>
    On Linux, you must specify a custom user data directory to activate Widevine. It is required
    due to the way Widevine is implemented on Linux. When the component is activated for the first
    time, or it is updated to the latest version during activation, the engine must be restarted to
    apply the changes. To find out if the restart is required, check the activation status:
</p>

<pre><code class="lang-csharp">var status = engine.Widevine.Activate().Result;
if (status == WidevineActivationStatus.RestartRequired)
{
    // Engine restart is required.
}</code></pre>

<p>
    <b>Important</b>: Widevine is a Google proprietary component, governed by its own terms
    of use. For more information, see
    <a href="https://www.widevine.com/">https://www.widevine.com/</a>.
    TeamDev shall not be responsible for your use of Widevine.
</p>

## Properties

### <a id="DotNetBrowser_Engine_IWidevine_Engine"></a> Engine

Gets the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance that this Widevine service belongs to.

```csharp
IEngine Engine { get; }
```

#### Property Value

 [IEngine](DotNetBrowser.Engine.IEngine.md)

### <a id="DotNetBrowser_Engine_IWidevine_IsActivated"></a> IsActivated

Indicates whether Widevine is activated.

```csharp
bool IsActivated { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

## Methods

### <a id="DotNetBrowser_Engine_IWidevine_Activate"></a> Activate\(\)

Activates the Widevine component and updates it to the latest version if it is available.

```csharp
Task<WidevineActivationStatus> Activate()
```

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[WidevineActivationStatus](DotNetBrowser.Engine.WidevineActivationStatus.md)\>

The task that completes with the status of the Widevine activation.

#### Remarks

<p>The Widevine component files are stored in the user data directory of the engine.</p>
<p>
    On Windows and macOS, you can activate Widevine without specifying a custom user data
    directory. There's no need to restart the engine after first activation or update, as the
    changes are applied automatically.
</p>
<p>
    On Linux, you must specify a custom user data directory to activate Widevine. It is
    required due to the way Widevine is implemented on Linux. When the component is activated
    for the first time, or it is updated to the latest version during activation, the engine
    must be restarted to apply the changes.
</p>
<p>
    Here is an example of how to specify a custom user data directory and restart the engine
    if it is required:
</p>

<pre><code class="lang-csharp">var options = new EngineOptions.Builder()
{
    // Specify a custom user data directory.
    UserDataDirectory = "path/to/user/data/dir"
}.Build();
var engine = EngineFactory.Create(options);
// Activate Widevine and restart the engine if necessary.
var status = engine.Widevine.Activate().Result;
if (status == WidevineActivationStatus.RestartRequired)
{
    // Restart the engine with the same options.
    engine.Dispose();
    engine = EngineFactory.Create(options);
}
var browser = engine.CreateBrowser();</code></pre>

#### Exceptions

 [ObjectDisposedException](https://learn.microsoft.com/dotnet/api/system.objectdisposedexception)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> has already been disposed.

 [ConnectionClosedException](DotNetBrowser.Engine.ConnectionClosedException.md)

The connection to the Chromium engine is closed.

#### See Also

[EngineOptions](DotNetBrowser.Engine.EngineOptions.md).[Builder](DotNetBrowser.Engine.EngineOptions.Builder.md).[UserDataDirectory](DotNetBrowser.Engine.EngineOptions.Builder.md\#DotNetBrowser\_Engine\_EngineOptions\_Builder\_UserDataDirectory)

