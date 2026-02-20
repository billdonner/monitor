# Server Monitor

A multi-frontend dashboard for monitoring heterogeneous servers (HTTP, Redis, PostgreSQL). Three frontends share the same backend collectors and config.

## Ecosystem

| Repo | Stack | Purpose |
|------|-------|---------|
| [monitor](https://github.com/billdonner/monitor) | Docs | Specs, documentation, orchestration hub |
| [server-monitor](https://github.com/billdonner/server-monitor) | Python / FastAPI / Textual | Web dashboard + Terminal TUI (port 9860) |
| [server-monitor-ios](https://github.com/billdonner/server-monitor-ios) | SwiftUI / WidgetKit | iOS companion app + widget |

## What It Monitors

| Service | Type | Port |
|---------|------|------|
| Alities Engine | HTTP /metrics | 9847 |
| Nagzerver | HTTP /metrics | 9800 |
| OBO Server | HTTP /metrics | 9810 |
| Server Monitor (self) | HTTP /metrics | 9860 |
| Redis | Native protocol | 6379 |
| Postgres (Nagz) | Native protocol | 5433 |

## Documentation

See [Docs/](Docs/) for specs and architecture docs.

## Features

- **Three frontends**: Web (browser), Terminal (Textual TUI), iOS (SwiftUI + WidgetKit)
- **Red/green status banner**: Aggregate health at a glance across all frontends
- **Error highlighting**: Red border on unreachable server panels
- **Mini player**: Compact status-bar mode for web and terminal
- **LAN access**: Detects and displays LAN IP for cross-device monitoring
- **Cloudflare tunnel**: Quick tunnel support for remote access
