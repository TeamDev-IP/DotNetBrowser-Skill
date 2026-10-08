# JavaScript

Paths are relative to the skill folder, the one that holds `SKILL.md`.

- `frame.Document` is the `IDocument` (DOM); `frame.ExecuteJavaScript<T>(js)`
  returns `Task<T>`. Injecting a .NET object into the page is
  `window.Properties["MyObject"] = new MyObject()` on the `IJsObject` for
  `window`; its public methods are then callable from JavaScript.
- Before choosing the `T` of `ExecuteJavaScript<T>` or handling script
  errors, read "Executing JavaScript" and "Type conversion" in the guide: the
  method casts rather than converts, JavaScript numbers become `double`, and
  a script that throws gives `null` (or, for a non-nullable value type `T`,
  `NullReferenceException`) instead of a JavaScript exception. To observe a
  thrown JavaScript error, use `IJsFunction.Invoke` or `InvokeAsync`, which
  report `JsException`; see `references/api/DotNetBrowser.Js.IJsFunction.md`.

The guide is `references/site/docs/guides/gs/javascript/index.md`.
