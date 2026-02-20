# Server Monitor Hub — Central Entry Point

Multi-frontend dashboard for monitoring heterogeneous servers.

## Ecosystem Layout

| Repo | Path | Purpose |
|------|------|---------|
| **monitor** | `~/monitor` | Specs, documentation, orchestration hub |
| **server-monitor** | `~/server-monitor` | Python web dashboard + Terminal TUI (port 9860) |
| **server-monitor-ios** | `~/server-monitor-ios` | SwiftUI iOS companion + WidgetKit |

There is NO runnable code in this repo. All executable work happens in the satellite repos.

## Cross-Project Integration

This dashboard monitors servers from other ecosystems. When those projects change:

| Change | Action |
|--------|--------|
| Engine port changes from 9847 | Update `config/servers.yaml` in server-monitor |
| Nagzerver port changes from 9800 | Update `config/servers.yaml` in server-monitor |
| OBO server port changes from 9810 | Update `config/servers.yaml` in server-monitor |
| New server added to any ecosystem | Add entry to `config/servers.yaml` |
| METRICS_SPEC.md format changes | Update collectors in server-monitor |
