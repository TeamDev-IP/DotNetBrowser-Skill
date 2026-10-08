
# Installing the agent skill

**Lead**
This guide describes how to add the DotNetBrowser agent skill to your project,
so that AI coding agents can look up the DotNetBrowser API and documentation.


An AI coding agent without information about the DotNetBrowser API guesses type
and member names from its training data, which may come from older versions.
The DotNetBrowser agent skill gives the agent this information. It is a folder
in the [Agent Skills][docs-agent-skills] format that contains:

* instructions on how to write code with DotNetBrowser;
* the API reference;
* an offline copy of the DotNetBrowser documentation, release notes, and
  migration guides.

Each DotNetBrowser release has its own skill, so the API reference matches the
version you build against. The agent reads the skill on its own when a task
involves DotNetBrowser.

The skill is installed in the `dotnetbrowser` subdirectory of the agent's
skills directory:

| Agent | Skills directory in the project |
| --- | --- |
| Claude Code | `.claude/skills/` |
| Codex | `.agents/skills/` |
| Cursor | `.cursor/skills/` |
| GitHub Copilot | `.github/skills/` |

Agents look for skills in the repository root, and some also in the directory
where you start them.

You can install the skill in three ways:

* from NuGet, in an existing project;
* from a ZIP archive, copied into a project or into your home directory;
* with a project template, in a new project.

## Installing in an existing project

### From NuGet

The `DotNetBrowser.AgentSkills` package installs the skill when you build the
project. It adds no assemblies or runtime dependencies to your application.

In the project directory, add the package with the same version as your
DotNetBrowser packages:

```bash
dotnet add package DotNetBrowser.AgentSkills --version <version>
```

Replace `<version>` with the version of your DotNetBrowser packages, for
example `4.3.3`. The command adds the package with
`PrivateAssets="all"`, so it does not flow to projects that reference yours.
In Visual Studio, you can add the package with the NuGet Package Manager
instead, as described in [Installing from NuGet][guides-nuget]. This also works
in .NET Framework projects that use `packages.config`.

Then set the `DotNetBrowserAgentSkillsAgent` property to your agent in the
project file:

| Agent | Value |
| --- | --- |
| Claude Code | `ClaudeCode` |
| Codex | `Codex` |
| Cursor | `Cursor` |
| GitHub Copilot | `Copilot` |

```xml
<PropertyGroup>
  <DotNetBrowserAgentSkillsAgent>ClaudeCode</DotNetBrowserAgentSkillsAgent>
</PropertyGroup>
```

Instead of running `dotnet add package`, you can add the package reference
and the property to the project file in one step. Put the version of your
DotNetBrowser packages in place of `...`:

```xml
<PropertyGroup>
  <DotNetBrowserAgentSkillsAgent>ClaudeCode</DotNetBrowserAgentSkillsAgent>
</PropertyGroup>
<ItemGroup>
  <PackageReference Include="DotNetBrowser.AgentSkills"
                    Version="..."
                    PrivateAssets="all" />
</ItemGroup>
```

When you build the project, the skill is installed in the agent's skills
directory in the project directory. This normally happens before the code is
compiled, so the skill is there even when the code does not compile. The build
installs the skill again when the package has a different version of it, or
when files are missing from or added to the installed directory.

If the project is not in the repository root, set the skills directory with
the `DotNetBrowserAgentSkillsDirectory` property instead. This is the case for
a project created in Visual Studio, which puts the project in a subdirectory of
the solution by default. For example, for a project one level below the
repository root:

```xml
<PropertyGroup>
  <DotNetBrowserAgentSkillsDirectory>..\.claude\skills</DotNetBrowserAgentSkillsDirectory>
</PropertyGroup>
```

Set the skills directory itself, not its `dotnetbrowser` subdirectory. A
relative path is resolved from the project directory. When both properties are
set, the skills directory is used. Also use this property for an agent that is
not in the table, with the skills directory from the agent's documentation.

MSBuild does not expand `~`. For a skills directory in your home directory,
start the path with `$(UserProfile)` on Windows or `$(HOME)` on Linux and
macOS.

To install the skill without building the project, run:

```bash
dotnet msbuild <project_file> -restore -t:InstallDotNetBrowserAgentSkills
```

