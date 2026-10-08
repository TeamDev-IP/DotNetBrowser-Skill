# <a id="DotNetBrowser_Engine_EngineFactory"></a> Class EngineFactory

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.Core.dll  

Factory class that is used to create <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instances.

```csharp
public static class EngineFactory
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[EngineFactory](DotNetBrowser.Engine.EngineFactory.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="DotNetBrowser_Engine_EngineFactory_Create_DotNetBrowser_Engine_EngineOptions_"></a> Create\(EngineOptions\)

Creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static IEngine Create(EngineOptions options)
```

#### Parameters

`options` [EngineOptions](DotNetBrowser.Engine.EngineOptions.md)

The <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> instance that will be used for initializing the engine

#### Returns

 [IEngine](DotNetBrowser.Engine.IEngine.md)

A completely initialized Chromium engine.

#### Examples

<pre><code class="lang-cs">string dataDir = Path.Combine(Path.GetTempPath(), Guid.NewGuid().ToString());
Directory.CreateDirectory(dataDir);

EngineOptions engineOptions = new EngineOptions.Builder
    {
        UserDataDirectory = dataDir
    }
   .Build();
IEngine engine = EngineFactory.Create(engineOptions);</code></pre>

#### Exceptions

 [EngineInitializationException](DotNetBrowser.Engine.EngineInitializationException.md)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some reason.

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

Native keyboard input is enabled with hardware-accelerated rendering on Windows or Linux.

### <a id="DotNetBrowser_Engine_EngineFactory_Create_DotNetBrowser_Engine_RenderingMode_"></a> Create\(RenderingMode\)

Creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static IEngine Create(RenderingMode renderingMode)
```

#### Parameters

`renderingMode` [RenderingMode](DotNetBrowser.Engine.RenderingMode.md)

The <xref href="DotNetBrowser.Engine.RenderingMode?text=rendering+mode" data-throw-if-not-resolved="false"></xref> that will be used for initializing the engine.

#### Returns

 [IEngine](DotNetBrowser.Engine.IEngine.md)

A completely initialized Chromium engine.

#### Remarks

Calling this method is equivalent to calling the <xref href="DotNetBrowser.Engine.EngineFactory.Create(DotNetBrowser.Engine.EngineOptions)" data-throw-if-not-resolved="false"></xref>
method with the <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> built by calling
<code>new EngineOptions.Builder().Build()</code> with the <xref href="DotNetBrowser.Engine.RenderingMode?text=rendering+mode" data-throw-if-not-resolved="false"></xref> specified.

#### Exceptions

 [EngineInitializationException](DotNetBrowser.Engine.EngineInitializationException.md)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some reason.

### <a id="DotNetBrowser_Engine_EngineFactory_Create"></a> Create\(\)

Creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static IEngine Create()
```

#### Returns

 [IEngine](DotNetBrowser.Engine.IEngine.md)

A completely initialized Chromium engine.

#### Remarks

Calling this method is equivalent to calling the <xref href="DotNetBrowser.Engine.EngineFactory.Create(DotNetBrowser.Engine.EngineOptions)" data-throw-if-not-resolved="false"></xref> method
with the <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> built by calling <code>new EngineOptions.Builder().Build()</code>.

#### Exceptions

 [EngineInitializationException](DotNetBrowser.Engine.EngineInitializationException.md)

The <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some reason.

### <a id="DotNetBrowser_Engine_EngineFactory_CreateAsync"></a> CreateAsync\(\)

Asynchronously creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static Task<IEngine> CreateAsync()
```

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IEngine](DotNetBrowser.Engine.IEngine.md)\>

A task which returns an initialized Chromium engine on completion. The task can throw
<xref href="DotNetBrowser.Engine.EngineInitializationException" data-throw-if-not-resolved="false"></xref> if the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some
reason.

#### Remarks

Calling this method is equivalent to calling the <xref href="DotNetBrowser.Engine.EngineFactory.CreateAsync(DotNetBrowser.Engine.EngineOptions)" data-throw-if-not-resolved="false"></xref>
method with the <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> built by calling <code>new EngineOptions.Builder().Build()</code>.

### <a id="DotNetBrowser_Engine_EngineFactory_CreateAsync_DotNetBrowser_Engine_EngineOptions_"></a> CreateAsync\(EngineOptions\)

Asynchronously creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static Task<IEngine> CreateAsync(EngineOptions options)
```

#### Parameters

`options` [EngineOptions](DotNetBrowser.Engine.EngineOptions.md)

The <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> instance that will be used for initializing the engine

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IEngine](DotNetBrowser.Engine.IEngine.md)\>

A task which returns an initialized Chromium engine on completion. The task can throw
<xref href="DotNetBrowser.Engine.EngineInitializationException" data-throw-if-not-resolved="false"></xref> if the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some
reason.

#### Examples

<pre><code class="lang-cs">string dataDir = Path.Combine(Path.GetTempPath(), Guid.NewGuid().ToString());
Directory.CreateDirectory(dataDir);

EngineOptions engineOptions = new EngineOptions.Builder
    {
        UserDataDirectory = dataDir
    }
   .Build();
IEngine engine = await EngineFactory.CreateAsync(engineOptions);</code></pre>

#### Exceptions

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

Native keyboard input is enabled with hardware-accelerated rendering on Windows or Linux.

### <a id="DotNetBrowser_Engine_EngineFactory_CreateAsync_DotNetBrowser_Engine_RenderingMode_"></a> CreateAsync\(RenderingMode\)

Asynchronously creates and returns an <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> instance.

```csharp
public static Task<IEngine> CreateAsync(RenderingMode renderingMode)
```

#### Parameters

`renderingMode` [RenderingMode](DotNetBrowser.Engine.RenderingMode.md)

The <xref href="DotNetBrowser.Engine.RenderingMode" data-throw-if-not-resolved="false"></xref> that will be used for initializing the engine

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IEngine](DotNetBrowser.Engine.IEngine.md)\>

A task, which returns an initialized Chromium engine on completion. The task can throw
<xref href="DotNetBrowser.Engine.EngineInitializationException" data-throw-if-not-resolved="false"></xref> if the <xref href="DotNetBrowser.Engine.IEngine" data-throw-if-not-resolved="false"></xref> initialization has failed for some
reason.

#### Remarks

Calling this method is equivalent to calling the <xref href="DotNetBrowser.Engine.EngineFactory.CreateAsync(DotNetBrowser.Engine.EngineOptions)" data-throw-if-not-resolved="false"></xref>
method with the <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> built by calling
<code>new EngineOptions.Builder().Build()</code> with the <xref href="DotNetBrowser.Engine.RenderingMode?text=rendering+mode" data-throw-if-not-resolved="false"></xref> specified.

