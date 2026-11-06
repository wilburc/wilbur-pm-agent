---
name: open-action-items
description: Turn every open decision and anything waiting on the lead into a short question they can answer in a word or phrase. Each question is one or two numbered lines (what, ask, recommendation, deadline, who) and expands into full detail on request. Use when asked what needs a decision or what is waiting on me.
---

# Open action items

## Input
- The project's Slack channel.
- Where the plan lives: PRD, eng spec, Jira epic.
- Who the lead is (the person the questions are for), so you can tell what is waiting on them.

## Output
A numbered "Questions for you" list, one or two lines per question, answerable in a word or a short phrase:
`N. <what and why, plain words>. Ask: <the ask>. Rec: <recommendation> (opinion). By: <deadline>. Who: <decider; chase>. [link]`
- Options only if there is a real choice: one short line.
- If the owner is unknown, mark it "Unsure" and say so.

## Expand on request
When the lead asks to expand item N, give the full detail: what is happening and why it matters; options, each with a one-line tradeoff; your recommendation (marked opinion); what happens if nobody decides, and by when; who decides (a name, and why them: owner or approver per the doc, ticket, or channel) and who to chase; links to the Slack message or doc section.

## Steps
1. Read recent Slack, the PRD and spec, and Jira. Find every open (undecided) decision, whoever owns it, not only ones waiting on the lead.
2. Also include items waiting on the lead: specs where they are the approver, PRs awaiting their sign-off, and decisions left for them.
3. Before asking for a missing doc or fact, try to find it yourself: search the channel (including threads), Slack search, Confluence, and Jira. Ask only if that turns up nothing, and say what you searched.
4. Write each item as a question per the Output shape. Put each question in the list; don't bury it inside another item.

## Rules
- Read-only. Never post, comment, or message anyone except the lead.
- Style: terse fragments, no full sentences. Numbered items so the lead can cite them by number. Key facts only, ONE link per item (the exact section), placed last. Plain words: say what it means first; no jargon, ticket numbers, or code names in the lead; define a technical term if unavoidable.
- Don't report an item twice; if it changed, say what changed.
