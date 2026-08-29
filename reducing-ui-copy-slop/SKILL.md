---
name: reducing-ui-copy-slop
description: Removes unnecessary user-visible product interface copy while preserving meaning, actionability, safety, recovery, and accessibility. Use when creating, reviewing, or editing UI labels, helper text, buttons, dialogs, empty states, errors, or success messages that feel verbose, repetitive, promotional, vague, overly reassuring, or AI-generated; not for marketing or long-form prose.
license: MIT
---

# Reducing UI Copy Slop

## Core Principle

A string earns its place only when it contributes information not already carried by the layout, label, value, control, state, or nearby text. Complete means every required element is covered, not every imaginable element is added.

## Fence the Scope First

Read the brief, component anatomy, interaction, and surrounding copy. Separate facts from assumptions. *Polished*, *premium*, *friendly*, *helpful*, and *finished* describe quality; they do not authorize extra UI.

Do not invent controls, panels, states, metrics, progress steps, guarantees, confirmations, tooltips, or product behavior. If necessary behavior is unspecified, list it under `Open product facts`; do not write speculative copy for it.

## Give Each String One Job

A valid string identifies an object or state, names an outcome, communicates a constraint or consequence, explains recovery, provides necessary instruction, or supplies an accessible name.

Use this decision contract:

- **Delete** when the string has no unique job or repeats stronger nearby copy.
- **Shorten** when its job is necessary but the wording is indirect or padded.
- **Keep** when removing it would reduce understanding, actionability, recovery, safety, or accessibility.

For new UI, return `Element | Copy | Unique job` for explicitly specified elements and states only. For an audit, return `Location | Decision | Final copy | Unique job`. Do not add another section after these tables except `Open product facts` when needed.

## Quick Reference

| Element | Useful shape |
| --- | --- |
| Button | Name the outcome with a direct verb and object. |
| Helper | Add a constraint, consequence, format, or non-obvious example. |
| Success | Confirm the outcome; add a next consequence only when it changes what the user should do. |
| Error | Say what failed and what to do next; include a cause only when known and useful. |
| Empty state | Distinguish why it is empty and offer the next useful action. |
| Destructive action | Name the object and preserve the irreversible consequence. |
| Disabled or icon-only control | Preserve the availability reason and accessible name. |

## Example

Given a `Backups` heading and a `Backup schedule` control set to `Every 6 hours`:

| Current copy | Decision | Final copy | Unique job |
| --- | --- | --- | --- |
| Safeguard your precious worlds effortlessly with powerful automated backup protection. | Delete | — | None; promotional repetition. |
| Create a new backup now | Shorten | Create backup | Names the outcome. |
| Your backup was successfully created and is now safely stored. | Shorten | Backup created. | Confirms completion without an unverified safety claim. |

## Common Mistakes

- Rewriting unnecessary copy instead of deleting it.
- Treating “all copy” as “all possible states” instead of all specified states.
- Treating suspicious words as proof; word lists are signals only.
- Removing safety, recovery, disabled reasons, or accessible names.
- Inventing behavior, guarantees, or states while trying to help.
- Varying established terms for style.

## Verify

Confirm each string maps to a specified element, has a unique job, and states verified behavior. Confirm deletions preserve meaning. When the UI is available, check realistic width, dynamic values, and accessible names. Keep edits in scope.
