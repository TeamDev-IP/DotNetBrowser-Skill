# <a id="DotNetBrowser_Engine_SandboxNotSupportedException"></a> Class SandboxNotSupportedException

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

Thrown when the current environment does not support creating processes within a new user namespace,
preventing Chromium from being launched in sandbox mode.

```csharp
public sealed class SandboxNotSupportedException : EngineInitializationException, ISerializable
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Exception](https://learn.microsoft.com/dotnet/api/system.exception) ← 
[EngineInitializationException](DotNetBrowser.Engine.EngineInitializationException.md) ← 
[SandboxNotSupportedException](DotNetBrowser.Engine.SandboxNotSupportedException.md)

#### Implements

[ISerializable](https://learn.microsoft.com/dotnet/api/system.runtime.serialization.iserializable)

#### Inherited Members

[Exception.GetBaseException\(\)](https://learn.microsoft.com/dotnet/api/system.exception.getbaseexception), 
[Exception.GetObjectData\(SerializationInfo, StreamingContext\)](https://learn.microsoft.com/dotnet/api/system.exception.getobjectdata), 
[Exception.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.exception.gettype), 
[Exception.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.exception.tostring), 
[Exception.Data](https://learn.microsoft.com/dotnet/api/system.exception.data), 
[Exception.HelpLink](https://learn.microsoft.com/dotnet/api/system.exception.helplink), 
[Exception.HResult](https://learn.microsoft.com/dotnet/api/system.exception.hresult), 
[Exception.InnerException](https://learn.microsoft.com/dotnet/api/system.exception.innerexception), 
[Exception.Message](https://learn.microsoft.com/dotnet/api/system.exception.message), 
[Exception.Source](https://learn.microsoft.com/dotnet/api/system.exception.source), 
[Exception.StackTrace](https://learn.microsoft.com/dotnet/api/system.exception.stacktrace), 
[Exception.TargetSite](https://learn.microsoft.com/dotnet/api/system.exception.targetsite), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

<p>
    When this exception is thrown, consider disabling the sandbox mode via
    <xref href="DotNetBrowser.Engine.EngineOptions.Builder.SandboxDisabled" data-throw-if-not-resolved="false"></xref> property or by adding the
    <code>--no-sandbox</code> switch to <xref href="DotNetBrowser.Engine.EngineOptions.Builder.ChromiumSwitches" data-throw-if-not-resolved="false"></xref>.
</p>
<p>
    For more information, see
    <a href="https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#sandbox">https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#sandbox</a>.
</p>

