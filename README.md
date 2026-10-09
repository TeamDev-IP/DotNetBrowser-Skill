# DotNetBrowser skill for AI coding agents

[![skills.sh](https://skills.sh/b/TeamDev-IP/DotNetBrowser-Skill)](https://skills.sh/TeamDev-IP/DotNetBrowser-Skill)
[![Security: A — Skills Directory](https://www.skillsdirectory.com/api/skills/teamdev-ip-dotnetbrowser/badge)](https://www.skillsdirectory.com/skills/teamdev-ip-dotnetbrowser)

The official [Agent Skill](https://agentskills.io) for
[DotNetBrowser](https://teamdev.com/dotnetbrowser), TeamDev's Chromium-based
browser component for .NET applications built with WPF, Windows Forms, WinUI 3,
Avalonia UI, or as console apps.

The skill teaches Claude and other coding agents how to write, review, and debug
DotNetBrowser code: choosing NuGet packages, engine and browser lifecycle,
`BrowserView`, handlers and events, navigation, DOM access, the JavaScript bridge,
printing, network interception, deployment, and licensing. It bundles the full
API reference and an offline copy of the guides, release notes, migration guides,
and blog for **DotNetBrowser 4.3.3**, so the agent answers from documentation that
matches the version rather than from memory.

## Install

### Claude (claude.ai, Cowork, Claude Code)

Find **DotNetBrowser** in the [Claude directory](https://claude.ai/directory) and
add it. In Claude Code, you can also install it from this repository:

```text
/plugin marketplace add TeamDev-IP/DotNetBrowser-Skill
/plugin install dotnetbrowser@teamdev-dotnetbrowser
```

### Other agents (Codex, Cursor, GitHub Copilot, and more)

Install with the [skills](https://skills.sh) CLI:

```bash
npx skills add TeamDev-IP/DotNetBrowser-Skill
```

### Pinned to your DotNetBrowser version

This repository tracks the latest DotNetBrowser release. To get the skill that
matches the exact version your project builds against, use the
`DotNetBrowser.AgentSkills` NuGet package or the per-release ZIP archive described
in the [installation guide](https://teamdev.com/dotnetbrowser/docs/guides/installation/agent-skill/).

## Use

Ask your agent about a DotNetBrowser task, for example "Show a login page in a
WPF window and fill in the form from C#" or "Intercept requests to our API and
add a header". The agent loads the skill on its own when a task involves
DotNetBrowser. In Claude Code you can also invoke it directly with
`/dotnetbrowser:dotnetbrowser`.

## Data and behavior

The skill consists of Markdown files only. It contains no scripts, hooks, or MCP
servers, runs nothing, and sends no data anywhere. Some reference pages include
links to the live DotNetBrowser documentation, which the agent may open if it
needs a newer page.

## License

The contents of this repository are provided under the
[TeamDev terms](https://www.teamdev.com/terms-and-privacy). See [LICENSE](LICENSE).

DotNetBrowser itself is a commercial library and requires a license key. A free
30-day evaluation license is available at
https://www.teamdev.com/dotnetbrowser#evaluate.
