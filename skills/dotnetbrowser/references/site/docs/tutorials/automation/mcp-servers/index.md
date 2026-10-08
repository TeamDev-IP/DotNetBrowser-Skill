
# MCP servers

**Lead**
Playwright MCP and Chrome DevTools MCP can attach to the browser your
application already embeds. This tutorial covers the client configuration,
what an AI agent does on the page, and the limits of CDP mode.


An MCP server gives an AI agent a set of tools over the Model Context
Protocol. The agent's client, such as Claude Code, VS Code, or Cursor, starts
the server and calls its tools. Browser MCP servers offer tools that read the
page, click, type, and run scripts.

Playwright MCP and Chrome DevTools MCP normally launch their own copy of
Chrome. Both can also connect to a running Chromium over the Chrome DevTools
Protocol, or CDP, which is how they attach to DotNetBrowser. The agent then
operates on the page shown in the `BrowserView` control, and every click and
keystroke appears in your application's window.

Read [DevTools Protocol](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/) first
for the rules that apply to every tool that connects over CDP.

## Prerequisites

You need three things:

* Node.js 20.19, 22.12, or newer. Chrome DevTools MCP requires it, and the
  Playwright package that Playwright MCP installs declares Node.js 20 as its
  minimum, although the Playwright MCP README asks for Node.js 18.
* An MCP client that starts local servers, such as Claude Code, VS Code, or
  Cursor.
