# C# desktop app with Shadcn UI

For years, .NET developers have built desktop apps with toolkits like WinForms
and WPF. These frameworks get the job done and give you native controls, but
making them look modern takes a lot of extra work. The default components feel
old-fashioned, and adding smooth animations or a clean, modern style isn’t
exactly straightforward.

The web, on the other hand, moves fast. With frameworks like React and 
a massive library ecosystem, developers can spin up responsive, 
good-looking interfaces in no time. That’s why so many popular 
apps — Slack, Notion, Microsoft Teams — use web-based UIs even for their 
desktop versions.

In this article, we suggest an architecture that keeps flexibility and
productivity of the web, while delivering a native desktop experience.

## Why web UI on desktop?

Using a web UI in a desktop application brings clear advantages that go beyond
looks. Modern web tech makes it **easy to build** clean, responsive interfaces
that just feel right across different platforms.

The real power comes from the **huge ecosystem**. There’s a huge pool of
ready-to-use components and plenty of web developers out there, so you spend
less time reinventing things and more time actually building your app.

Cross-platform support is another win. With frameworks like Avalonia or
DotNetBrowser, you can run the same code on **Windows, macOS, and Linux**
instead of maintaining separate versions for each system.

And then there’s flexibility. The same frontend can live **both on the web 
and the desktop**, so you keep things simple, reuse your work, and roll 
out updates without doing everything twice.

![Screenshot of the desktop app with web UI][img-screenshot]
<p class="image-caption">Screenshot of the desktop app with web UI.</p>

The full source code is available on [GitHub][github].

## Challenges

At first glance, embedding a web interface into a .NET desktop app seems
straightforward, but there are several challenges that need to be addressed:

* **Secure resource loading.** The application should not depend on a local or
  remote server for loading its UI, and the bundled resources must not be
  exposed.
* **Communication between JavaScript and .NET.** The web UI needs a safe and
  structured way to call backend logic and receive results.

Let’s see how Avalonia and DotNetBrowser can help solve these challenges.

## Application Window and Web View

We use Avalonia to create the application window and handle native integration.
Inside the window, we embed DotNetBrowser’s `BrowserView` — a Chromium-based web
view component.

**XAML window definition:**

```xml
<Window ...>
    <app:BrowserView x:Name="BrowserView" />
</Window>
```

**Initialization in code-behind:**

```c#
private async void Window_Opened(object? sender, EventArgs e)
{
    Browser = ServiceProvider.GetService<IEngineService>()?.CreateBrowser();
    BrowserView.InitializeFrom(Browser);
    await Browser.Navigation.LoadUrl("dnb://internal.host/");
}
```

In the code-behind, we initialize the Chromium engine and then load the special
internal UI, not available from the outside.

## Loading pages

In web development, it’s common to run the app through a local dev server that
automatically reloads changes as you code — a workflow most front-end developers
take for granted. In our setup, we keep that same approach: the web app runs
locally with hot reload enabled, so you can see updates instantly without
rebuilding the entire desktop app each time.

In production, we don’t want to rely on a web server. Why? First, anyone with
access to the server’s URL could peek into its resources, including logic that’s
supposed to stay private. Second, it adds extra moving parts, making deployment
and maintenance more complicated than necessary.

Instead, we embed the frontend resources inside the application package and make
them available only within the app.

DotNetBrowser provides **custom scheme handlers** for this purpose. A scheme
handler allows us to intercept requests for specific URL schemes,
like <nobr>`my-app://`</nobr> and respond to them with arbitrary data, rather 
than fetching from a remote server. In our example, when a browser requests 
<nobr>an `index.html`</nobr> or any other file, we will read it from 
the application resources:

```c#
public class ResourceRequestHandler
    : IHandler<InterceptRequestParameters, InterceptRequestResponse>
{

    public InterceptRequestResponse Handle(InterceptRequestParameters parameters)
    {
        string url = parameters.UrlRequest.Url;
        // Locate and serve embedded resource (index.html, JS, CSS).
        ...
    }
}
...

EngineOptions engineOptions = new EngineOptions.Builder
{
    Schemes = 
    {
        { Scheme.Create("my-app"), new ResourceRequestHandler() }
    }
}.Build();

IEngine engine = EngineFactory.Create(engineOptions);
```

With this setup, we intercept all requests to `my-app://` URL scheme, and let
regular HTTP requests pass through. The result is a secure, self-contained
package that runs offline and keeps resources hidden from direct access.

## JavaScript and .NET communication

