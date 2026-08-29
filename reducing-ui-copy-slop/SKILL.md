---
name: reducing-ui-copy-slop
description: Cuts verbose, repetitive, promotional, vague, speculative, or reassuring product UI copy without losing meaning, safety, recovery, or accessibility. Use for labels, helper text, buttons, dialogs, empty states, errors, success messages, and UI-copy examples in documentation; not marketing, visual design, or unrelated prose.
license: MIT
---

# Reducing UI Copy Slop

## Rule

Use the shortest wording that keeps meaning. Count layout, labels, values, controls, state, and nearby text as information. Keep domain terms unless context makes them redundant. Ignore punctuation-only edits unless asked. Cover required elements; add no plausible ones.

## Scope

Read the brief, component, interaction, and nearby copy. Separate facts from assumptions. *Polished*, *premium*, *friendly*, *helpful*, or *finished* UI does not authorize extra UI.

Do not invent controls, states, metrics, progress, guarantees, confirmations, tooltips, or behavior. Specific claims require verified behavior. List `Open product facts` only when a missing fact blocks accurate copy.

## Decide

Each string must identify an object or state, name an outcome, state a constraint or consequence, explain recovery, instruct, or provide an accessible name.

- **Delete** if it has no unique job or repeats nearby copy.
- **Shorten** by deleting padding.
- **Rewrite** unclear or misleading copy using verified facts only.
- **Keep** if removal harms understanding, recovery, safety, or accessibility.

Audit changed copy only. Each unique finding contains only original copy, decision, and final copy; add location solely when identical strings need different decisions. Fit labels and layout to the task; omit preambles, summaries, and routine reasons. Apply requested file edits.

For docs examples, remove setup or reasons that only justify **Delete** or **Shorten**, including nearby headings, controls, or values. Keep stated consequences, safety facts, and context needed to avoid a misleading result. Never put agent or implementation reasoning in UI copy.

## Quick Reference

| Element | Rule |
| --- | --- |
| Button | Name the outcome. Add the object only if context is unclear or confirmation needs precision. |
| Helper | Add only a constraint, consequence, format, or non-obvious example. |
| Success | State the outcome once. Cut reassurance and internal claims such as “safely stored”; keep needed verified safety facts. |
| Error | State the failure. Add recovery only if it exists; add a cause only if known and useful. |
| Empty state | State the empty condition. Add a known reason or existing action only if useful. |
| Destructive action | Name the object and keep the irreversible consequence. |
| Disabled control | Keep an existing availability reason when needed. |
| Icon-only control | Keep its accessible name. |

## Example

| Example | Type | Result |
| --- | --- | --- |
| Safeguard your precious worlds effortlessly with powerful automated backup protection. | Delete | — |
| Create a new backup now | Shorten | Create backup |
| Changed entries | Rewrite | Changes |
| Your backup was successfully created and is now safely stored. | Shorten | Backup created. |

## Avoid

- Rewriting copy that should be deleted.
- Treating “all copy” as all possible states or a word list as proof of slop.
- Removing safety, recovery, disabled reasons, or accessible names.
- Adding reassurance, assumptions, internal reasoning, or style-only rewrites.
- Editing unrelated documentation.

## Check

Check format, one verified job per string, and safe deletions. Drop unchanged rows. If **Shorten** changes words or their order, mark **Rewrite**. Audits show **Delete**, **Shorten**, and **Rewrite**; show **Keep** only when asked for unchanged copy, repeating it. With UI, test real width, dynamic values, and accessible names. Keep scope.
