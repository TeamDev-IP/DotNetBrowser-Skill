# Engine, profiles, and browsers

Paths are relative to the skill folder, the one that holds `SKILL.md`.

Namespaces: `DotNetBrowser.Engine`, `DotNetBrowser.Browser`,
`DotNetBrowser.Navigation`, `DotNetBrowser.Frames`, `DotNetBrowser.Dom`,
`DotNetBrowser.Js`, `DotNetBrowser.Handlers`, `DotNetBrowser.Net`,
`DotNetBrowser.Print`, `DotNetBrowser.Profile`, and the UI namespaces
`DotNetBrowser.Wpf`, `DotNetBrowser.WinForms`, `DotNetBrowser.WinUi3`,
`DotNetBrowser.AvaloniaUi`.

## Creating

- `IEngine` is the root object. `EngineFactory.Create()`,
  `EngineFactory.Create(EngineOptions)`, or
  `EngineFactory.Create(RenderingMode)` starts the Chromium main process and
  blocks until it is ready, which can take a few seconds;
  `EngineFactory.CreateAsync(...)` has the same overloads and returns
  `Task<IEngine>`. Options come from `new EngineOptions.Builder { ... }.Build()`.
  The engine may be created on any thread, including the UI thread. The
  samples create it synchronously in the window constructor because the code
  is shorter; the UI is unresponsive only while the engine starts. Use
  `CreateAsync` when that pause matters, and then handle the window being
  closed before the task completes: dispose the engine when it arrives, in
  code that does not need the UI thread (for example, a `ContinueWith`
  continuation). Code after `await` on the UI thread may never run: once the
  last window closes, WPF shuts down its dispatcher by default, and WinUI 3
  stops the window thread's message loop (see `references/browser-view.md`).
  An undisposed engine keeps the process alive. In this case no browser exists
  yet, so dispose only the engine, and do not wait for the UI thread first.
- The engine's rendering mode is the default for its browsers; to use another
  mode for one browser, see "Rendering" in
  `references/site/docs/guides/gs/browser-view/index.md`.
- Each engine has a default `IProfile` (`engine.Profiles.Default`). Profile
  services such as `Network`, `Proxy`, `CookieStore`, and `SpellChecker`
  hang off the profile, for example `engine.Profiles.Default.Network`.
  Handlers and events set on a profile service apply to every browser of that
  profile; browsers of another profile need their own.
- `IBrowser` is created with `engine.Profiles.Default.CreateBrowser()` or
  `profile.CreateBrowser()`; the guides recommend this over the equivalent
  `engine.CreateBrowser()`. It is not a visual control.
- Methods that return `Task<T>` run asynchronously; methods that return a value
  block until Chromium answers. The library is thread safe.

## Disposing

- Decide how to clean up an object by its interfaces, not by its name. A type
  that implements `IDisposable` - for example `IEngine`, `IBrowser`, and the
  capture `DotNetBrowser.Capture.ISession` - is owned by the code that
  created it; call `Dispose()` on it explicitly. Dependent service objects
  that implement only `IAutoDisposable` (`IProfile`, `INetwork`,
  `IBrowserSettings`, `IFrame`, and others) have no `Dispose()` method and are
  disposed automatically together with their owner: disposing the engine
  disposes its browsers; disposing a browser disposes its frames; a page
  unload can dispose its frames. An `IFrame` can also survive a navigation
  while the DOM and JavaScript objects of the previous document are
  disposed, so get `frame.Document` and other DOM or JavaScript objects again
  after each navigation. Do not generate a `Dispose()` call for an
  `IAutoDisposable`-only object; check `IsDisposed` or the `Disposed` event
  instead. When unsure, check the type's interfaces in `references/api/`.
  Using a disposed object throws `ObjectDisposedException`; a closed engine
  connection throws `ConnectionClosedException`.
- Dispose browsers and the engine as soon as they are no longer needed. Each
  engine runs its own Chromium processes; an engine or browser left
  undisposed keeps those processes alive and can prevent the application from
  exiting.
