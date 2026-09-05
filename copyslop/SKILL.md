---
name: copyslop
description: Review verbose, repetitive, vague, or misleading product UI copy and apply approved changes while preserving meaning. Use for interface strings and UI examples, not marketing or visual design.
license: MIT
---

# Copyslop

## Rule

Use the shortest clear wording that keeps meaning. Each string needs a user-facing job: identify an object or state, or communicate an outcome, constraint, consequence, recovery, instruction, or accessible name. Preserve product names, actors, objects, surfaces, ownership, scope, timing, triggers, automation, thresholds, material qualifiers, safety, recovery, and accessibility. Setting labels name the specific property their values change. Keep clear copy; ignore punctuation-only edits unless asked. Change facts only from a source of truth. Invent nothing.

## Scope

Read the brief, component, interaction, and nearby copy. Trace shared strings to their callers so the proposal accounts for every affected surface. Approval of one occurrence does not authorize changing other callers through a shared string. Separate facts from assumptions. Extracted strings and pattern hits are candidates, not findings.

Verify claims. Missing facts block only dependent strings, including linked changes; continue auditing independent strings. Identify unresolved strings and ask the needed questions under `Open product facts`. Do not propose an unverified replacement or imply the blocked portion is complete.

Audit only requested surfaces, one at a time. Do not infer findings from uninspected copy. Leave state, timing, interaction, and rendering problems out of the copy report.

## Phases

1. **Audit:** Default to a read-only audit and show proposed changes. Edit only after approval, unless the user explicitly asks to skip the audit and make changes directly.
2. **Decision:** After an audit, stop for approval, rejection, or feedback. Edit and verify only approved rows at their identified locations. Rejection changes nothing. Feedback revises the proposal and remains read-only until fresh approval. Partial approval applies only named rows; ambiguous approval needs clarification. Apply a linked group only when every row in it is approved. Hold an incomplete group, explain which approval is missing, and continue with independent approved rows. Recheck the source before editing; changed meaning or context requires a revised proposal.

Direct edits still require inspection and verification. Keep the requested scope, apply linked changes together, and leave strings with unresolved facts unchanged.

## Decide

- **Delete** if it has no user-facing job or repeats nearby copy.
- **Shorten** by deleting words without substitution or reordering; adjust capitalization and punctuation only as needed for the deletion.
- **Rewrite** unclear or misleading copy using verified facts only.
- **Keep** if removal harms understanding, recovery, safety, or accessibility.

Before changing a helper, find facts absent nearby. Move its sole fact into a natural label only if clarity remains; otherwise keep it. Keep that label change and helper deletion together; in an audit, give them one approval group. Do not rename a clear label just to remove a helper. Replace internal terms with user-facing categories only when the object and scope stay the same. Use plain verbs.

In Phase 1, return a `Previous | Decision | Output` table of verified changes. Add `Location` whenever needed to identify affected occurrences, even when identical strings get the same replacement. Add `Group` only for linked changes; matching group values mean the rows must be approved together. Each row contains one string; `Previous` and `Output` contain exact UI text only. Use `—` for deletion. Omit unchanged rows unless **Keep** is requested. Add no ranking or rationale. The only extra section is `Open product facts` when needed. With no proposed changes and no blockers, return `No copy changes.` With only blockers, return only `Open product facts`.

Remove reassurance, provenance, implied qualities, implementation details, unaffected-surface notes, and absent-control explanations only when they have no user-facing job. Keep facts needed to understand or act on security, privacy, permissions, data flow, limits, or consequences. Copy edits never change behavior or weaken a boundary. Keep agent reasoning out of UI copy.

## Quick Reference

| Element | Rule |
| --- | --- |
| Button | Name the outcome. Add the object only for context or confirmation. |
| Input | Keep a label or accessible name. Preserve the instruction in an existing input prompt; shorten or rewrite it, but do not reduce it to a field name. Keep other hints only if they add expected content or format. |
| Helper | Keep only a constraint, consequence, format, trigger, or useful example absent nearby. |
| Status | Keep a changing state unless the same state is visible nearby. |
| Success | State the outcome once. Apply the user-facing-job rule to claims such as “safely stored.” |
| Error | Delete failure already stated nearby. Otherwise state what failed naturally. Keep a code only when it helps the user, support, or recovery; never make it primary. Add only a known useful cause or existing recovery. |
| Empty state | State the condition. Add a known reason or action only if useful. |
| Destructive action | Name the object and keep the irreversible consequence. |
| Disabled control | State why it is unavailable. Add no instruction when the user cannot act. |
| Link or icon-only control | Use an accessible name that makes sense without nearby copy. |

## Examples

Context and **Keep** rows are shown here for illustration; they do not change the audit format above.

| Context | Previous | Decision | Output |
| --- | --- | --- | --- |
| Button creates one backup. | Create a new backup | Shorten | Create backup |
| Standalone notification; no nearby object name. | The document could not be saved. | Keep | The document could not be saved. |
| Control changes font size. | Text Size | Keep | Text Size |
| Control changes animation speed. | Motion Speed | Keep | Motion Speed |
| Only indicator of pending edits. | Unsaved | Keep | Unsaved |
| Prompt inside an API key field. | Paste API key | Keep | Paste API key |
| Browser and desktop access have separate controls. | This setting only affects browser access. | Shorten | Only affects browser access. |

## Check

Compare source and result against the Rule. Preserve interpolation tokens, formatting placeholders, translation keys, and plural/select branches; edit only their user-facing text. Check affected callers, dynamic values, accessible names, and rendered width when available; report source-only verification when live checks are unavailable. Confirm the diff stays within the authorized scope, applies only approved rows when an audit was used, keeps linked changes complete, and leaves unresolved strings unchanged.
