# Copyslop

Copyslop is an Agent Skill for reviewing and reducing verbose, repetitive, promotional, and speculative interface copy while preserving useful guidance, safety, recovery, and accessibility.

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

Invoke `$copyslop` in Codex or `/copyslop` in Claude Code. Both use the same skill instructions.

### Claude chat

Download [copyslop.zip](copyslop.zip). In Claude, open **Customize > Skills**, select **+ > Create skill > Upload a skill**, upload the ZIP, and enable it. See [Claude's upload instructions](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

The ZIP contains `copyslop/SKILL.md`, Codex UI metadata, and the MIT license. Supply the relevant copy and nearby interaction context in chat; missing product facts remain open questions. Claude chat cannot inspect a local repository unless you provide access or its relevant contents.

To rebuild the ZIP from the repository root with PowerShell:

```powershell
Compress-Archive -LiteralPath ./copyslop -DestinationPath ./copyslop.zip -Force
```

## Review and approval

The first pass is read-only and returns a `Previous | Decision | Output` table. Approve all changes or identify the rows to apply; rejection changes nothing, and feedback stays read-only until fresh approval. `Location` identifies ambiguous occurrences. Matching `Group` values identify changes that must be approved together, such as moving a helper's fact into its label.

Missing facts appear under `Open product facts` while independent proposals remain available. `No copy changes.` means the requested audit found neither changes nor unresolved facts.

See the [contextual examples](copyslop/SKILL.md#examples) and [regression checks](TESTS.md).

## License

MIT
