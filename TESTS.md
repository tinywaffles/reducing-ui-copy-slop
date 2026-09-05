# Copyslop regression checks

Run these cases with the current skill in a disposable workspace. Compare observable output and file changes, not exact prose. Repeat in each host before claiming behavior has been tested there; frontmatter and ZIP validation alone do not prove model behavior.

1. **Mixed known and unknown facts.** A backup button says `Create a new backup` and creates one backup. A status says `Your backups are safely stored`, but the retention and storage behavior are unavailable. Ask for an audit. Expect the button proposal plus `Open product facts` identifying the uncertain status and asking only what is needed to assess it; no invented replacement, file edits, or claim that the blocked status is resolved. Repeat with just the uncertain status: expect only the questions. Repeat with just the clear label `Create backup`: expect `No copy changes.`

2. **Duplicate occurrences and partial approval.** Two independent buttons in different files say `Create a new backup`. Both can shorten to `Create backup`. Audit both, then approve only the first file's row. Expect distinct locations and an edit only in that file. Reject the remaining row: it must remain unchanged.

3. **Linked label and helper.** A control labeled `Text` changes font size. Its helper says `Changes text size`. Audit it alongside the independent backup button. If the proposal moves the helper's fact into `Text Size` and deletes the helper, expect a shared group. Approve only the helper deletion and backup row. Expect the backup edit, both grouped strings unchanged, and identification of the missing label approval. Approve the complete group: both changes may now be applied.

4. **Scope, state, and useful instructions.** Audit `Text Size`, `Motion Speed`, `Unsaved` as the only pending-edit indicator, `Paste API key` inside its input, and `This setting only affects browser access` beside separate browser and desktop controls. Expect property-specific labels, state, input instruction, and browser-only scope preserved. Keep rows appear only when requested.

5. **Meaningful boundaries and object names.** Audit `Managed by your organization` beneath an unavailable setting, `Cloud upload is unavailable while offline` beside a disabled upload button, and the standalone notification `The document could not be saved.` Expect the ownership, disabled reason, and document identity retained. Brevity alone does not justify replacing the notification with `Failed to save.`

6. **Dynamic strings and shared callers.** A shared catalog entry `backup.remaining` is `{count, plural, one {There is # backup remaining} other {There are # backups remaining}}`. Another entry `backup.failed` is `Could not save backup {name}: %s`. Audit one caller, then approve a wording change. Expect callers traced before proposing any edit, no unapproved effects on other surfaces, keys/tokens and all plural branches preserved, and an explicit source-only limitation if rendering cannot be checked.

7. **Feedback and stale proposals.** Audit the backup button. Respond with feedback without approval: expect a revised proposal and no edit. Before applying a proposal, change the fixture's behavior so it schedules a backup instead of immediately creating one. Approve the old proposal: expect the changed context to be rechecked and a revised proposal before editing.
