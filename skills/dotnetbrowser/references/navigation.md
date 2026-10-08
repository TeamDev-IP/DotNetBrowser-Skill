# Navigation results

Paths are relative to the skill folder, the one that holds `SKILL.md`.

- Before loading a page or deciding whether it loaded, read "Navigation
  result" in the guide: `LoadUrl()` completes even when the page failed or
  was stopped, so always check `LoadResult`, and `Completed` means only that
  the main frame fired its `load` event. It does not mean that content added
  by scripts is there, that HTTP succeeded (HTTP 4xx/5xx pages with server
  HTML are `Completed`; check `NavigationFinished.ResponseCode`), or that the
  page will not replace itself with a client-side redirect. Do not block on
  the task (`.Result`, `Wait()`) on the UI thread.
- Before handling navigation events, read "Navigation events" and "Common
  mistakes": no event means "page ready", `LoadFinished` covers the whole
  browser and fires several times, `FrameLoadFinished` fires per frame and
  again for each new document, and handler order is not guaranteed.
- Before using page content after a load, a click, or a form submission,
  read "Waiting for page content" and "After a click or a form submission":
  wait for the element you need, with a timeout, and restart the wait if the
  page loads a new document.
- Before tracking a navigation's status from events, read "Tracking the
  navigation status": use only main-frame events, check `HasCommitted`, keep
  a reported failure across later events, and for navigations the app starts
  use the task returned by `LoadUrl()`.
- When the app fills in and submits a login form by script in a
  `BrowserView`, the view's default `SavePasswordHandler` shows a "Save
  password?" prompt. To suppress it, set `browser.Passwords.SavePasswordHandler`
  to a handler that returns `SavePasswordResponse.Ignore`, or `NeverSave` to
  stop prompts for that site.

The guide is `references/site/docs/guides/gs/navigation/index.md`.
