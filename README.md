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
| Initializing environment variables for your personalized workspace... | Rewrite | Preparing environment… |
| Please wait while we securely establish your connection. | Rewrite | Connecting… |
| Your profile settings have been successfully updated. | Shorten | Profile settings updated. |
| An unexpected error occurred while attempting to process your request. | Rewrite | Request failed. |
| A task is currently in progress. Please wait patiently for it to complete before starting another one. | Rewrite | A task is already running. |
| Please enter your exact username in the field below... | Shorten | Enter username |
| Deleting this file is a permanent action that cannot be undone. | Rewrite | This permanently deletes the file. |

## License

MIT
