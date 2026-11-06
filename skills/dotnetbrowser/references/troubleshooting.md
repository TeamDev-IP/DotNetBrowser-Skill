# Troubleshooting checklist

Paths are relative to the skill folder, the one that holds `SKILL.md`. Guide
pages below are under `references/site/docs/guides/`.

- Engine fails to start: check the exception type (`NoLicenseException`,
  `InvalidLicenseException`, `ChromiumBinariesMissingException`,
  `EngineInitializationException`) in `troubleshoot/common-exceptions/index.md`.
  Two engines must not share a `UserDataDirectory`, even across processes.
- Engine fails to start on Windows with `AutoDeElevationException`: the application
  runs with administrator rights, for example from a terminal opened as administrator
  or from Visual Studio running as administrator. In 4.3.5 and earlier, the same case
  throws the generic `EngineInitializationException: Failed to establish RPC connection
  to the Chromium engine.`, which has other causes too, so check whether the
  application runs elevated. See "Running as admin on Windows" in
  `troubleshoot/common-issues/index.md`: run without administrator rights, or add the
  `--do-not-de-elevate` switch. Windows services aren't affected.
- Blank or frozen `BrowserView`: confirm `InitializeFrom` ran on the UI thread
  after the control was created, and that no handler or event handler blocks
  on the UI thread (see `references/handlers-and-threading.md`). Check
  rendering-mode limitations for the framework in `gs/browser-view/index.md`.
- Application does not exit: the engine and browsers were not disposed.
- UI exception from an event: marshal to the UI thread (see
  `references/handlers-and-threading.md`).
- Anything else: enable logging (`LoggerProvider.Instance.Level`, file output
  per `troubleshoot/logging/index.md`) and read the log before guessing.
