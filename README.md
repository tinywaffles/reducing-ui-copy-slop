# Reducing UI Copy Slop

An Agent Skill for removing verbose, repetitive, promotional, and speculative interface copy while preserving useful guidance, safety, recovery, and accessibility.

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

| Example | What | Result |
| --- | --- | --- |
| Safeguard your precious worlds effortlessly with powerful automated backup protection. | Delete | — |
| Create a new backup now | Shorten | Create backup |
| The document could not be saved. | Rewrite | Failed to save. |
| Your backup was successfully created and is now safely stored. | Shorten | Backup created. |

## Design basis

The structure follows the [Agent Skills specification](https://agentskills.io/specification), [OpenAI skill-authoring guidance](https://learn.chatgpt.com/docs/build-skills), and [Anthropic's skill-authoring guidance](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices). Its copy decisions draw from Impeccable's [Clarify](https://github.com/pbakaus/impeccable/blob/main/.agents/skills/impeccable/reference/clarify.md) and [Distill](https://github.com/pbakaus/impeccable/blob/main/.agents/skills/impeccable/reference/distill.md) approaches, narrowed specifically to UI copy.

## License

MIT
