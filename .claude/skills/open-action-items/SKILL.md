---
name: open-action-items
description: Turn every open decision and anything waiting on the lead into a short question they can answer in a word or phrase. Each question carries the context, options with tradeoffs, a recommendation, urgency, and who to chase. Use when asked what needs a decision or what is waiting on me.
---

# Open action items

## Input
- The project's Slack channel.
- Where the plan lives: PRD, eng spec, Jira epic.
- Who the lead is (the person the questions are for), so you can tell what is waiting on them.

## Output
A "Questions for you" list. One question per item, answerable in a word or a short phrase. Each question has:
- **What is happening and why it matters**, in plain language.
- **Options**, each with a one-line tradeoff. Your recommendation if you have one, marked as opinion.
- **What happens if nobody decides**, and by when (a date or milestone, tied to the timeline if known).
- **Who decides** (a name, and why them: owner or approver per the doc, ticket, or channel), and **who to chase** if not the lead. If the owner is unknown, mark it "Unsure" and say so.
- **Link** to the Slack message or doc section where it was raised, at the end.

## Steps
1. Read recent Slack, the PRD and spec, and Jira. Find every open (undecided) decision, whoever owns it, not only ones waiting on the lead.
2. Also include items waiting on the lead: specs where they are the approver, PRs awaiting their sign-off, and decisions left for them.
3. Before asking for a missing doc or fact, try to find it yourself: search the channel (including threads), Slack search, Confluence, and Jira. Ask only if that turns up nothing, and say what you searched.
4. Write each item as a question per the Output shape. Put each question in the list; don't bury it inside another item.

## Rules
- Read-only. Never post, comment, or message anyone except the lead.
- Plain language first. No jargon, ticket numbers, or code names in the lead sentence; define a technical term if unavoidable. Every item gets a link, placed last as backup, to the exact section. As simple and short as possible.
- Don't report an item twice; if it changed, say what changed.
