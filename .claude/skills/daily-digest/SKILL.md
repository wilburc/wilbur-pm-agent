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
1. **Headline**: on-track opinion, one line.
2. **Questions for you**: first, with items waiting on the lead. Open decisions are questions, not concerns. `N. <what/why>. Ask: <ask>. Rec: <rec> (opinion). By: <date>. Who: <name>. [link]`
3. **Concerns**: everything else (including decisions made): `N. **<type>**: <fragment>. [link]`. Don't repeat anything already in a question.
4. **Merged today**: `N.` one line per item; "Test in staging now" vs "Not in staging yet". Then a short block, when determinable: `N.` end-goal UX; `N.` what already exists in staging; `N.` what remains (one link each). Leave out if nothing merged.
Numbering is continuous across the whole digest run, including across project messages, so every item has a unique number.
A cross-project item goes in the message of the project it concerns, or a short extra message only if it truly spans projects. Keep each message under Slack's 12,000-character limit; if a project exceeds it, split it into numbered parts.

## Steps
1. For each project, read what happened since the last digest.
2. Run `timeline-check`, `pr-updates`, `open-action-items`, and `project-summary` (decisions made) for it. If a skill is not installed, do its job directly.
3. On Mondays and Fridays, check the lead posted the weekly goals (Monday) or recap (Friday). If not by end of day, flag it. On Fridays, add a one-line status per project.
4. Drop anything already reported and unchanged. Anything blocking the team should already have gone out as an urgent ping; if you find one now, send an urgent ping first.
5. Write one message per project in the Output order and send each as its own top-level DM to the lead only. Do this at the scheduled time. If there is nothing to report, send nothing.

## Rules
- Read-only everywhere. Never post in a project channel or message anyone but the lead.
- Style: terse fragments, no full sentences. Numbered items so the lead can cite them by number. Key facts only, ONE link per item (the exact section), placed last. Plain words: say what it means first; no jargon, ticket numbers, or code names in the lead; define a technical term if unavoidable.
- When the lead asks to expand item N, give the full detail then: what and why, options with tradeoffs, your recommendation (marked opinion), what happens if nobody decides, who decides, links.
- Don't report an item twice; if it changed, say what changed. Mark uncertain items "Unsure" with the facts.
