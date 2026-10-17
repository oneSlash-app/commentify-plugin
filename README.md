# Commentify

Your team's design feedback from Figma, Jira and Notion, in Claude.

Commentify brings the comment threads from your Figma files, Jira issues and Notion pages into one place. This plugin connects Claude to it, and teaches Claude how to use it well.

## What it does

- **Ask what the team said.** "What did the team say about the Inbox page?" "Is there open feedback on PROJ-123?" Claude answers from the threads and cites them.
- **Check feedback before changing code.** When you work on a screen or a component, Claude looks up the threads about those files and brings the decisions and open questions into the work.
- **Reply in your name.** Claude drafts a reply, shows it to you, and posts it on Figma, Jira or Notion once you confirm. Pro plan.
- **Close threads.** Mark threads done in Commentify when they are handled, after you confirm the list. Pro plan.

## Setup

1. Sign up at [app.commentify.one](https://app.commentify.one) and connect at least one of Figma, Jira or Notion under Settings → Connect.
2. Install this plugin. In Claude Code, one line does it:

   ```
   /plugin install commentify --marketplace oneSlash-app/commentify-plugin
   ```

   On claude.ai and in Cowork, add it from Customize → Plugins, then connect the Commentify connector from the plugin's Connectors tab and sign in. In Claude Code, run `/mcp` and sign in when the browser opens.
3. Ask Claude about your feedback.

Reading is on every Commentify plan, within a daily limit. Replying and marking threads done need the Pro plan. The full guide is at [app.commentify.one/docs/agents](https://app.commentify.one/docs/agents).

## Data

The plugin sends your questions, the file paths and ticket keys you mention, and the replies you confirm to Commentify at `app.commentify.one`, over the connector you sign in to. Commentify answers with your own team's comment threads. The plugin stores nothing itself. Commentify's privacy policy is at [commentify.one/privacy-policy](https://commentify.one/privacy-policy).

## Skills

| Skill | When Claude uses it |
| --- | --- |
| `design-feedback-digest` | A question about what the team said, or a digest of open threads |
| `feedback-for-code` | Working on UI files, a component or a ticket that designers commented on |
| `reply-to-feedback` | Answering a thread in your name (Pro) |
| `close-feedback-threads` | Marking handled threads done (Pro) |
