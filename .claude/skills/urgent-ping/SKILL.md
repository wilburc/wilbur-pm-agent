---
name: urgent-ping
description: Send an immediate private ping when something is actually blocking the team and needs the lead, or the lead should know who owns the unblock. Only for blockers; everything else waits for the daily digest.
---

# Urgent ping

## Input
- The blocker, the project, and who to message (the lead).

## Output
A short DM to the lead: numbered fragments, key details first, one link per item last.
1. Project.
2. What is blocked, who or what it blocks, what it means for the project.
3. Why you think so. If the lead is needed (tagged or asked, named spec approver, or explicit decision owner): ask, deadline. Otherwise: "Owner of the unblock: <name>", no ask.
4. Links as backup. If unsure, say "Unsure" and give the facts.

## Steps
1. Use only when something is actually blocking the team and either needs the lead or has no one visibly unblocking it. A date, owner, or review that is merely unclear or slow is not a blocker; leave it for the daily digest status.
2. Confirm it is a blocker and not already reported. Confirm whose call the unblock is; if it is someone else's, name them and do not ask the lead.
3. DM the lead, and nobody else. Keep it to a few lines.

## Rules
- Never post in the project channel. Read-only everywhere else.
- Whose call: ask the lead (a question, "needs you", "waiting on you") only when they are explicitly tagged or asked to make that call, OR are the named spec approver, OR are the explicit owner of that decision. Never frame an item as blocked on the lead because a date is unclear, an owner is missing, a decision belongs to someone else, or a PR needs review. Never list PR reviews or code-owner reviews as waiting on the lead unless they are tagged. If unsure whether it is their call, treat it as not theirs and name who owns it. Everything else is a short status line with a named owner and the risk to a date or to quality, or is left out if it is neither.
- Style: terse numbered fragments, no full sentences. Key facts only, ONE link per item (the exact section), last. Plain words: say what it means first; no jargon, ticket numbers, or code names in the lead; define a technical term if unavoidable. Check PR and ticket numbers before citing them. Recommendations need solid reasons, never weak or speculative examples.
- On "expand N" from the lead: give the full detail then: what and why, options with tradeoffs, recommendation (marked opinion), what happens if nobody decides, who decides, links.
