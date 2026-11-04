---
name: daily-digest
description: Build and send the end-of-day digest of one or more project channels as one top-level DM per project, built from the pr-updates, open-action-items, project-summary, and timeline-check skills. Use at the end of the day, or when someone just wants a project digest.
---

# Daily digest

## Input
- The list of project channels, and for each: PRD, eng spec, Jira epic, and the timeline.
- Who receives it (the lead) and when (default: weekdays 5:00 pm Eastern).

## Output
Separate top-level DMs to the lead, not replies in an existing thread, one message per project. Each message, in this order:
1. **Headline**: your on-track opinion.
2. **Questions for you**: first, with the items waiting on the lead in it. Open decisions are questions, not concerns.
3. **Concerns**: everything else (including decisions made), one line each: `- **<type>**: <what and why>. [link]`. Don't repeat anything already in a question.
4. **Merged today**: what merged and what to test in staging; leave it out if nothing merged.
A cross-project item goes in the message of the project it concerns, or a short extra message only if it truly spans projects. Keep each message under Slack's 12,000-character limit; if a project exceeds it, split it into numbered parts. Keep it short.

## Steps
1. For each project, read what happened since the last digest.
2. Run `timeline-check`, `pr-updates`, `open-action-items`, and `project-summary` (decisions made) for it. If a skill is not installed, do its job directly.
3. On Mondays and Fridays, check the lead posted the weekly goals (Monday) or recap (Friday). If not by end of day, flag it. On Fridays, add a one-line status per project.
4. Drop anything already reported and unchanged. Anything blocking the team should already have gone out as an urgent ping; if you find one now, send an urgent ping first.
5. Write one message per project in the Output order and send each as its own top-level DM to the lead only. Do this at the scheduled time. If there is nothing to report, send nothing.

## Rules
- Read-only everywhere. Never post in a project channel or message anyone but the lead.
- Plain language first: say what it means for scope, timeline, quality, or customers. No jargon, ticket numbers, or code names in the lead sentence. Every item gets a link, placed last as backup, to the exact section. Write for a busy reader who is not deep in the code; as simple and short as possible.
- Don't report an item twice; if it changed, say what changed. Mark uncertain items "Unsure" with the facts.
