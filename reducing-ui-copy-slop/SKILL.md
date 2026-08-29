---
name: reducing-ui-copy-slop
description: Cuts verbose, repetitive, promotional, vague, speculative, or reassuring product UI copy without losing meaning, safety, recovery, or accessibility. Use for labels, helper text, buttons, dialogs, empty states, errors, success messages, and UI-copy examples in documentation; not marketing, visual design, or unrelated prose.
license: MIT
---

# Reducing UI Copy Slop

## Rule

Use the shortest wording that keeps the meaning and context. Keep a string only if it adds information not shown by the layout, label, value, control, state, or nearby text. Cover required elements; do not add plausible ones.

## Scope

Read the brief, component, interaction, and nearby copy. Separate facts from assumptions. Requests for *polished*, *premium*, *friendly*, *helpful*, or *finished* UI do not authorize extra UI.

Do not invent controls, states, metrics, progress, guarantees, confirmations, tooltips, or behavior. If a missing fact blocks accurate copy, list only it under `Open product facts`. Otherwise proceed without guessing.

## Decide

Each string must identify an object or state, name an outcome, state a constraint or consequence, explain recovery, give required instruction, or provide an accessible name.

- **Delete** if it has no unique job or repeats stronger nearby copy.
- **Shorten** if its job is needed but the wording is indirect or padded.
- **Keep** if removal would hurt understanding, recovery, safety, or accessibility.

Return a compact audit with source copy, decision, and result. Fit labels and layout to the task; never force a schema. Cut preambles, summaries, and routine reasons. Explain only when asked or to preserve safety, recovery, or accessibility. Apply file edits when requested.

Use this for docs examples too. Drop setup or reasons that only justify **Delete** or **Shorten**, including nearby headings, controls, or values. Keep stated consequences and safety facts; labels do not replace them. Keep other context only to avoid a misleading result. Never show agent or implementation reasoning as UI copy.

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
| Your backup was successfully created and is now safely stored. | Shorten | Backup created. |

## Avoid

- Rewriting copy that should be deleted.
- Treating “all copy” as all possible states or a word list as proof of slop.
- Removing safety, recovery, disabled reasons, or accessible names.
- Adding reassurance, assumptions, internal reasoning, or unspecified behavior.
- Lengthening context-clear actions or varying terms for style.
- Editing unrelated documentation.

## Check

Check the requested format, one verified job per string, safe deletions, and blocking `Open product facts` only. If the UI is available, test realistic width, dynamic values, and accessible names. Keep scope.
