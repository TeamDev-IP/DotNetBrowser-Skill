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
   - `.claude-plugin/marketplace.json`: `description` (the version is set only
     in `plugin.json`)
   - `README.md`: the "DotNetBrowser x.y.z" mention

   Clients only receive an update when `version` changes. For a fix to this
   repository without a new DotNetBrowser release, use a suffix such as
   `4.3.3-1`.

4. Validate:

   ```bash
   claude plugin validate .
   ```

   The `Check` workflow runs on every pull request, on `main`, and on tags. It
   validates the plugin, checks the directory limits below, and checks that
   the version matches in every place listed in step 3, in `SKILL.md`, and in
   the tag.

5. Commit, merge to `main`, and tag the commit with the version:

   ```bash
   git tag -a v<version> -m "DotNetBrowser <version> agent skill"
   git push origin v<version>
   ```

   The Claude directory picks up the new commit,
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
