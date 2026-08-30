---
name: copyslop
description: Use when reviewing or editing product UI copy that may be verbose, repetitive, promotional, vague, speculative, reassuring, or misleading, including labels, helpers, controls, dialogs, empty states, errors, success messages, and documentation examples; not marketing, visual design, or unrelated prose.
license: MIT
---

# Copyslop

## Rule

Use the shortest wording that keeps meaning. Review each string with nearby UI and its interaction. Each string must name an object or state, or communicate an outcome, constraint, consequence, recovery, instruction, or accessible name. Labels name the changed property and fit its values. Preserve product names and material timing, trigger, scope, ownership, behavior, safety, recovery, and accessibility. Change facts only from a source of truth. Keep clear copy; ignore punctuation-only edits unless asked. Invent nothing.

## Scope

Read the brief, component, interaction, and nearby copy. Separate facts from assumptions. Extracted strings and pattern hits are candidates, not findings.

Verify claims. If missing product facts prevent accurate copy, return only `Open product facts` with the needed questions.

Audit only requested surfaces, one at a time. Do not infer findings from uninspected copy. Leave state, timing, interaction, and rendering problems out of the copy report.

## Decide

- **Delete** if it has no user-facing job or repeats nearby copy.
- **Shorten** by removing padding without changing the remaining words or their order.
- **Rewrite** unclear or misleading copy using verified facts only.
- **Keep** if removal harms understanding, recovery, safety, or accessibility.

Before changing a helper, find facts absent nearby. Move its sole fact into a natural label only if clarity remains; otherwise keep it. Do not rename a clear label just to remove a helper. Replace internal terms with user-facing categories. Drop provenance and implied qualities; keep material qualifiers. Use plain verbs.

Return only a `Previous | Decision | Output` table of changed strings. Add `Location` only when identical `Previous` strings need different results. Each row contains one string; `Previous` and `Output` contain exact UI text only. `Decision` is **Delete**, **Shorten**, or **Rewrite**; include **Keep** only when asked. Use `—` for deletion. Add no ranking or rationale. If nothing changes, return `No copy changes.` A read-only audit changes no files; otherwise apply only requested edits.

Remove reassurance, implementation details, unaffected-surface notes, and absent-control explanations only when they have no user-facing job. Keep boundary copy needed to understand or act on security, privacy, permissions, data flow, limits, consequences, recovery, or safety. Copy edits never change behavior or weaken a boundary. Absence needs no explanation. Keep agent reasoning out of UI copy.

## Quick Reference

| Element | Rule |
| --- | --- |
| Button | Name the outcome. Add the object only for context or confirmation. |
| Input | Keep a label or accessible name. An existing input prompt may be shortened or rewritten, not deleted. Keep other hints only if they add expected content or format. |
| Helper | Keep only a constraint, consequence, format, trigger, or useful example absent nearby. |
| Success | State the outcome once. Cut reassurance and internal claims such as “safely stored”; keep safety facts. |
| Error | Delete failure already stated nearby. Otherwise state what failed naturally. Keep a code only when it helps the user, support, or recovery; never make it primary. Add only a known useful cause or existing recovery. |
| Empty state | State the condition. Add a known reason or action only if useful. |
| Destructive action | Name the object and keep the irreversible consequence. |
| Disabled control | State why it is unavailable. Add no instruction when the user cannot act. |
| Link or icon-only control | Use an accessible name that makes sense without nearby copy. |

## Example

| Previous | Decision | Output |
| --- | --- | --- |
| Create a new backup now | Shorten | Create backup |
| The document could not be saved. | Rewrite | Failed to save. |
| Your backup was successfully created and is now safely stored. | Shorten | Backup created. |

## Check

Compare source and result. Preserve material objects, qualifiers, triggers, automation, thresholds, safety, recovery, disabled reasons, and accessible names unless verified context corrects them. **Shorten** only deletes words; substitution or reordering is **Rewrite**. Drop unchanged rows. Check width, dynamic values, and accessible names. Keep scope.