* An engine created with `RemoteDebuggingPort` set to a free port, as
  described in
  [DevTools Protocol](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/#opening-the-endpoint).
  The example uses `9224`.

**Note**
The behavior described here was tested with `@playwright/mcp` 0.0.82,
`chrome-devtools-mcp` 1.10.1, Node.js 22.20, Claude Code 2.1.280, and VS Code
1.132.0 on Windows. Newer versions of the servers can behave differently. To
reproduce this setup, replace `@latest` with `@0.0.82` for Playwright MCP and
`@1.10.1` for Chrome DevTools MCP.


## Connecting Playwright MCP

Start Playwright MCP with `--cdp-endpoint` set to the endpoint URL. In Claude
Code, add the server with this command:

```bash
claude mcp add playwright -- npx @playwright/mcp@latest --cdp-endpoint http://127.0.0.1:9224
```

Everything after `--` is the command that starts the server. To share the
configuration with your team, add `--scope project` before `--`. Claude Code
then stores the server in `.mcp.json` at the project root:

```json
{
  "mcpServers": {
    "playwright": {
      "type": "stdio",
      "command": "npx",
      "args": [
        "@playwright/mcp@latest",
        "--cdp-endpoint",
        "http://127.0.0.1:9224"
      ]
    }
  }
}
```

In VS Code, the configuration goes to `.vscode/mcp.json`, and the top-level
key is `servers` rather than `mcpServers`. VS Code starts workspace servers
only after you trust the workspace:

```json
{
  "servers": {
    "playwright": {
      "command": "npx",
      "args": [
        "@playwright/mcp@latest",
        "--cdp-endpoint",
        "http://127.0.0.1:9224"
      ]
    }
  }
}
```

Other clients, such as Cursor, take the same `command` and `args` in their own
configuration.

Once connected, Playwright MCP reuses the engine's browser context and makes
its first page the current tab. The agent does not have to navigate anywhere:
its first `browser_snapshot` call returns the accessibility tree of the page
your application displays.

DotNetBrowser does not support opening a new tab from the agent. As
[Attach, do not launch](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/#attach-do-not-launch)
explains, browsers are created in other ways: by your application or as
pop-ups. The engine answers the CDP `Target.createTarget` command with an
empty target ID and creates no page, so the `browser_tabs` tool with the `new`
action returns this error:

```text
TypeError: browserBackend.callTool: Cannot read properties of undefined (reading '_page')
```

For the same reason, do not start the server with `--isolated`. Over CDP, that
option makes Playwright MCP create a browser context of its own instead of
reusing the engine's. The engine creates the context, but opening a page in it
is not supported, so every tool call then returns the same error.

Playwright MCP waits up to 30 seconds for the CDP connection by default, and
`--cdp-timeout` sets another limit in milliseconds. A refused connection fails
at once, regardless of the limit.

Playwright MCP saves snapshots and console logs to a `.playwright-mcp` folder
in the working directory of the client, which in VS Code is the workspace
root.

## Connecting Chrome DevTools MCP

Chrome DevTools MCP connects to a running browser with `--browser-url`, which
also accepts `--browserUrl` and the short form `-u`. In Claude Code:

```bash
claude mcp add chrome-devtools -- npx chrome-devtools-mcp@latest --browser-url=http://127.0.0.1:9224
```

In `.mcp.json`:

```json
{
  "mcpServers": {
    "chrome-devtools": {
      "type": "stdio",
      "command": "npx",
      "args": [
        "chrome-devtools-mcp@latest",
        "--browser-url=http://127.0.0.1:9224"
      ]
    }
  }
}
```

In VS Code, the same entry goes under `servers` in `.vscode/mcp.json`.

The `--ws-endpoint` option takes the engine's WebSocket URL instead. That URL
changes every time the engine starts, so `--browser-url` is the practical
choice.

On connection, the server lists the open pages and selects the first one.
`list_pages` shows the page your application displays as page `1`, marked as
selected, and the page tools take that number as `pageId`.

DotNetBrowser does not support `new_page` either, with or without the
`isolatedContext` parameter. The server waits 30 seconds for a page that the
engine does not create, and returns `Error: Timed out after waiting 30000ms`.

Chrome DevTools MCP officially supports only Google Chrome and Chrome for
Testing. Other Chromium-based browsers, DotNetBrowser among them, may work,
with no guarantee.

Chrome DevTools MCP sends usage statistics to Google by default. Add
`--no-usage-statistics` to turn this off, or set the
`CHROME_DEVTOOLS_MCP_NO_USAGE_STATISTICS` or `CI` environment variable. Its
performance tools also send the URLs of traced pages to the Chrome UX Report
API unless you add `--no-performance-crux`.

## Do the servers need `--remote-allow-origins`?

No. Neither server sends an `Origin` header when it connects, so the engine
accepts the connection without the switch. Both servers connected to an
engine created with nothing but `RemoteDebuggingPort`.

The switch matters only when you make a server send an `Origin` header
yourself, through Playwright MCP `--cdp-header` or Chrome DevTools MCP
`--ws-headers`. Chromium then answers `403 Forbidden`, and the error the agent
receives includes Chromium's explanation:

```text
Rejected an incoming WebSocket connection from the http://example.com origin. Use the command line flag --remote-allow-origins=http://example.com to allow connections from this origin or --remote-allow-origins=* to allow all origins.
```

Pass that switch through `ChromiumSwitches`, as the
[Engine](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#remote-debugging-port) guide shows. With the
origin allowed, both servers connect again.

## What the agent sees and does

The example application loads a page with a "Recent orders" table and a
"New order" form. In one run, Claude Code received this prompt, with
Playwright MCP as its only source of tools:

```text
The embedded browser already shows an Orders page. Read the "Recent orders"
table and tell me the total quantity ordered. Then add an order for Dana Lee,
dana@example.com, product Headset, quantity 4, and confirm that the new row
appears in the table.
```

The agent made four tool calls. In the excerpt, each line that starts with `>`
is a call, and the lines below it are the result, trimmed to the relevant
parts. Playwright MCP includes the Playwright code for each action in the
result:

```text
> browser_snapshot {}
- Page URL: file:///E:/.../McpServers/bin/Debug/net9.0-windows/orders.html
- Page Title: Orders
    - textbox "Customer" [ref=e35]
    ...
    - button "Add order" [ref=e42]

> browser_fill_form {"fields":[
    {"target":"e35","name":"Customer","type":"textbox","value":"Dana Lee"},
    {"target":"e37","name":"Email","type":"textbox","value":"dana@example.com"},
    {"target":"e39","name":"Product","type":"combobox","value":"Headset"},
    {"target":"e41","name":"Quantity","type":"textbox","value":"4"}]}
await page.getByRole('textbox', { name: 'Customer' }).fill('Dana Lee');
...

> browser_click {"target":"e42","element":"Add order button"}
await page.getByRole('button', { name: 'Add order' }).click();

> browser_snapshot {}
      - row [ref=e43]:
        - cell "1004" [ref=e44]
        - cell "Dana Lee" [ref=e45]
        - cell "dana@example.com" [ref=e46]
        - cell "Headset" [ref=e47]
        - cell "4" [ref=e48]
```

In this run, the agent read the page from its accessibility tree, not from
pixels. `browser_snapshot` returns that tree with a reference, such as `e35`,
for each element, and the following calls use those references.

The agent reported a total quantity of 6 before the new order and 10 after
it. It works on the page the `BrowserView` control displays, so the new row
appears in your application's window. With Chrome DevTools MCP, the same
prompt led to `list_pages`, `take_snapshot`, `fill_form`, `click`, and
`take_snapshot`, with the same result.

The calls depend on the client and the model. In VS Code, the agent completed
the same task with both servers but took a different route: for example, it
read the table with `browser_evaluate` and addressed the form fields by CSS
selectors rather than snapshot references.

## Limits of CDP mode

Page-level tools work as usual: snapshots, clicks, form input, script
evaluation, console messages, screenshots, and navigation. Playwright MCP also
saves the page as PDF when started with `--caps=pdf`, and Chrome DevTools MCP
records performance traces. Most of the limits come from tools that assume
the server launched the browser:

* **Launch switches.** Both servers normally launch Chrome with a set of
  command-line switches of their own. DotNetBrowser starts Chromium with a
  different set, so a tool that relies on one of those switches can behave
  differently here.
* **Browser process.** Anything that assumes the server owns the browser
  process — closing the browser, launch options, and the tooling built on
  them — does not apply. Playwright MCP `browser_close` only disconnects: the
  page stays open, and the next tool call reconnects to it.
* **New tabs.** Opening a tab is not supported, as described in the
  connection sections above. A server can create a browser context, but not a
  page in it.
* **Pop-ups.** A page can still open a [pop-up](https://teamdev.com/dotnetbrowser/docs/guides/gs/popups/) with
  `window.open`, for example from a script the agent runs. With the default
  pop-up handlers of `BrowserView`, the pop-up opens in a separate window of
  your application, and both servers list it as a new tab or page that the
  agent can select, read, and close.
* **Several pages.** Both servers start on the first page they find. With
  several `IBrowser` instances, that is not necessarily the page your users
  see, as
  [Attach, do not launch](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/#attach-do-not-launch)
  explains. Ask the agent to list the pages and select one by its URL.
* **Closing the page.** Playwright MCP `browser_tabs` with the `close` action
  closes the page your application displays: DotNetBrowser disposes that
  `IBrowser`, the `BrowserView` control goes blank, and later tool calls
  fail. Chrome DevTools MCP `close_page` refuses to close the last open page,
  so it protects the page your application displays only while no pop-up is
  open.
* **Resizing.** Playwright MCP `browser_resize` and Chrome DevTools MCP
  `resize_page` do not resize your application's window. They resize
  Chromium's own window inside the `BrowserView` control, so the page no
  longer matches the control, and a larger size is cut off at the edges. The
  size stays in effect after the server disconnects and after a reload, until
  the control itself is resized. Chrome DevTools MCP `emulate` with a
  `viewport` has the same effect until the emulation is cleared.
* **`file://` URLs.** Playwright MCP blocks `browser_navigate` to `file://`
  URLs unless you start it with `--allow-unrestricted-file-access`. A page
  your application loaded from a file stays available without the option.
  Chrome DevTools MCP navigates to `file://` URLs without extra options.

Neither server checks the Chromium version it attaches to. As with Playwright
and Puppeteer, a tool that relies on a CDP command newer than DotNetBrowser's
Chromium build can fail; see
[Match the Chromium version](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/#match-the-chromium-version).

## Security

**Important**
The remote debugging endpoint has no authentication. Any process on the same
machine that can reach the port can control the pages in that engine, and an
MCP server is such a process.


An agent adds a second risk. Everything the server returns — page text,
snapshots, console messages, network data — becomes input to the model. Text
on the page can therefore steer the agent, which is known as prompt
injection. A page that shows content your team does not control, such as
user comments or third-party widgets, can contain instructions addressed to
the agent, and the agent may act on them with the tools it has.

The Playwright MCP README states that Playwright MCP is not a security
boundary. Chrome DevTools MCP prints a notice every time it starts: the server
exposes the browser content to the MCP client, which can inspect and modify
any data in the browser.

To limit the risk:

* Enable `RemoteDebuggingPort` only in development and test builds, as the
  [overview](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/#security)
  recommends.
* Keep the endpoint local. It listens on `127.0.0.1` only; do not expose the
  port through port forwarding or a proxy.
* When the page shows content you do not control, give the agent only the
  tools the task needs:
  * Chrome DevTools MCP removes tool categories with `--no-category-*`
    options. For example, `--no-category-navigation` removes `navigate_page`,
    `new_page`, and the other page-management tools, and
    `--no-javascript-evaluation` removes `evaluate_script`.
  * Playwright MCP has no option that removes its core tools; `--caps` only
    adds optional ones. Restrict it in the client instead. For example, start
    Claude Code with `--disallowedTools` followed by
    `mcp__playwright__browser_run_code_unsafe`, which runs arbitrary Playwright
    code, and `mcp__playwright__browser_evaluate`, which runs JavaScript on
    the page.

## Off-screen rendering

`RemoteDebuggingPort` does not depend on the rendering mode. Both servers
attach to an engine created with `RenderingMode.OffScreen` in the same way,
and snapshots and screenshots work with no window on screen. That suits
agent-driven test runs in CI, where nobody watches the window.

## Troubleshooting

* **The connection is refused.** Playwright MCP reports
  `connect ECONNREFUSED 127.0.0.1:9224`, and Chrome DevTools MCP reports
  `Could not connect to Chrome. Check if Chrome is running.` Check that the
  application is running and that the port matches `RemoteDebuggingPort`.
  Prefer `127.0.0.1` to `localhost`: the endpoint listens on `127.0.0.1`
  only, and `localhost` can resolve to `::1` first. Both servers connected
  through `localhost` with Node.js 22, but the explicit address rules the
  question out.
* **The server started before the engine.** The first tool call fails at
  once with the errors above; neither server waits for the endpoint. You do
  not need to restart the server: the first tool call after the engine
  starts connects. The same applies when your application restarts while the
  server keeps running. Chrome DevTools MCP then assigns new page IDs and
  says so in its reply.
* **The agent sees `about:blank`.** If the agent connects right after the
  engine starts, your page can still be loading. Ask the agent to take the
  snapshot again.
* **The connection fails with `403 Forbidden`.** The server sent an `Origin`
  header. See
  [Do the servers need `--remote-allow-origins`?](#do-the-servers-need---remote-allow-origins)
* **A single tool fails while others work.** The tool may rely on a CDP
  command that DotNetBrowser's Chromium build does not have. See
  [Match the Chromium version](https://teamdev.com/dotnetbrowser/docs/tutorials/automation/devtools-protocol/#match-the-chromium-version).
* **The page is cut off or does not fill the window.** A resize or emulation
  tool changed the size the page is laid out at. Resize the window to restore
  it, or, after Chrome DevTools MCP `emulate`, ask the agent to clear the
  emulation.

The complete example is available in our repository:
[C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/csharp/devtools-protocol/McpServers),
[VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/vbnet/devtools-protocol/McpServers).
