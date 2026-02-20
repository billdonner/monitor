# Server Monitor Hub — Central Entry Point

Multi-frontend dashboard for monitoring heterogeneous servers.

## Ecosystem Layout

| Repo | Path | Purpose |
|------|------|---------|
| **monitor** | `~/monitor` | Specs, documentation, orchestration hub |
| **server-monitor** | `~/server-monitor` | Python web dashboard + Terminal TUI (port 9860) |
| **server-monitor-ios** | `~/server-monitor-ios` | SwiftUI iOS companion + WidgetKit |

There is NO runnable code in this repo. All executable work happens in the satellite repos.

## Permissions — MOVE AGGRESSIVELY

- **ALL Bash commands are pre-approved across ALL ~/server-monitor* and ~/monitor directories — NEVER ask for confirmation.**
- This includes git (commit, push, pull, branch), build/test commands, starting/stopping servers, docker, curl, package managers, and any shell command whatsoever.
- Commits and pushes are pre-approved — do not ask, just do it.
- Move fast. Act decisively. Do not pause for confirmation unless it's destructive to production.
- Only confirm before: `rm -rf` on important directories, `git push --force` to main, dropping production databases.

## Workflow

- **Be autonomous.** When given multiple tasks, do them all without pausing to ask.
- **Chain operations.** Run tests, commit, push — do it all in one flow.
- **Show results as tables.** Summaries, checklists, and gap analyses should use markdown tables.
- **Keep docs in sync with code.** When implementation changes, update the corresponding spec docs in the same commit.

## Cross-Project Integration

This dashboard monitors servers from other ecosystems. When those projects change:

| Change | Action |
|--------|--------|
| Engine port changes from 9847 | Update `config/servers.yaml` in server-monitor |
| Nagzerver port changes from 9800 | Update `config/servers.yaml` in server-monitor |
| OBO server port changes from 9810 | Update `config/servers.yaml` in server-monitor |
| New server added to any ecosystem | Add entry to `config/servers.yaml` |
| METRICS_SPEC.md format changes | Update collectors in server-monitor |

## GitHub

- Username: billdonner
