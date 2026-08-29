# Reducing UI Copy Slop

An Agent Skill for removing verbose, repetitive, promotional, and speculative interface copy while preserving useful guidance, safety, recovery, and accessibility.

## Install

With GitHub CLI:

```sh
gh skill install tinywaffles/reducing-ui-copy-slop reducing-ui-copy-slop
```

Or copy `reducing-ui-copy-slop/` into your personal or project skills directory, such as `~/.agents/skills/` or `.agents/skills/`.

## Use

```text
Use $reducing-ui-copy-slop to audit the copy in this interface.
```

The skill asks whether each string performs a unique job, then returns **Keep**, **Shorten**, or **Delete**. It also prevents copy work from quietly inventing product behavior just to make a UI feel more complete.

## Design basis

The structure follows the [Agent Skills specification](https://agentskills.io/specification), [OpenAI skill-authoring guidance](https://github.com/openai/skills/blob/main/skills/.system/skill-creator/SKILL.md), and [Anthropic's evaluation-first authoring guidance](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices). Its copy decisions draw from Impeccable's [Clarify](https://github.com/pbakaus/impeccable/blob/main/.agents/skills/impeccable/reference/clarify.md) and [Distill](https://github.com/pbakaus/impeccable/blob/main/.agents/skills/impeccable/reference/distill.md) approaches, narrowed specifically to UI copy.

## License

MIT
