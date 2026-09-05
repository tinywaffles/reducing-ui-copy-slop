# Copyslop

Copyslop reviews interface copy and proposes clearer wording while preserving meaning, safety, recovery, and accessibility.

## Install

For Codex:

```sh
gh skill install tinywaffles/reducing-ui-copy-slop copyslop --agent codex --scope user
```

For Claude Code:

```sh
gh skill install tinywaffles/reducing-ui-copy-slop copyslop --agent claude-code --scope user
```

Remove `--scope user` to install into the current project. For a manual install, copy `copyslop/` into `~/.agents/skills/` for Codex or `~/.claude/skills/` for Claude Code.

Invoke `$copyslop` in Codex or `/copyslop` in Claude Code.

### Claude chat

Download the [Claude ZIP](https://github.com/tinywaffles/reducing-ui-copy-slop/releases/download/v1.0.1/copyslop.zip). In Claude, open **Customize > Skills**, select **+ > Create skill > Upload a skill**, upload the ZIP, and enable it. See [Claude's upload instructions](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

Share the relevant copy in chat and explain how the surrounding interface works. Claude chat cannot inspect a local repository unless you provide access or its relevant contents.

To rebuild the ZIP from the repository root with PowerShell:

```powershell
Compress-Archive -LiteralPath ./copyslop -DestinationPath ./copyslop.zip -Force
```

## Review and approval

By default, the skill returns a read-only `Previous | Decision | Output` review. To edit directly, explicitly ask it to skip the audit and make changes.

After a review, approve all changes or identify the rows to apply; rejection changes nothing, and feedback stays read-only until fresh approval. `Location` identifies ambiguous occurrences. Rows with the same `Group` must be approved together.

Questions appear under `Open product facts`; other proposals can still be approved. `No copy changes.` means there are no proposed edits or unanswered product questions.

See the [contextual examples](copyslop/SKILL.md#examples) and [regression checks](TESTS.md).

## License

MIT
