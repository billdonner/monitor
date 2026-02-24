# Server Monitor

A multi-frontend dashboard for monitoring heterogeneous servers (HTTP, Redis, PostgreSQL). Three frontends share the same backend collectors and config.

## What It Monitors

| Service | Type | Port |
|---------|------|------|
| card-engine | HTTP /metrics | 9810 |
| Nagzerver | HTTP /metrics | 9800 |
| Server Monitor (self) | HTTP /metrics | 9860 |
| Redis | Native protocol | 6379 |
| Postgres (Nagz) | Native protocol | 5433 |

## Features

- **Three frontends**: Web (browser), Terminal (Textual TUI), iOS (SwiftUI + WidgetKit)
- **Red/green status banner**: Aggregate health at a glance across all frontends
- **Error highlighting**: Red border on unreachable server panels
- **Mini player**: Compact status-bar mode for web and terminal
- **LAN access**: Detects and displays LAN IP for cross-device monitoring
- **Cloudflare tunnel**: Quick tunnel support for remote access

## Documentation

See [Docs/](Docs/) for specs and architecture docs.

## All Projects

### Server Monitor — Multi-frontend server dashboard

| Repo | Description | Port |
|------|-------------|------|
| [monitor](https://github.com/billdonner/monitor) | **This repo** — specs, docs, orchestration hub | — |
| [server-monitor](https://github.com/billdonner/server-monitor) | Python web dashboard + Terminal TUI | 9860 |
| [server-monitor-ios](https://github.com/billdonner/server-monitor-ios) | SwiftUI iOS + WidgetKit companion | — |

### Nagz — AI-mediated nagging/reminder app

| Repo | Description | Port |
|------|-------------|------|
| [nagz](https://github.com/billdonner/nagz) | Hub — specs, docs, orchestration | — |
| [nagzerver](https://github.com/billdonner/nagzerver) | Python API server | 9800 |
| [nagz-web](https://github.com/billdonner/nagz-web) | TypeScript/React web app | 5173 |
| [nagz-ios](https://github.com/billdonner/nagz-ios) | SwiftUI iOS app + Apple Intelligence | — |

### OBO — Flashcard learning app

| Repo | Description | Port |
|------|-------------|------|
| [obo](https://github.com/billdonner/obo) | Hub — specs, docs, orchestration | — |
| [card-engine](https://github.com/billdonner/card-engine) | Unified flashcard + trivia backend | 9810 |
| [obo-gen](https://github.com/billdonner/obo-gen) | Swift CLI deck generator | — |
| [obo-ios](https://github.com/billdonner/obo-ios) | SwiftUI iOS flashcard app | — |

### Alities — Trivia game platform

| Repo | Description | Port |
|------|-------------|------|
| [alities](https://github.com/billdonner/alities) | Hub — specs, docs, orchestration | — |
| [card-engine](https://github.com/billdonner/card-engine) | Unified backend (trivia + ingestion) | 9810 |
| [alities-studio](https://github.com/billdonner/alities-studio) | React/TypeScript game designer | 9850 |
| [alities-mobile](https://github.com/billdonner/alities-mobile) | SwiftUI iOS game player | — |
| [alities-trivwalk](https://github.com/billdonner/alities-trivwalk) | Python TrivWalk trivia game | — |

### Standalone Tools

| Repo | Description |
|------|-------------|
| [claude-cli](https://github.com/billdonner/claude-cli) | Swift CLI for the Claude API |
| [Flyz](https://github.com/billdonner/Flyz) | Fly.io deployment configs for all servers |
