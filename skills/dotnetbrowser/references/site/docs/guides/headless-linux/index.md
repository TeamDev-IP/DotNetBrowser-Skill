
# Headless mode

## Configuring X server in headless Linux environment

DotNetBrowser library can be used in the headless Linux environment, given the X server is running.

Here is how to start the X Server:

### 1. Install Xvfb server

For example, this can be done via `apt` on Ubuntu 20.04 LTS or other supported Debian-based distributions:

```shell
sudo apt install xvfb
```

### 2. Run your .NET application

Use the `xvfb-run` command to run the command you need in a virtual X server environment. For example, you can wrap `dotnet run` command with `xvfb-run` to run your application from the source code:

```shell
xvfb-run --server-args="-screen 0 800x600x24+32" dotnet run
```

**Note**
It is mandatory to specify the screen size and the color depth.


You can also use `xvfb-run` to define an entrypoint of your Docker container:

```shell
ENTRYPOINT xvfb-run --server-args='-screen 0 800x600x24+32' dotnet Example.Console.dll
```

Check live demo development container configuration in our [quickstart repository.](https://github.com/TeamDev-IP/DotNetBrowser-QuickStart#development-container)

## About the “headless” command line flag

Chromium 58 and higher [support](https://chromium.googlesource.com/chromium/src/+/lkgr/headless/README.md)
the `--headless` command line flag which works for Linux only.

The flag allows to run Chromium in Linux headless environment without
starting the X server.
This flag is designed for the case when you just need to run Chromium in
headless environment, load some URL, and attach to the loaded web page
using DevTools via the `--remote-debugging-port` switch. For example:

```shell
chrome --headless --remote-debugging-port=9222 https://chromium.org
```

In such case you load the `localhost:9222` web page in a web browser
application and work with the loaded web page using DevTools.

As you can see, the `--headless` command line flag is designed to be
used when you need to load a single web page and work with it via
DevTools. We checked Chromium's source code and figured out that this
flag forces Chromium to use a separate, limited version of the Chromium
API that does not support most (~80-90%) of the features used in
DotNetBrowser.

It means that this flag disables most of the DotNetBrowser functionality, such
as loading different web pages by URL, HTML, navigating backward and
forward, executing JavaScript, etc.

This is why this flag is **NOT** supported by DotNetBrowser, and we recommend you to start the X server in order to use DotNetBrowser in a headless Linux environment.
