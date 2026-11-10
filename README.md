# Project manager watcher

Claude skills that watch a project and report to its lead. `CLAUDE.md` holds the standing rules (and environment details such as Figma access). Each skill below is self-contained.

| Skill | What it does |
|---|---|
| `daily-digest` | Builds one end-of-day message per project from the skills below. |
| `pr-updates` | Hanging PRs, what merged and what to test, end goal vs staging, unticketed work, Jira hygiene. |
| `open-action-items` | Each open decision that is the lead's call as a terse numbered question; others become status lines with a named owner. Full detail on request. |
| `project-summary` | Decisions made, and an on-track opinion. |
| `timeline-check` | Compares the project with its timeline and documents, including release dates and versions. |
| `urgent-ping` | An immediate ping when something blocks the team and needs the lead (or the lead should know who owns the unblock). |

## Copy a skill into another repo
Copy its folder, for example `.claude/skills/pr-updates/`, into `.claude/skills/` in the other repo. Each skill lists its own Input, Output, and steps and does not depend on `CLAUDE.md` or the other skills. `daily-digest` calls the others if they are installed.
