# Troubleshooting checklist

Paths are relative to the skill folder, the one that holds `SKILL.md`. Guide
pages below are under `references/site/docs/guides/`.

- Engine fails to start: check the exception type (`NoLicenseException`,
  `InvalidLicenseException`, `ChromiumBinariesMissingException`,
  `EngineInitializationException`) in `troubleshoot/common-exceptions/index.md`.
  Two engines must not share a `UserDataDirectory`, even across processes.
- Blank or frozen `BrowserView`: confirm `InitializeFrom` ran on the UI thread
  after the control was created, and that no handler or event handler blocks
  on the UI thread (see `references/handlers-and-threading.md`). Check
  rendering-mode limitations for the framework in `gs/browser-view/index.md`.
- Application does not exit: the engine and browsers were not disposed.
- UI exception from an event: marshal to the UI thread (see
  `references/handlers-and-threading.md`).
- Anything else: enable logging (`LoggerProvider.Instance.Level`, file output
  per `troubleshoot/logging/index.md`) and read the log before guessing.
