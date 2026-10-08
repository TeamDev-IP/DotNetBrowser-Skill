# How to generate PDF in C#

This step-by-step tutorial shows how to generate PDF files in C# with
DotNetBrowser.

There are many PDF libraries in the .NET world. But we find it easier to
generate PDFs with an integrated browser. Since DotNetBrowser can work entirely
off the screen, you can use it on servers, both on Windows and Linux.

The algorithm is simple:

1. Load a page.
2. Fill the page with data.
3. Configure the printer.
4. Print the page as PDF.

## Step 1: Create a project

For our task, we don't need the user interface. Therefore, we create a console
application.

Open the Terminal or Command Line prompt, navigate to the necessary directory,
and run the following command:

```shell
dotnet new console -o PdfGeneration
```

## Step 2: Integrate DotNetBrowser

Change the directory to `PdfGeneration` and add one DotNetBrowser package from
NuGet. Choose the package that matches the platforms your application runs on:

```shell
# For Windows:
dotnet add package DotNetBrowser

# For Windows, Linux, and macOS:
dotnet add package DotNetBrowser.CrossPlatform

# For a single platform, such as Linux x64:
dotnet add package DotNetBrowser.Linux-x64
```

Each of these packages fetches the Chromium binaries it needs. For the other
single-platform packages, see the
[NuGet installation guide](https://teamdev.com/dotnetbrowser/docs/guides/installation/nuget/).

After that,
[get your free license](https://teamdev.com/dotnetbrowser#evaluate) to start
using DotNetBrowser.



## Step 3: Load the page

Create a simple console application that starts DotNetBrowser and loads the page
with the template:

```cs
using DotNetBrowser.Browser;
using DotNetBrowser.Browser.Handlers;
using DotNetBrowser.Engine;
using DotNetBrowser.Handlers;
using DotNetBrowser.Print;
using DotNetBrowser.Print.Handlers;

class Program
{
    private static async Task Main()
    {
        var engineOptions = new EngineOptions.Builder
        {
            RenderingMode = RenderingMode.OffScreen,
            LicenseKey = "your license key"
        }.Build();

        using var engine = EngineFactory.Create(engineOptions);
        using var browser = engine.CreateBrowser();

        // The page is a resource in the project.
        var pageUrl = Path.GetFullPath("template.html");   
        await browser.Navigation.LoadUrl(pageUrl);
    }
}
```

> This is a regular page in a regular browser. Thus, use any JavaScript library
> (e.g. plotly.js or D3.js), WebGL, SVG graphics, or any other technology 
> available in Chromium.

## Step 4: Fill the page with data

To fill page with data, use DOM API or execute any JavaScript code. Let's use a
couple of JavaScript functions that we embedded into the page:

```cs
private static void FillInData(IBrowser browser)
{
    var accountNumber = "123-4567";
    var name = "Dr. Emmett Brown";
    var address = "1640 Riverside Drive";
    var reportingPeriod = "Oct 25 — November 25, 1985";

    browser.MainFrame.ExecuteJavaScript(
        $"setBillInfo('{accountNumber}', '{name}', '{address}', '{reportingPeriod}')"
    );

    var dayCost = 500; // Dollars.
    var dayUsage = 1.21; // Gigawatts.
    var nightCost = 312;
    var nightUsage = 88;

    browser.MainFrame.ExecuteJavaScript(
        $"addCharge('Day Tariff', {dayUsage}, {dayCost});" +
        $"addCharge('Night Tariff', {nightUsage}, {nightCost});"
    );
}
```

## Step 5: Configure printing

Tell the browser to print automatically and configure the print settings:

```cs
private static TaskCompletionSource<string> ConfigurePrinting(IBrowser browser)
{
    // Tell the browser to print automatically instead of showing the print preview.
    browser.RequestPrintHandler = 
        new Handler<RequestPrintParameters, RequestPrintResponse>(
            p => RequestPrintResponse.Print()
        );

    TaskCompletionSource<string> whenCompleted = new();
    // When the browser prints an HTML page.
    browser.PrintHtmlContentHandler = 
        new Handler<PrintHtmlContentParameters, PrintHtmlContentResponse>(
            parameters =>
            {
                // Use the PDF printer.
                var printer = parameters.Printers.Pdf;
                var job = printer.PrintJob;
    
                // Generate a random name for PDF file.
                var guid = Guid.NewGuid().ToString();
                var path = Path.GetFullPath($"{guid}.pdf");
                job.Settings.PdfFilePath = path;
    
                // Remove white areas on the sides.
                job.Settings.PageMargins = PageMargins.None;
                // Remove default browser headers and footers.
                job.Settings.PrintingHeaderFooterEnabled = false;
                job.PrintCompleted += (_, e) =>
                {
                    if (e.IsCompletedSuccessfully)
                    {
                        whenCompleted.SetResult(path);
                    }
                    else
                    {
                        var error = "Printing to PDF has failed.";
                        whenCompleted.SetException(
                            new InvalidOperationException(error));
                    }
                };

                // Proceed with printing.
                return PrintHtmlContentResponse.Print(printer);
            });
    return whenCompleted;
}
```

## Step 6: Generate PDF file

Put it all together, start printing, and wait until it's finished:

```cs {hl_lines=["14-17"]}
private static async Task Main()
{
    var engineOptions = new EngineOptions.Builder
    {
        RenderingMode = RenderingMode.OffScreen,
        LicenseKey = "your license key"
    }.Build();

    using var engine = EngineFactory.Create(engineOptions);
    using var browser = engine.CreateBrowser();
    
    await browser.Navigation.LoadUrl(Path.GetFullPath("template.html"));
    
    FillInData(browser);
    var whenPrintCompleted = ConfigurePrinting(browser);
    browser.MainFrame.Print();
    var resultPath = await whenPrintCompleted.Task;
}
```

## Results

Run the program:

```shell
dotnet run
```

And open the generated PDF file:

![PDF document generated in C# by DotNetBrowser](https://teamdev.com/dotnetbrowser/blog/how-to-generate-pdf-in-c-sharp/pdf-generated-by-dotnetbrowser.webp)
<p class="image-caption">PDF document generated in C# by DotNetBrowser</p>

## Source code

You can find the source code of this application in our 
[GitHub repository](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/csharp/console/Printing.WebPageToPdf/Program.cs).

## Discover more

* [Choosing between DotNetBrowser and WebView2](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/)
* [Choosing between DotNetBrowser and CefSharp](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/)
* [Chrome extensions in DotNetBrowser](https://teamdev.com/dotnetbrowser/blog/chrome-extensions-in-dotnetbrowser/)
