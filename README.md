# Reducing UI Copy Slop

An Agent Skill for reviewing and reducing verbose, repetitive, promotional, and speculative interface copy while preserving useful guidance, safety, recovery, and accessibility.

## Install

For Codex:

```sh
gh skill install tinywaffles/reducing-ui-copy-slop reducing-ui-copy-slop --agent codex --scope user
```

For Claude Code:

```sh
gh skill install tinywaffles/reducing-ui-copy-slop reducing-ui-copy-slop --agent claude-code --scope user
```

Remove `--scope user` to install into the current project. For a manual install, copy `reducing-ui-copy-slop/` into `~/.agents/skills/` for Codex or `~/.claude/skills/` for Claude Code.

## Example

| Previous | Decision | Output |
| --- | --- | --- |
| Please wait while we load your settings. | Rewrite | Loading settings… |
| Your settings were successfully saved. | Shorten | Settings saved. |
| A task is already running. Wait for it to finish before starting another one. | Shorten | A task is already running. |
| Enter exact username... | Shorten | Enter username |
| Deleting this file is permanent and cannot be undone. | Rewrite | This permanently deletes the file. |
| The document could not be saved. | Rewrite | Failed to save. |

## License

MIT
