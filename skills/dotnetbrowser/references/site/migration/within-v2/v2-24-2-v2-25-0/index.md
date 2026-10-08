
# Migrating from 2.24.2 to 2.25.0

## Updated API

### OpenFileHandler parameters

Due to changes in Chromium, the `OpenFileHandler` parameters no longer contain the `DefaultFileName` property. Instead, the `InitialDirectory` property was added, containing the initial directory that the file dialog box should display.

**v2.24.2**

```csharp
browser.Dialogs.OpenFileHandler =
    new Handler<OpenFileParameters, OpenFileResponse>(parameters =>
    {
        // The default file name.
        string defaultFileName = parameters.DefaultFileName;
        // The given file should be opened.
        return OpenFileResponse.SelectFile(Path.GetFullPath("<path-to-selected-file>"));
    });
```

**v2.25.0**

```csharp
browser.Dialogs.OpenFileHandler =
    new Handler<OpenFileParameters, OpenFileResponse>(parameters =>
    {
        // The suggested directory.
        string initialDirectory = parameters.InitialDirectory;
        // The given file should be opened.
        return OpenFileResponse.SelectFile(Path.GetFullPath("<path-to-selected-file>"));
    });
```
