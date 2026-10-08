# <a id="DotNetBrowser_Print_Settings_IFooterTemplate_1"></a> Interface IFooterTemplate<TPrintSettings\>

Namespace: [DotNetBrowser.Print.Settings](DotNetBrowser.Print.Settings.md)  
Assembly: DotNetBrowser.dll  

Allows configuring the HTML template for the print footer.

```csharp
public interface IFooterTemplate<out TPrintSettings> where TPrintSettings : class, IPrintSettings
```

#### Type Parameters

`TPrintSettings` 

The specific print settings type.

#### Extension Methods

[FooterTemplateExtensions.SetFooterTemplate<TPrintSettings\>\(IFooterTemplate<TPrintSettings\>, string\)](DotNetBrowser.Print.Settings.FooterTemplateExtensions.md\#DotNetBrowser\_Print\_Settings\_FooterTemplateExtensions\_SetFooterTemplate\_\_1\_DotNetBrowser\_Print\_Settings\_IFooterTemplate\_\_\_0\_\_System\_String\_)

## Remarks

<p>
    This interface is implemented by specific <xref href="DotNetBrowser.Print.Settings.IPrintSettings" data-throw-if-not-resolved="false"></xref> implementations that support configuring
    the footer for printing.
</p>

## Properties

### <a id="DotNetBrowser_Print_Settings_IFooterTemplate_1_FooterTemplate"></a> FooterTemplate

Gets or sets the HTML to be displayed in the footer.

```csharp
string FooterTemplate { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

#### Remarks

<p>
           Apply the following CSS classes to insert printing metadata into the template. These classes
           don't affect the visual appearance of the elements.

       <ul>
               <li><code>date</code>: the formatted print date;</li>
               <li><code>title</code>: the document title;</li>
               <li><code>url</code>: the document location;</li>
               <li><code>pageNumber</code>: the current page number;</li>
               <li><code>totalPages</code>: the total page count in the document;</li>
           </ul>
       </p>
       <p>
           For example, 

       <pre><code class="lang-csharp"></code></pre>

would generate a span containing a title.
       </p>
       <p>
           The programming, audio/video, and frame tags are not supported. Images are supported
           only with Base64 content.
       </p>

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

The specified footer template is null.

