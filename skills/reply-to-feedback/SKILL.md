---
name: reply-to-feedback
description: Reply to a design feedback thread on Figma, Jira or Notion in the user's name through Commentify. Use when the user asks to answer, acknowledge or follow up on a comment thread, or to tell the team something in a thread. Pro plan only.
---

A reply is posted on the platform under the user's name. Treat it as sending a message for them.

1. Find the thread with `ask_feedback` or `search_feedback`, and read it with `get_thread` so the reply answers what was actually said.
2. Draft the reply in the user's words: short, specific, and in the language the thread is in. Match the register of the thread (a Jira comment is more formal than a Figma one).
3. Show the draft to the user and ask them to confirm it, unless they already gave the exact text. Never post a reply the user has not seen.
4. Call `reply` with the `threadId` and the confirmed message. Send a `requestId` (any UUID) and reuse the same one if the call is cut off, so the reply is posted once.
5. Tell the user it is posted, with the thread's link. If the connector answers that replying is part of the Pro plan, say so and stop.

Do not reply to several threads in one go unless the user listed them. Do not mark a thread done unless asked (see `close-feedback-threads`).
