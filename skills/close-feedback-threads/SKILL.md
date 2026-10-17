---
name: close-feedback-threads
description: Mark design feedback threads as done in Commentify, or reopen them. Use when the user says a comment is resolved, handled, shipped, or asks to clean up or triage open threads. Pro plan only.
---

Marking a thread done moves it from Comments to Checked in Commentify for the user. It does not change the thread on Figma, Jira or Notion.

1. List what would be marked done. Find the threads with `search_feedback` (use `openOnly: true` and the user's clues) and show them: file, head comment, who, when.
2. Ask the user to confirm the list, unless they named exactly one thread. Do not close threads by guessing from a vague request such as "clean up".
3. Call `set_thread_status` with `status: "CHECKED"` for each confirmed thread, one call per thread. Use `"COMMENTS"` to reopen one.
4. Report what was done. If a thread had an unanswered question in it, say so; the user may want to reply first (see `reply-to-feedback`).

If the connector answers that this is part of the Pro plan, say so and stop.
