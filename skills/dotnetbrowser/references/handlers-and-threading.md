# Handlers, events, and threads

Paths are relative to the skill folder, the one that holds `SKILL.md`.

- Configurable behavior is exposed as handler *properties* of type
  `IHandler<TParameters>` or `IHandler<TParameters, TResponse>`, for example
  `browser.CreatePopupHandler`, `browser.RequestPrintHandler`,
  `network.SendUrlRequestHandler`. Assign
  `new Handler<TParameters, TResponse>(p => ...)` for a synchronous lambda or
  `new AsyncHandler<TParameters, TResponse>(async p => ...)` for an async one.
  An async handler must complete its `Task`, otherwise the engine waits for the
  response until termination.
- A handler property holds one handler. Assigning it again replaces the
  previous one, so combine all logic for one property (for example, blocking
  images *and* rewriting URLs in `SendUrlRequestHandler`) in a single handler.
- Before writing a handler, an event handler, or code that updates UI from
  either, read "How handlers run", "Events", and "Updating the UI from
  handlers and events" in `references/site/docs/guides/design/index.md`.
  They cover the threads handlers and events run on, thread safety, logged
  handler exceptions, non-blocking UI updates per framework, and the
  deadlock caused by blocking a handler on `Invoke`.
- `engine.Disposed` with `e.ExitCode != 0` means Chromium crashed. Do not
  rely on event order beyond what the API docs state.
- Before calling DotNetBrowser methods inside a handler, check that handler's
  API remarks in `references/api/`. Some handlers forbid calls to the browser
  or engine, even from the handler's own thread, for example
  `StartNavigationHandler`, `ShowHttpErrorPageHandler`, and
  `ShowNetErrorPageHandler`. Use the handler's parameters and response types
  to make the decision.
