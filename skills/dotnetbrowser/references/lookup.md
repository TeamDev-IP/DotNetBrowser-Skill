# Looking up the API and guides

Paths are relative to the skill folder, the one that holds `SKILL.md`.

## API reference

`references/api/INDEX.md` lists every namespace, then every type by kind
(Classes, Interfaces, Enums) with a summary and its file. It is long: search
it for the type name rather than reading it whole. Conventions:

- Files are named by full type name: `DotNetBrowser.Browser.IBrowser.md`.
  Generic types use an arity suffix instead of `<...>`:
  `DotNetBrowser.Handlers.Handler-2.md` is `Handler<TParameters, TResponse>`.
  Nested types are dotted: `DotNetBrowser.Engine.EngineOptions.Builder.md`.
- Each file has the declaration, inheritance, then every property, method, and
  event with its signature. Remarks may still contain raw
  `<xref href="DotNetBrowser.X.Y">` tags: read them as a reference to type `Y`.
- Handler parameter and response types, and enums used only by them (for
  example `DotNetBrowser.Net.Handlers.ResourceType`), live in `*.Handlers`
  namespaces; event argument types in `*.Events` namespaces. Related types
  can sit in different namespaces: `RequestPrintParameters` is in
  `DotNetBrowser.Browser.Handlers`, `PrintHtmlContentParameters` in
  `DotNetBrowser.Print.Handlers`.
- Extension methods are documented on their `*Extensions` class, not on the
  extended type's page.
- Guide samples usually omit `using` directives. Take each type's namespace
  from `references/api/INDEX.md`.
- The API reference covers the engine and the WPF, Windows Forms, WinUI 3,
  and Avalonia UI 11 packages. **`DotNetBrowser.AvaloniaUi.v12` has no pages
  of its own:** use the Avalonia UI 11 pages. DotNetBrowser's API is the same
  in both packages; members that come from Avalonia UI, inherited or
  overridden (for example `BrowserView.OnGotFocus`), follow Avalonia UI 12.

## Guides and other site pages

`references/site/INDEX.md` has one table per section: Documentation (guides,
quick starts, tutorials, troubleshooting), Releases, Migration, Blogs, plus
live-only links (FAQ, Roadmap). Pages are the raw Markdown of the site:

- Links inside pages are mostly absolute. Resolve
  `https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#anchor` to
  `references/site/docs/guides/gs/engine/index.md`: drop the
  `https://teamdev.com/dotnetbrowser/` prefix and the fragment, and append
  `index.md`. A few links are relative to that site root
  (`docs/guides/...`); resolve them the same way. Resolve
  `https://api.dotnetbrowser.dev/<version>/api/DotNetBrowser.X.Y` to
  `references/api/DotNetBrowser.X.Y.md` when `<version>` is this skill's
  version (if that file does not exist, the last segment is a member: open
  the type's file and search for it). Links to other versions describe an
  older API. Prefer the bundled file; use the live URL only when it is not
  bundled.
- Pages that are not in `references/site/INDEX.md` (for example release notes
  older than 4.0) are not bundled; use the live URL.
- Images and diagrams are not included; `<div class="diagram-box">` blocks are
  empty. The surrounding text describes what they showed.
- Samples come in C# and VB.NET pairs; use whichever matches the project.
- Release notes are under `references/site/releases/`; a version newer than
  4.3.3 may exist online. Use the URLs in
  `references/site/llms.txt` (every page is also served as Markdown at that
  URL) when the user runs a newer version.

## Upgrading across several versions

There is no single guide. Apply every migration guide on the path in version
order (for example, from 2.27: `from-v2-to-v3`, `within-v3/v3-3-7-v3-4-0`,
`from-v3-to-v4`, `within-v4/v4-0-1-v4-1-0`, `within-v4/v4-1-1-v4-2-0`), and
read the release notes of every version on the path: some releases, such as
4.1.1, have breaking changes but no migration guide.
`references/site/INDEX.md` sorts migration guides as text, not by version.
Release notes older than 4.0 are not bundled; use the live URLs for them.
