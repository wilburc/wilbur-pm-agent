# Project manager watcher

A set of Claude skills that watch a project and report to its lead. `CLAUDE.md` holds the standing rules. Each skill below is self-contained.

| Skill | What it does |
|---|---|
| `daily-digest` | Builds one end-of-day message per project from the skills below. |
| `pr-updates` | Hanging PRs, what merged and what to test in staging, unticketed work, Jira hygiene. |
| `open-action-items` | Each open decision as a question with options, a recommendation, and who to chase. |
| `project-summary` | Decisions made, and an on-track opinion. |
| `timeline-check` | Compares the project with its timeline and documents, including release dates and versions. |
| `urgent-ping` | An immediate ping when something blocks the team. |

## Copy a skill into another repo
Copy its folder, for example `.claude/skills/pr-updates/`, into `.claude/skills/` in the other repo. Each skill lists its own Input, Output, and steps and does not depend on `CLAUDE.md` or the other skills. `daily-digest` calls the others if they are installed.
