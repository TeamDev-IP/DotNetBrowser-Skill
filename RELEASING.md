# Releasing a new skill version

Each DotNetBrowser release ships its own copy of the skill. Update this
repository after every release so it always holds the latest one.

1. Download the archive for the new version:

   ```text
   https://teamdev.download/downloads/dotnetbrowser/<version>/dotnetbrowser-<version>-agent-skill.zip
   ```

2. Delete `skills/dotnetbrowser/` and replace it with the `dotnetbrowser` folder
   from the archive. Copy it unchanged; don't edit files inside it by hand.

3. Bump the version to `<version>` in:
   - `.claude-plugin/plugin.json`: `version` and `description`
   - `.claude-plugin/marketplace.json`: `version` and `description`
   - `README.md`: the "DotNetBrowser x.y.z" mention

   Clients only receive an update when `version` changes. For a fix to this
   repository without a new DotNetBrowser release, use a suffix such as
   `4.3.3-1`.

4. Validate:

   ```bash
   claude plugin validate .
   ```

5. Commit and merge to `main`. The Claude directory picks up the new commit,
   scans it, and the new version is published from the
   [developer portal](https://claude.ai/directory/manage). skills.sh serves the
   `main` branch directly.

## Directory limits to keep in mind

- Every non-image file must stay under 256 KiB.
- The plugin has more than 512 files, so each version is held for a reviewer
  before it goes live. This is expected.
- Don't commit `.DS_Store`, `Thumbs.db`, `desktop.ini`, `__MACOSX`, symbolic
  links, Git LFS files, or `filter`/`export-ignore` rules in `.gitattributes`;
  the directory rejects them.
