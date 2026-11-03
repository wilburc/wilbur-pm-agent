---
name: daily-digest
description: Build and send Wilbur's end-of-day digest of project channels. Use at the end of the day, or when Wilbur asks for a digest.
---

# Daily digest

All rules (what to flag, format, links, unsure items, schedule) are in CLAUDE.md. Follow them.

1. For each project channel you watch, read what has happened since the last digest: Slack messages, linked Jira tickets, PRs, and Confluence or Google Docs changes.
2. Run the `timeline-check` skill for each project.
3. Collect items for every type in "What to flag". Drop anything already reported and unchanged.
4. On Mondays and Fridays, check the lead posted the weekly goals (Monday) or recap (Friday). If not by end of day, flag it. On Fridays, add each project's one-line status.
5. Anything that is blocking the team should already have gone out as an urgent ping. If you find one now, use `urgent-ping` first.
6. Write the digest per "Format": "Waiting on you" first, then one section per project with your on-track opinion and "Merged today", then "Questions for you" (one direct question for each Unsure item).
7. DM it to Wilbur. Nobody else. Do this on weekdays at 5:00 pm Eastern. If there is nothing to report, send nothing.
