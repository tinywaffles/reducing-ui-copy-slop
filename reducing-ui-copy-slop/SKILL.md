---
name: reducing-ui-copy-slop
description: Cuts verbose, repetitive, promotional, vague, speculative, or reassuring product UI copy without losing meaning, safety, recovery, or accessibility. Use for labels, helper text, buttons, dialogs, empty states, errors, success messages, and UI-copy examples in documentation; not marketing, visual design, or unrelated prose.
license: MIT
---

# Reducing UI Copy Slop

## Rule

Use the shortest wording that keeps meaning. Prefer concrete states and outcomes to narration. Keep labels grammatical with their values and use one term per concept. Treat layout, controls, state, and nearby copy as context. Keep domain terms unless redundant. Ignore punctuation-only edits unless asked. Invent nothing.

## Scope

Read the brief, component, interaction, and nearby copy. Separate facts from assumptions. Requests for *polished*, *premium*, *friendly*, *helpful*, or *finished* UI do not authorize extra UI.

Do not invent controls, states, metrics, progress, guarantees, confirmations, tooltips, or behavior. Verify specific claims. List `Open product facts` only when needed for accurate copy.

## Decide

Each string must identify an object or state, or communicate an outcome, constraint, consequence, recovery, instruction, or accessible name.

- **Delete** if it has no unique job or repeats nearby copy.
- **Shorten** by deleting padding.
- **Rewrite** unclear or misleading copy using verified facts only.
- **Keep** if removal harms understanding, recovery, safety, or accessibility.

Audit changed copy only. Each finding has original copy, decision, and result; add location only when identical strings differ. Adapt labels to the task. Omit preambles, summaries, and routine reasons. Apply requested edits.

In docs examples, cut setup or reasons that only justify **Delete** or **Shorten**. Keep consequences, safety facts, and context needed for accuracy. Keep agent and implementation reasoning out of UI copy.

## Quick Reference

| Element | Rule |
| --- | --- |
| Button | Name the outcome. Add the object only for context or precise confirmation. |
| Helper | Add only a constraint, consequence, format, or useful example. |
| Success | State the outcome once. Cut reassurance and internal claims such as “safely stored”; keep needed safety facts. |
| Error | Delete failure already stated nearby. Otherwise state what failed naturally. Keep a code only when it helps the user, support, or recovery; never make it the primary message. Add only a known useful cause or existing recovery. |
| Empty state | State the condition. Add a known reason or existing action only if useful. |
| Destructive action | Name the object and keep the irreversible consequence. |
| Disabled control | State why it is unavailable. Add no instruction when the user cannot act. |
| Link or icon-only control | Use an accessible name that makes sense without nearby copy. |

## Example

| Example | Type | Result |
| --- | --- | --- |
| Safeguard your precious worlds effortlessly with powerful automated backup protection. | Delete | — |
| Create a new backup now | Shorten | Create backup |
| The document could not be saved. | Rewrite | Failed to save. |
| Your backup was successfully created and is now safely stored. | Shorten | Backup created. |

## Avoid

- Rewriting copy that should be deleted.
- Treating “all copy” as all possible states, or extracted strings, word lists, or pattern hits as proof of slop.
- Removing safety, recovery, disabled reasons, or accessible names.
- Adding reassurance, assumptions, internal reasoning, or style-only rewrites.
- Editing unrelated documentation.

## Check

Check format, one verified job per string, and safe deletions. Drop unchanged rows. Mark word or order changes **Rewrite**, not **Shorten**. Show **Keep** only when requested, repeating the copy. With UI, test width, dynamic values, and accessible names. Keep scope.
