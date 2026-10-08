# <a id="DotNetBrowser_Engine_BinariesExtractionOptions"></a> Class BinariesExtractionOptions

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The options that are used to configure the Chromium binaries extraction process.

```csharp
public sealed class BinariesExtractionOptions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BinariesExtractionOptions](DotNetBrowser.Engine.BinariesExtractionOptions.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Engine_BinariesExtractionOptions__ctor_System_String_"></a> BinariesExtractionOptions\(string\)

Creates and initializes an instance of <xref href="DotNetBrowser.Engine.BinariesExtractionOptions" data-throw-if-not-resolved="false"></xref>.

```csharp
public BinariesExtractionOptions(string additionalBinariesSearchPath = null)
```

#### Parameters

`additionalBinariesSearchPath` [string](https://learn.microsoft.com/dotnet/api/system.string)

The additional custom path to search for an assembly containing compatible
Chromium binaries.

## Properties

### <a id="DotNetBrowser_Engine_BinariesExtractionOptions_AdditionalBinariesSearchPath"></a> AdditionalBinariesSearchPath

Gets the additional custom path to search for an assembly containing compatible Chromium binaries.

```csharp
public string AdditionalBinariesSearchPath { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="DotNetBrowser_Engine_BinariesExtractionOptions_CheckLinuxDependencies"></a> CheckLinuxDependencies

Indicates whether it is necessary to check if Linux environment has all required shared libraries.

```csharp
public bool CheckLinuxDependencies { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

<p>
    By default, the check is performed.
</p>
<p>
    If <code>false</code>, this step is skipped. It's useful for clients that are confident in their
    environments.
</p>
<p>
    The <code>ldd</code> command is used to check presence of the libraries required
    by Chromium executable.
</p>

### <a id="DotNetBrowser_Engine_BinariesExtractionOptions_Chromium64BitPreferred"></a> Chromium64BitPreferred

Indicates whether 64-bit Chromium binaries are preferred when possible.

```csharp
public bool Chromium64BitPreferred { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

#### Remarks

<p>By default, the bitness of the Chromium process will match the bitness of the .NET process.</p>
<p>
    However, when this option is set to true, the .NET process is 32-bit, and the operating system is 64-bit,
    DotNetBrowser will try using the 64-bit Chromium binaries.
</p>

### <a id="DotNetBrowser_Engine_BinariesExtractionOptions_VerificationLevel"></a> VerificationLevel

Gets or sets the binaries verification level.

```csharp
public BinariesVerificationLevel VerificationLevel { get; set; }
```

#### Property Value

 [BinariesVerificationLevel](DotNetBrowser.Engine.BinariesVerificationLevel.md)

#### Remarks

By default, the binaries verification level is set to <xref href="DotNetBrowser.Engine.BinariesVerificationLevel.Normal" data-throw-if-not-resolved="false"></xref>.

