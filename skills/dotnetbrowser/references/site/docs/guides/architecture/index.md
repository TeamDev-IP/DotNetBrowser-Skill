
# Architecture

**Lead**
This is an overview of the DotNetBrowser architecture.


## Overview

The architecture of the DotNetBrowser library consists of multiple processes such as .NET application and different Chromium ones:

<div class="diagram-box">


</div>

Sections below provide the details for each of the processes, the main components of the library, and describe how it all works.

### Processes
#### .NET process

This is a standard .NET process where your .NET application runs.

#### Chromium main process

This is the main process of the Chromium engine. It is started by DotNetBrowser when you [create](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#creating-an-engine) an `IEngine` instance.

**Note**
For each `IEngine` instance, a separate Chromium Main process is used.


#### Chromium renderer process

This process contains the `IFrame` instances which manage DOM and JavaScript of the loaded web page. The process is started by the Chromium engine when you navigate `IBrowser` to a web page with a different domain.

#### Chromium GPU process

This process renders the content of the web pages loaded in different Chromium Renderer processes using the GPU.

#### Inter-process communication

Communication between different processes is performed using Inter-Process Communication (IPC). IPC transfers data between two processes on a local machine.

To transfer data between .NET and Chromium processes, DotNetBrowser uses its own IPC implementation based on sockets and shared memory. Communication between the Chromium processes is performed using [Chromium IPC](https://www.chromium.org/developers/design-documents/inter-process-communication) implementation.

### Main components
#### IEngine

The `IEngine` instance manages the lifecycle of the Chromium Main process and provides access to the core Chromium functionality such as zoom, proxy, cache, cookies, plugins, downloads, etc. associated with the default `Profile`.

All the operations with the engine are performed through the `IEngine` interface. Engine is a top-level object in the objects hierarchy of the library. Any actions with the library begin with creation of an `IEngine` instance.

For detailed instructions on creation and usage of the `IEngine` instance, please see the [Engine](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/) guide.

#### Profile

Represents a Chromium profile. It allows keeping all browser data separately, like history, cookies, cache, proxy settings, spellchecker configurations, etc. Each `IEngine` has a default profile that is created automatically during `Engine` initialization. The default profile cannot be deleted.

You can create new profiles and delete them if they are not required using the `Profiles` service.

The profile's files for history, cookies, cache, etc. are stored in the [user data directory](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#user-data-directory). If you configure `IEngine` with the user data directory and create a profile, it will be stored in the user data directory and be restored after application restart.

Read more about profiles in the [Profile](https://teamdev.com/dotnetbrowser/docs/guides/gs/profile/) guide.

#### Browser

This is a web browser, which can be used to perform a number of actions, such as:
 * loading web pages or local HTML files; 
 * finding text on the loaded web page;
 * modifying zoom level;
 * enabling or muting audio; 
 * getting notifications about loading progress; 
 * dispatching keyboard and mouse events.

All the operations with the browser are performed through the `IBrowser` interface. Each `IBrowser` instance [is bound](https://teamdev.com/dotnetbrowser/docs/guides/design/#relationship) to `Profile`. The `IBrowser` instance is disposed automatically when its `Profile` is deleted or parent `IEngine` instance crashes or it is disposed by the application.

For details on how to create and use the `IBrowser` instance, see the [Browser](https://teamdev.com/dotnetbrowser/docs/guides/gs/browser/) guide.

#### Frame

Any web page loaded in the `IBrowser` instance has a main `IFrame` instance in it. This `IFrame` may have child frames. You can use the `IFrame` instances to access and work with [DOM](https://teamdev.com/dotnetbrowser/docs/guides/gs/dom/) and [JavaScript](https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/). When a web page is unloaded, its main `IFrame` instance and all child frames are disposed automatically.

## How it works

### Creating an engine

When you create an `IEngine` instance, the library performs the following actions:

1. Start the *Chromium Main* and *GPU* processes.
2. Initialize the Chromium engine in the Chromium Main process.
3. Initialize the default profile.
4. Establish the IPC connection between .NET and the Chromium Main process.

<div class="diagram-box">


</div>

If you create two `IEngine` instances, separate *Chromium Main* and *GPU* processes are started for each of them. See the example below:

<div class="diagram-box">


</div>

### Creating a browser

When you create an `IBrowser` instance, the library automatically loads an `about:blank` web page in it. As a result, the *Chromium Renderer* process is started to handle all the DOM and JavaScript on the web page:

<div class="diagram-box">


</div>

**Note**
If you navigate the `IBrowser` instance to a web page, the page is loaded in this *Chromium Renderer* process. If you navigate to a web page from a different domain later, it is loaded in a different *Chromium Renderer* process instance which is started automatically. Note that the *Chromium Renderer* process that handled the contents of the previous web page will be terminated.


### Browser dispose

When you release the `IBrowser` instance, corresponding *Chromium Renderer* process is terminated automatically. As a consequence, all the `IFrame` instances running in the terminated process will be automatically disposed as well:

<div class="diagram-box">


</div>

### Engine dispose

When you dispose the `IEngine`instance, the library performs the following actions:

1. Closing existing IPC connection between .NET and the Chromium Main processes.
2. Disposal of the Chromium engine in the Chromium Main process.
3. Terminating the Chromium Main and GPU processes.
