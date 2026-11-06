---
name: project-summary
description: Summarize the decisions made on a project, with date, who decided, why, and a link, plus an on-track opinion against the agreed timeline. Use when asked for a project summary or what has been decided.
---

# Project summary

## Input
- The project's Slack channel.
- The agreed timeline (board or schedule) and supporting docs: PRD, eng spec, Jira epic.
- The period to cover (default: since the last summary).

## Output
Numbered fragments, one link last per item.
1. **Headline**: on track or at risk, how sure, why. One line.
2. **Decisions made**: `N.` what was decided and what it means, date, who, why. [link]
3. **Plan changes**: decisions that change scope, dates, or versions, and whether the docs reflect them.

## Steps
1. Read recent Slack, the docs, and Jira. Find every decision made, however small.
2. Find the current week's goals (the latest weekly goals post); ignore earlier weeks. With no goals post, use the "next week" list from the previous Friday's recap and flag any unclear items.
3. Compare the goals with the timeline and give your on-track opinion with the reason and how sure you are. Use the timeline only for milestones and dates, not for who is assigned.
4. If a decision departs from a document, link the exact section of each side and name the passage.

## Rules
- Read-only. Never post, comment, or edit anything.
- Style: terse numbered fragments, no full sentences. Key facts only, ONE link per item (the exact section), last. Plain words: say what it means first; no jargon, ticket numbers, or code names in the lead; define a technical term if unavoidable. Check PR and ticket numbers before citing them. Recommendations need solid reasons, never weak or speculative examples.
- On "expand N" from the lead: give the full detail then: what and why, options with tradeoffs, recommendation (marked opinion), what happens if nobody decides, who decides, links.
- Don't guess: if you can't tell, mark it "Unsure" and list the facts. Don't report an item twice; if it changed, say what changed.
