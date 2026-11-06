---
name: pr-updates
description: Report on a project's pull requests and Jira board. Covers PRs that are hanging, what merged today and what to test in staging, work that is scoped but has no ticket, and tickets that are missing from the epic, unclear, mislabeled, or out of date. Use for a PR status update or a board check.
---

# PR updates

## Input
- The project's Slack channel.
- Where the plan lives: PRD and eng spec links, and the Jira epic.
- Read access to GitHub, Jira, and Slack. Optional: a deploy system (for example Jenkins) to confirm what is in staging.

## Output
Numbered fragments, one line each, one link last. Leave out empty sections.
1. **Hanging PRs**: what it does, why it matters, quiet for how long. [PR]
2. **Test in staging now**: one line per flow: who does what where, what to check. [PR or ticket] A ticket number or title is never the item itself.
3. **Merged, not in staging yet**: what changed, "not in staging yet" or "staging status unknown", what you checked. [PR]
4. **Not ticketed**: scoped work or PRs with no ticket. [source section]
5. **Board hygiene**: not under the epic, no clear version, unclear, blocked, or out of date. [ticket]

## Steps
1. Read recent Slack, open and merged PRs, and the Jira epic and its tickets.
2. Hanging PRs: a PR that sits open with no comments and no other activity. Judge each PR on its own, not by a fixed number of days. Say how long it has been quiet.
3. Quality: flag PRs merged with failing or no tests or with unaddressed review comments, bugs reported or regressions discussed, hotfixes, rushed or skipped QA, and open bug tickets on the critical path.
4. Merged today: list the functionality merged that day, in user-facing terms. Mark an item in staging only when the deploy containing the merge commit is confirmed (the deploy system (for example Jenkins, through its connector), staging deploy info, or release notes, where readable). Otherwise say "not in staging yet" or "staging status unknown" and what you checked. For an item behind a flag, give the flag name and say it must be enabled to test. If nothing merged, leave the section out.
5. Not ticketed: all work must be ticketed. Flag work described in the PRD, eng spec, channel, or an open PR that has no ticket, and PRs with no linked ticket.
6. Epic and versions: every ticket should be under the project's epic. If the project has no epic, flag that. If the project has versions (V1/V2, phases), each ticket must state its version, in its name or by living under a per-version epic. Flag tickets with no clear version, or a version that disagrees with the PRD or spec. Link the ticket and the PRD section.
7. Clarity and ownership: flag vague tickets, tickets with no description or acceptance criteria, and tickets with no owner, and say what is unclear. Flag blocked tickets and unassigned tickets on the critical path, and how long each has been stuck.
8. Jira status: if someone says in the channel that a ticket is merged, done, or released, check the ticket. If it is still in an earlier column (for example In Progress), flag it with the ticket link and the Slack message.

## Rules
- Read-only. Never post, comment, edit, or create anything in Slack, Jira, GitHub, or any doc. Only read deploy info; never trigger, rebuild, or change anything.
- Style: terse fragments, no full sentences. Numbered items so the lead can cite them by number. Key facts only, ONE link per item (the exact section), placed last. Plain words: say what it means first; no jargon, ticket numbers, or code names in the lead; define a technical term if unavoidable.
- When the lead asks to expand item N, give the full detail then: what and why, options with tradeoffs, your recommendation (marked opinion), what happens if nobody decides, who decides, links.
- If you can't tell, mark it "Unsure" and list the facts. Don't report an item twice; if it changed, say what changed.
