---
name: feedback-for-code
description: Check the team's design feedback before or while changing code. Use when the user is working on UI files, a component, a screen or a ticket and asks whether there is feedback about it, or when a change touches something designers commented on.
---

Before changing a screen or a component, check what the team already said about it.

1. Call `ask_feedback` with the file paths being changed in `files`, the repo or project name in `project`, and the ticket key in `ticket` if the branch or the task names one. Add the component or screen name in `terms`.
2. Read the answer and its citations. Each citation names the thread, the platform and the file or issue it is on.
3. Bring the relevant points into the work:
   - A decision in a thread (agreed size, colour, copy, behaviour) is a requirement. Follow it, and say which thread it came from.
   - An open question in a thread is a risk. Name it to the user before building on an assumption.
   - A thread that is already checked (done) is history, not a requirement.
4. When nothing matches, say that no feedback was found for those files and carry on. Do not invent feedback.

Mention the threads you used by their links, so the user can read them. Do not reply in a thread from this skill; the user decides that (see the `reply-to-feedback` skill).
