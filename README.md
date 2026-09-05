# Copyslop

Agent skill for identifying and reducing unnecessary AI-generated UI copy slop.

## Examples

| Before | After | Decision |
| --- | --- | --- |
| Create a new backup | Create backup | Shorten |
| Your backup has been successfully created. | Backup created. | Shorten |
| Are you sure you want to permanently delete this backup? | Permanently delete this backup? | Shorten |
| Enjoy a seamless and intuitive experience designed to make every interaction feel effortless. Our thoughtfully crafted interface puts you in complete control, giving you the confidence to focus on what matters most while we take care of the details behind the scenes. | — | Delete |
| Our intelligent backup management system works tirelessly behind the scenes to keep your storage clean and organized, so you never have to worry about unnecessary clutter. Backups older than 30 days are automatically and permanently deleted, while your most recent backup is always kept to give you confidence and peace of mind. | Backups older than 30 days are automatically and permanently deleted, except the latest backup. | Rewrite |

## Install

Ask Codex or Claude Code:

```text
Install the copyslop skill from https://github.com/tinywaffles/Copyslop-skill.
```

Or use the GitHub CLI.

For Codex:

```sh
gh skill install tinywaffles/Copyslop-skill copyslop --agent codex --scope user
```

For Claude Code:

```sh
gh skill install tinywaffles/Copyslop-skill copyslop --agent claude-code --scope user
```

Remove `--scope user` to install into the current project. For a manual install, copy `copyslop/` into `~/.agents/skills/` for Codex or `~/.claude/skills/` for Claude Code.

Invoke `$copyslop` in Codex or `/copyslop` in Claude Code.

### Claude chat

Download the [Claude ZIP](https://github.com/tinywaffles/Copyslop-skill/releases/download/v1.0.1/copyslop.zip). In Claude, open **Customize > Skills**, select **+ > Create skill > Upload a skill**, upload the ZIP, and enable it. See [Claude's upload instructions](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

## Usage

By default, the skill returns a read-only `Previous | Decision | Output` review. To edit directly, explicitly ask it to skip the audit and make changes.

## License

MIT