A web UI is great for presentation, but most of the real work still happens
elsewhere. Things like reading or writing files, saving settings, or talking to
the operating system can only be done by the .NET backend. Still, 
the frontend has to trigger those actions and get the results back. That’s 
why we need a way for JavaScript and .NET to talk to each other.

### Direct calls between JavaScript and .NET

For small projects, a simple bridge may be enough. Most web view components let
JavaScript directly communicate with .NET. Some handle this by passing JSON
messages back and forth. Others, like DotNetBrowser, let you access .NET
objects right from JavaScript, and vice versa. Here's a simple example.

First, we define a class in C#. Then, we mirror it in TypeScript, keeping the
same interface. Then we configure DotNetBrowser to inject the .NET instance into
a JavaScript object of the matching type.

Let's consider the following simple C# class:

```c#
public class PrefsService {

    public void SetBrightness(int percents) {
        ...
    }
}
```

Then, let's mirror it in TypeScript:

```typescript
// The matching class.
declare class PrefsService { 

   SetBrightness(percents: number): void; 
}

// The global variable that will host the object.
declare const prefService: PrefsService;
...
prefService.SetBrightness(95);
```

And finally, when the page loads, we inject the .NET object into 
the declared JavaScript variable:

```c#
browser.InjectJsHandler = new Handler<InjectJsParameters>(p =>
{
    dynamic window = p.Frame.ExecuteJavaScript("window").Result;
    if (window != null)
    {
        window.prefService = new PrefsService();
    }
});
```

That’s a simple and effective approach — at least in the beginning. The problem
is, it doesn't scale well. You have to manually keep the C# and TypeScript
definitions in sync, and as the API grows and evolves, the inevitable mismatches
will be a constant source of bugs.

### RPC between JavaScript and .NET

Instead of keeping two separate definitions in sync, we can define the data once
and let tooling handle the generation of matching code in C# and TypeScript.

We use [Protobuf][protobuf] and [gRPC][grpc] to handle communication between the
frontend and backend. Protobuf defines the shared data structures and services 
in a language-neutral way and generates type-safe code for both C# and 
TypeScript.

The result: requests and responses are checked at build time, and you get full
type hints and autocompletion without any extra setup.

![Communication diagram][img-comm-diagram]

<p class="image-caption">Communication between JavaScript and .NET.</p>

Here's the equivalent Protobuf definition:

```proto
service PrefsService {
 rpc SetBrightness(Brightness) returns (google.protobuf.Empty);
}

message Brightness {
 int32 percents = 1;
}
```

And the .NET implementation that auto-generated types from the Protobuf
definition:

```c#
public override Task<Empty> SetBrightness(Brightness brightness, ServerCallContext context)
{
    int percents = brightness.Percents;
    ...
    return Task.FromResult(new Empty());
}
```

This time, we don't need to inject an object. But we need to pass the gRPC host
to frontend, so it can connect:

```c#
browser.InjectJsHandler = new Handler<InjectJsParameters>(p =>
{
    dynamic window = p.Frame.ExecuteJavaScript("window").Result;
    if (window != null)
    {
        window.rpcAddress = "http://localhost:5051";
    }
});
```

Now the web frontend can use auto-generated code to send requests to 
the .NET backend:

```typescript
import {createGrpcWebTransport} from "@connectrpc/connect-web";
import {createClient} from "@connectrpc/connect";
import {PreferencesService} from "@/gen/prefs_pb.ts";

const transport = createGrpcWebTransport({
   baseUrl: `http://localhost:50051`,
});

const prefsClient = createClient(PrefsService, transport);
...
prefsClient.SetBrightness(...);
```

## Conclusion

Building desktop apps with a web UI makes development faster and more flexible.
You get to use modern tools, tap into the huge web ecosystem, and deliver
interfaces that look and feel up to today’s standards.

In this article, we mixed web and desktop tech — using DotNetBrowser to host 
a React-based UI, bundling the frontend right into the app, and wiring up 
two-way communication between .NET and JavaScript.

Along the way, we solved a few common pain points: embedding the web view,
loading static files without a local server, and making the frontend and backend
talk smoothly.



[img-screenshot]: https://teamdev.com/dotnetbrowser/blog/c-sharp-desktop-app-with-shadcn-ui/avalonia-shadcn-ui-screenshot.webp
[img-comm-diagram]: https://teamdev.com/dotnetbrowser/blog/c-sharp-desktop-app-with-shadcn-ui/communication-diagram.svg
[github]: https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v3/csharp/web-ui
[protobuf]: https://protobuf.dev/
[grpc]: https://grpc.io/
