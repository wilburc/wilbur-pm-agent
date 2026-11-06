---
name: timeline-check
description: Check whether a project is on track by comparing recent activity and the weekly goals with its agreed timeline and source-of-truth documents. Covers timeline slips, date drift, release readiness, version alignment, document divergence, scope creep, risks, and communication gaps. Use before a digest or when asked if a project is on track.
---

# Timeline check

## Input
- The agreed timeline (board or schedule) and the supporting docs: PRD, eng spec, Jira epic.
- The project's Slack channel.
- Release dates, if the PRD has any.

## Output
Numbered fragments, one line each, one link last:
1. **On-track opinion**: on track or at risk, how sure, why. On Fridays, a one-line status and whether it moved since last week.
2. **Findings**: `N.` per check below. Mark uncertain items "Unsure" with the facts.

## Steps
1. Find the timeline and docs. If none, say so and ask. Don't guess. Use the timeline only for milestones and dates, not for who is assigned.
2. Read them, then recent Slack, Jira, and PRs.
3. Check:
   - **Timeline**: late or stalled milestones and tickets. Say why it may be off track.
   - **Timeline visibility**: a change, slip, or new risk discussed in Slack or implied by the work but not yet in the timeline, Jira, PRD or spec, or announced in the channel. Also when the weekly goals or recap show different dates than the timeline.
   - **Date drift**: a date in Slack that differs from the timeline, PRD, spec, or Jira, or a document gone stale.
   - **Release readiness**: for every release date in the PRD (internal, GA, per-version), check it is announced in the channel (cite the message, or flag that it isn't); it matches the timeline (say what the timeline shows, which may be estimates rather than dates, and flag mismatches with the PRD section and timeline item); your on-track opinion for hitting it with confidence and reason, based on goals, open tickets, and PR state; and that its tickets are done, PRs are merged, a QA ticket exists, and the date is stated. Flag conflicts with release freezes or other stated dates.
   - **Divergence**: work or talk that departs from a document, or documents that disagree.
   - **Version alignment**: where versions (V1/V2, phases, releases) are defined (PRD, Slack, Jira fix versions or labels, the timeline), the PRD, eng spec, Jira, and design files must agree on what is in each version. Flag an item in different versions in different places, in a version in one place and absent in another, or in no version. If a Figma link matters: Figma can't be read, so say "Figma link not read", include the link, don't describe or guess at its contents, and add a "Questions for you" item asking the lead to check the Figma version scope himself.
   - **Scope creep**: work or requests beyond what the docs describe.
   - **Risks**: anything that could threaten the timeline or the plan, such as dependencies, blockers, unanswered questions.
   - **Communication**: a channel silent while work is in flight, no stakeholder update before a release or milestone, or a change stakeholders outside the channel need to know.
4. If you suspect the timeline is off track, write one or two lines on why, with links, plus any context that helps the lead decide. Give the reason and a little context.
5. Weekly goals: each project lead posts goals on Monday and a recap on Friday. If either is missing by end of day, flag it. Only the current week's goals (latest Monday post) count; ignore earlier weeks. With no Monday post, use the previous Friday's "next week" list, flag any unclear items, and still flag the missing post. A good goal can be verified ("finish ticket X", not "make progress on Y"); flag vague goals and say what is unclear.

## Rules
- Read-only. Never post, comment, or edit anything.
- Style: terse fragments, no full sentences. Numbered items so the lead can cite them by number. Key facts only, ONE link per item (the exact section), placed last. Plain words: say what it means first; no jargon, ticket numbers, or code names in the lead; define a technical term if unavoidable.
- When the lead asks to expand item N, give the full detail then: what and why, options with tradeoffs, your recommendation (marked opinion), what happens if nobody decides, who decides, links.
- Link the exact section of each document involved (heading anchor, message link, ticket, or PR file and line) and quote or name the passage in a few words; if a section link isn't possible, name the heading. For a finding about two documents, one link per side.
- Don't report an item twice; if it changed, say what changed.
