# <a id="DotNetBrowser_Chromium_ChromiumBinariesExtractor"></a> Class ChromiumBinariesExtractor

Namespace: [DotNetBrowser.Chromium](DotNetBrowser.Chromium.md)  
Assembly: DotNetBrowser.Core.dll  

A tool that is used to extract the corresponding Chromium binaries.

```csharp
public sealed class ChromiumBinariesExtractor
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ChromiumBinariesExtractor](DotNetBrowser.Chromium.ChromiumBinariesExtractor.md)

#### Inherited Members

[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="DotNetBrowser_Chromium_ChromiumBinariesExtractor__ctor_DotNetBrowser_Engine_BinariesExtractionOptions_"></a> ChromiumBinariesExtractor\(BinariesExtractionOptions\)

Creates and initializes an instance of <xref href="DotNetBrowser.Chromium.ChromiumBinariesExtractor" data-throw-if-not-resolved="false"></xref>.

```csharp
public ChromiumBinariesExtractor(BinariesExtractionOptions extractionOptions = null)
```

#### Parameters

`extractionOptions` [BinariesExtractionOptions](DotNetBrowser.Engine.BinariesExtractionOptions.md)

the extraction options that are used to configure the binaries extractor.

## Properties

### <a id="DotNetBrowser_Chromium_ChromiumBinariesExtractor_DefaultChromiumDirectory"></a> DefaultChromiumDirectory

The default directory that will be used for binaries extraction
if a different location is not specified in the <xref href="DotNetBrowser.Engine.EngineOptions.ChromiumDirectory" data-throw-if-not-resolved="false"></xref>.

```csharp
public string DefaultChromiumDirectory { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="DotNetBrowser_Chromium_ChromiumBinariesExtractor_ExtractBinariesIfNecessary_DotNetBrowser_Engine_EngineOptions_"></a> ExtractBinariesIfNecessary\(EngineOptions\)

Locate and extract the Chromium binaries if the corresponding binaries were not extracted yet
or cannot be found at the location specified in <xref href="DotNetBrowser.Engine.EngineOptions.ChromiumDirectory" data-throw-if-not-resolved="false"></xref>.

<p>
    If the <xref href="DotNetBrowser.Engine.EngineOptions.ChromiumDirectory" data-throw-if-not-resolved="false"></xref> is not specified, the
    <xref href="DotNetBrowser.Chromium.ChromiumBinariesExtractor.DefaultChromiumDirectory" data-throw-if-not-resolved="false"></xref> value will be used for binaries extraction.
</p>

```csharp
public void ExtractBinariesIfNecessary(EngineOptions options)
```

#### Parameters

`options` [EngineOptions](DotNetBrowser.Engine.EngineOptions.md)

the <xref href="DotNetBrowser.Engine.EngineOptions" data-throw-if-not-resolved="false"></xref> instance to use.

