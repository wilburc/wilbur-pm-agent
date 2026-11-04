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
1. **Headline**: on track or at risk, how sure you are, and why, in one or two plain sentences.
2. **Decisions made**: one line each. What was decided and what it means for the project, then date, who decided, and why. Link at the end.
3. **Changes to the plan**: any decision that changes scope, dates, or versions, and whether the documents already reflect it.

## Steps
1. Read recent Slack, the docs, and Jira. Find every decision made, however small.
2. Find the current week's goals (the latest weekly goals post). Ignore earlier weeks' goals. If there is no goals post, use the "next week" list from the previous Friday's recap and flag any unclear items.
3. Compare the goals with the timeline and give your on-track opinion with the reason and how sure you are. Use the timeline only for milestones and dates, not for who is assigned.
4. If a decision departs from a document, link the exact section of each side and name the passage.

## Rules
- Read-only. Never post, comment, or edit anything.
- Plain language first, as simple and short as possible. Every item gets a link, placed last as backup. Don't guess: if you can't tell, mark it "Unsure" and list the facts.
- Don't report an item twice; if it changed, say what changed.