Replace `<project_file>` with the path to your project file. If the .NET SDK
is not installed, run the same command with `msbuild` instead of
`dotnet msbuild`, for example in the Developer Command Prompt for Visual
Studio. If neither property is set, the command installs the skill in
`.agents/skills/dotnetbrowser/` in the project directory. In a project that
uses `packages.config`, `-restore` does not restore the package, so restore it
in Visual Studio first.

Keep in mind:

* The installation requires MSBuild 16 (Visual Studio 2019) or later.
* When several projects share one skills directory, set the property in one of
  them only, not in `Directory.Build.props`. Installations from projects that
  build at the same time are not synchronized.
* A project with several target frameworks installs the skill only when you
  build it for all of them. Building one framework, for example with
  `dotnet build -f net8.0`, does not install the skill. Neither does a project
  that sets `TargetFramework` while it inherits `TargetFrameworks`, for example
  from `Directory.Build.props`. Clear `TargetFrameworks` in that project or run
  the command above.
* In a static graph build (`-graphBuild`), a project with several target
  frameworks installs the skill after the code is compiled.
* Visual Studio skips building a project that it considers up to date, so it
  does not check the installed skill either. Run the command above to restore
  missing files right away.
* The package replaces only a directory that it installed itself. If the
  skills directory already has a `dotnetbrowser` folder copied from the ZIP,
  delete it before the first build, or the build fails.

### From ZIP

[Download the DotNetBrowser 4.3.3 agent skill][docs-skill-zip]
and unpack it. The archive contains the `dotnetbrowser` folder.

Copy this folder, as is, into the agent's skills directory in the repository
root. To use the skill in all projects, copy it into the skills directory in
your home directory instead: `~/.claude/skills/` for Claude Code,
`~/.agents/skills/` for Codex, or `~/.cursor/skills/` for Cursor.

For an agent that does not read the Agent Skills format, keep the folder
anywhere in the repository and reference `dotnetbrowser/SKILL.md` from the
agent's rules or instructions file.

## Creating a project with the skill

The DotNetBrowser project templates add the skill with the `--agent` option:

```bash
dotnet new dotnetbrowser.console.app -o Example.Console --agent ClaudeCode
```

The option accepts `ClaudeCode`, `Codex`, `Cursor`, or `Copilot`. In Visual
Studio, choose the agent in the **AI coding agent** field when you create the
project. The template adds the `DotNetBrowser.AgentSkills` package and the
`DotNetBrowserAgentSkillsAgent` property to the project, so the skill is
installed when you build it, as described [above][guides-from-nuget].

Visual Studio creates the project in a subdirectory of the solution by
default, so the skill is installed there, not in the solution directory. If
you start the agent in the solution directory, set the
`DotNetBrowserAgentSkillsDirectory` property to the skills directory in the
solution directory, for example `..\.claude\skills`.

A project created this way uses the package, so the NuGet instructions below
for updating, version control, and removing apply to it.

See the [quick start guides][guides-quickstart] for creating a project from a
template.

## Updating

If you installed the skill from NuGet, update the `DotNetBrowser.AgentSkills`
package together with the DotNetBrowser packages and build the project. Each
installation replaces the whole `dotnetbrowser` directory, so do not keep your
own files there. If you changed a file in the installed skill by mistake, the
build does not notice. Run the [install command][guides-from-nuget] to
restore the skill.

If you installed the skill from ZIP, replace the whole `dotnetbrowser` folder
with the one from the new archive.

## Version control

If you installed the skill from NuGet, add the installed `dotnetbrowser`
directory to `.gitignore`, because the package installs it again on build.
Keep the hidden `.dotnetbrowser-agent-skill` file in that directory: without
it, the package does not replace the directory.

## Removing

To remove a skill installed from NuGet, remove the package reference and the
property from the project, then delete the installed `dotnetbrowser`
directory. To remove a skill installed from ZIP, delete the `dotnetbrowser`
folder.

[docs-agent-skills]: https://agentskills.io
[docs-skill-zip]: https://teamdev.download/downloads/dotnetbrowser/4.3.3/dotnetbrowser-4.3.3-agent-skill.zip
[guides-from-nuget]: #from-nuget
[guides-nuget]: https://teamdev.com/dotnetbrowser/docs/guides/installation/nuget/
[guides-quickstart]: https://teamdev.com/dotnetbrowser/docs/quickstart/
