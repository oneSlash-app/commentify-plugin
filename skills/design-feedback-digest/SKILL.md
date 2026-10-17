---
name: design-feedback-digest
description: Summarize the team's design feedback on a feature, a screen, a ticket or a period. Use when the user asks what the team said, what is still open, what changed this week, or wants a digest of comments from Figma, Jira or Notion.
---

Use the Commentify connector. It holds the team's comment threads from Figma files, Jira issues and Notion pages, as of the last sync.

1. Call `ask_feedback` with every clue the user gave: the question in plain words, the project or feature name, a ticket key such as `PROJ-123`, key terms, and `since` when they named a period. Pass `openOnly: true` when they ask what is still open.
2. If the answer says it needs a clarification (several files match), show the options and ask which one. Then call again with that `fileId`.
3. For a digest over many threads, call `search_feedback` with the same clues and read the summaries and stances it returns. Call `get_thread` only for the threads the user wants in full.
4. Write the digest for a designer or a product manager:
   - Lead with the decisions and the open questions, not the thread list.
   - Group by screen or feature, newest activity first.
   - Name who said what, with their stance in their own words where it matters.
   - End with the threads that still need an answer, each with its link.
5. Keep it short. One line per thread is enough unless the user asked for detail. Do not paste whole threads.

If the connector answers that a limit was reached, say so and stop. Do not retry in a loop.
