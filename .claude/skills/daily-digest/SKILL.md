---
name: daily-digest
description: Build and send the end-of-day digest of one or more project channels as one top-level DM per project, built from the pr-updates, open-action-items, project-summary, and timeline-check skills. Use at the end of the day, or when someone just wants a project digest.
---

# Daily digest

## Input
- The project channels, and for each: PRD, eng spec, designs, Jira epic, and the timeline. A project with no docs gets Jira and ticket health only; don't flag missing docs.
- Who receives it (the lead) and when (default: weekdays 5:00 pm Eastern).

## Output
Separate top-level DMs to the lead, not replies in an existing thread, one message per project. Each message, in this order:
1. **Headline**: on-track opinion, one line.
2. **Questions for you**: first, only the lead's calls: explicitly tagged or asked, named spec approver, or explicit decision owner (see Rules, "Whose call"). If none, leave the section out. `N. <what/why>. Ask: <ask>. Rec: <rec> (opinion). By: <date>. Who: <name>. [link]`
3. **Status (not blocked on you)**: optional, short. Risks to a date or to quality that others own, such as hanging PRs, unowned tickets, date drift, a missing weekly post: `N. <fragment>. Owner: <name>. Risk: <date or quality>. [link]`. Omit what is no risk. Never worded as an ask to the lead.
4. **Concerns**: other findings the lead should know (including decisions made), each with a named owner where there is one: `N. **<type>**: <fragment>. [link]`. Don't repeat anything already in a question or status line.
5. **Merged today**: `N.` one line per item, "Test in staging now" (concrete user flows) vs "Not in staging yet". Then, when determinable, per version (or the whole project if no versions): `N.` "<version> includes: a, b, c"; `N.` "In staging now (testable): flows x, y"; `N.` "Still to build: flow z". Leave out if nothing merged.
Numbering is continuous across the whole digest run, including across project messages, so every item has a unique number.
A cross-project item goes in the message of the project it concerns, or a short extra message only if it truly spans projects. Keep each message under Slack's 12,000-character limit; if a project exceeds it, split it into numbered parts.

## Steps
1. For each project, read what happened since the last digest.
2. Run `timeline-check`, `pr-updates`, `open-action-items`, and `project-summary` (decisions made) for it. If a skill is not installed, do its job directly.
3. Sort every finding by whose call it is: question (the lead's call only), status (owned by others, a risk to a date or quality), or left out. On Mondays and Fridays, check the lead posted the weekly goals (Monday) or recap (Friday). If not by end of day, flag it. On Fridays, add a one-line status per project.
4. Drop anything already reported and unchanged. Anything actually blocking the team that needs the lead should already have gone out as an urgent ping; if you find one now, send an urgent ping first.
5. Write one message per project in the Output order and send each as its own top-level DM to the lead only, at the scheduled time. If there is nothing to report, send nothing.

## Rules
- Read-only everywhere. Never post in a project channel or message anyone but the lead.
- Whose call: ask the lead (a question, "needs you", "waiting on you") only when they are explicitly tagged or asked to make that call, OR are the named spec approver, OR are the explicit owner of that decision. Never frame an item as blocked on the lead because a date is unclear, an owner is missing, a decision belongs to someone else, or a PR needs review. Never list PR reviews or code-owner reviews as waiting on the lead unless they are tagged. If unsure whether it is their call, treat it as not theirs and name who owns it. Everything else is a short status line with a named owner and the risk to a date or to quality, or is left out if it is neither.
- Style: terse numbered fragments, no full sentences. Key facts only, ONE link per item (the exact section), last. Plain words: say what it means first; no jargon, ticket numbers, or code names in the lead; define a technical term if unavoidable. Check PR and ticket numbers before citing them. Recommendations need solid reasons, never weak or speculative examples.
- On "expand N" from the lead: give the full detail then: what and why, options with tradeoffs, recommendation (marked opinion), what happens if nobody decides, who decides, links.
- Don't report an item twice; if it changed, say what changed. Mark uncertain items "Unsure" with the facts.
