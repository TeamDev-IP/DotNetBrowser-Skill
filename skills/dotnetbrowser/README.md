# DotNetBrowser agent skill

This folder is an [Agent Skill](https://agentskills.io): `SKILL.md` tells an AI
coding agent how to work with DotNetBrowser, and `references/` holds topic
notes, the API references, and an offline copy of the documentation, release
notes, migration guides, and blog for the version named in `SKILL.md`. See
[references/lookup.md](references/lookup.md) for reference coverage.

## Installing

Copy this `dotnetbrowser` folder, as is, into the skills directory of your
agent. The agent reads `SKILL.md` on its own when a task involves DotNetBrowser.

| Agent | Where to put the folder |
| --- | --- |
| Claude Code | `.claude/skills/dotnetbrowser/` in the project, or `~/.claude/skills/dotnetbrowser/` for every project |
| OpenAI Codex | `.agents/skills/dotnetbrowser/` in the project, or `~/.agents/skills/dotnetbrowser/` for every project |
| Cursor | `.cursor/skills/dotnetbrowser/` in the project, or `~/.cursor/skills/dotnetbrowser/` for every project |
| GitHub Copilot | `.github/skills/dotnetbrowser/` in the project |
| Other agents | Keep the folder anywhere in the repository and reference `SKILL.md` from your rules or instructions file |

Check your agent's documentation for the current skills location; the layout
above follows the Agent Skills convention that all of them read.

The skill is also available as the `DotNetBrowser.AgentSkills` NuGet package.
Add it to your project and set the `DotNetBrowserAgentSkillsAgent` property to
`ClaudeCode`, `Codex`, `Cursor`, or `Copilot`, or the
`DotNetBrowserAgentSkillsDirectory` property to your agent's skills directory;
the skill is then installed when you build the project. The package README on
nuget.org describes the details and how to install the skill without building.

## Updating

Each DotNetBrowser release ships a new copy of this skill. Replace the whole
folder when you upgrade the NuGet packages, so the API reference matches the
version you build against. If you installed the skill with the
`DotNetBrowser.AgentSkills` package, update the package instead of replacing
the folder.
