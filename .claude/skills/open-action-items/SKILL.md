---
name: open-action-items
description: Find open decisions and keep as questions only the ones that are the lead's call (explicitly tagged or asked, named spec approver, or explicit decision owner), each a terse numbered question answerable in a word or phrase. Everything else becomes an "Owner" status line or is dropped. Expands into full detail on request. Use when asked what needs a decision or what is waiting on me.
---

# Open action items

## Input
- The project's Slack channel.
- Where the plan lives: PRD, eng spec, Jira epic.
- Who the lead is, so you can tell what is their call.

## Output
A numbered "Questions for you" list of only the lead's calls (see "Whose call is it"), one or two lines per question, answerable in a word or a short phrase:
`N. <what and why, plain words>. Ask: <the ask>. Rec: <recommendation> (opinion). By: <deadline>. Who: <decider; chase>. [link]`
- Options only if there is a real choice: one short line.
- Open items that are not the lead's call are not questions. Give each as a status line, or drop it if it is no risk to a date or quality: `N. <what>. Owner: <name>. Risk: <to which date or to quality>. [link]`
- If the owner is unknown, write "Owner: unknown" in the status line. Do not ask the lead to find one.

## Whose call is it
A question goes to the lead only when they are explicitly tagged or asked to make that call, OR are the named spec approver, OR are the explicit owner of that decision. Never frame an item as blocked on the lead because a date is unclear, an owner is missing, a decision belongs to someone else, or a PR needs review. Never list PR reviews or code-owner reviews as waiting on the lead unless they are tagged. If unsure whether it is their call, treat it as not theirs and name who owns it.

## Expand on request
On "expand N": what is happening and why it matters; options, each with a one-line tradeoff; recommendation (marked opinion); what happens if nobody decides, and by when; who decides (a name, and why them: owner or approver per the doc, ticket, or channel) and who to chase; links to the Slack message or doc section.

## Steps
1. Read recent Slack, the PRD and spec, and Jira. Find every open (undecided) decision, whoever owns it.
2. Filter: keep as a question only a decision where the lead is explicitly tagged or asked, is the named spec approver (a spec awaiting their approval), or is the explicit owner. Everything else, including PR and code-owner reviews (unless they are tagged), becomes an "Owner" status line or is dropped. When unsure, it is not the lead's call.
3. Before asking the lead for a missing doc or fact only they can supply, try to find it yourself: search the channel (including threads), Slack search, Confluence, and Jira. Ask only if that turns up nothing, and say what you searched. If a project has no PRD and the lead has said so, don't ask again.
4. Put each question in the list; don't bury it inside another item. Don't put status lines in the questions list.

## Rules
- Read-only. Never post, comment, or message anyone except the lead.
- Style: terse numbered fragments, no full sentences. Key facts only, ONE link per item (the exact section), last. Plain words: say what it means first; no jargon, ticket numbers, or code names in the lead; define a technical term if unavoidable. Check PR and ticket numbers before citing them. Recommendations need solid reasons, never weak or speculative examples.
- On "expand N" from the lead: give the full detail then: what and why, options with tradeoffs, recommendation (marked opinion), what happens if nobody decides, who decides, links.
- Don't report an item twice; if it changed, say what changed.
