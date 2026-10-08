
# Migrating from 2.17 to 2.18

## Updated API

### Navigation

The `LoadResult` is replaced with `NavigationResult` which contains more details about the possible navigation failure.

**v2.17**

```csharp
LoadResult result = await browser.Navigation.LoadUrl(“example.com”);
if (result == LoadResult.Completed)
{
    // The web page has loaded successfully, process its contents.
}
```

**v2.18**

```csharp
NavigationResult result = await browser.Navigation.LoadUrl(“example.com”);
if (result.LoadResult == LoadResult.Completed)
{
    // The web page has loaded successfully, process its contents.
}
```
