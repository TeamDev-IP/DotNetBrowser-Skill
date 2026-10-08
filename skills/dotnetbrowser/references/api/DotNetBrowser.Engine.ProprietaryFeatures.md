# <a id="DotNetBrowser_Engine_ProprietaryFeatures"></a> Enum ProprietaryFeatures

Namespace: [DotNetBrowser.Engine](DotNetBrowser.Engine.md)  
Assembly: DotNetBrowser.dll  

The list of supported proprietary features.

```csharp
[Flags]
public enum ProprietaryFeatures
```

## Fields

`Aac = 64` 

<p>Represents support of the AAC codec.</p>
<p>
    <b>Important</b>: AAC codec is a proprietary component. By enabling this codec you
    state that you are aware that AAC is a proprietary component and you should have a license
    in order to use it. For more information, you could contact patent holders: Via Licensing and
    MPEG LA. TeamDev shall not be responsible for your use of AAC codec.
</p>



`H264 = 1` 

<p>Represents support of the H.264 codec.</p>
<p>
    <b>Important</b>: H.264 codec is a proprietary component. By enabling this codec you
    state that you are aware that H.264 is a proprietary component and you should have a license
    in order to use it. For more information, you could contact patent holders: Via Licensing and
    MPEG LA. TeamDev shall not be responsible for your use of H.264 codec.
</p>



`Hevc = 16` 

<p>Represents support of the HEVC codec.</p>
<p>
    <b>Important</b>: HEVC codec is a proprietary component. By enabling this codec you
    state that you are aware that HEVC is a proprietary component and you should have a license
    in order to use it. For more information, you could contact patent holders: Via Licensing and
    MPEG LA. TeamDev shall not be responsible for your use of HEVC codec.
</p>



`None = 0` 

No proprietary features enabled.



