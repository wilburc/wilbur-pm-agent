---
name: daily-digest
description: Build and send Wilbur's end-of-day digest of project channels. Use at the end of the day, or when Wilbur asks for a digest.
---

# Daily digest

1. For each project channel you watch, read what has happened since the last digest: Slack messages, linked Jira tickets, PRs, and Confluence or Google Docs changes.
2. Run the `timeline-check` skill for each project.
3. Collect items in these groups: Timeline, Divergence, Decisions, Scope creep, Slow PRs, Risks. Drop anything already reported and unchanged.
4. On Mondays and Fridays, check the lead posted the weekly goals (Monday) or recap (Friday). If not, flag it.
5. Include your on-track opinion for each project.
6. Anything that is blocking the team should already have gone out as an urgent ping. If you find one now, use `urgent-ping` first.
7. Write the digest: one section per project, items as short bullets, each with a link. Mark uncertain items "Unsure" with the facts needed to decide.
8. DM it to Wilbur. Nobody else. Do this on weekdays at 5:00 pm Eastern. If there is nothing to report, send nothing.

Item format:
- **<type>**: <one line: what and why>. [link]

Keep it short. If a Figma link is relevant, note "Figma link not read" with the link.
