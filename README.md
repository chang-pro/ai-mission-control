# Mission Control — AI Agent Orchestration Dashboard

![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat-square&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Repo](https://img.shields.io/badge/Source-Private-orange?style=flat-square)

**A real-time dashboard for creating tasks, planning with AI, dispatching work to agents, and watching them execute.**

Forked from [**crshdn/mission-control**](https://github.com/crshdn/mission-control) — customized for my own AI agent workflow and project ecosystem.

---

## My Customizations

Took the original Mission Control and adapted it to work with my projects:

- Integrated with my OpenClaw setup for dispatching tasks to Claude Code and Codex agents
- Customized task templates and workflows for my specific projects (Ringora, trading bot, client sites)
- Adjusted the agent orchestration layer for my Mac Mini build server infrastructure

## Features

- **Task Management** — Create, prioritize, and organize tasks with full CRUD operations
- **AI Planning** — Use AI to break down complex tasks into actionable subtasks
- **Agent Dispatch** — Assign tasks to AI agents and monitor their progress in real-time
- **Live Monitoring** — Watch agents work with streaming status updates
- **OpenClaw Integration** — WebSocket connection to OpenClaw for AI agent orchestration
- **Docker Support** — One-command deployment with Docker Compose

## Architecture

```
┌──────────────────────────────────────────┐
│            Mission Control UI             │
│      Next.js 14 + React + TypeScript      │
└──────────────────┬───────────────────────┘
                   │
                   ▼
┌──────────────────────────────────────────┐
│             API Layer                     │
│    REST Endpoints + Server Actions        │
└──────────────────┬───────────────────────┘
                   │
          ┌────────┴────────┐
          ▼                 ▼
   ┌────────────┐   ┌─────────────┐
   │   SQLite   │   │  OpenClaw   │
   │  (Tasks,   │   │  Gateway    │
   │   State)   │   │  (Agents)   │
   └────────────┘   └─────────────┘
```

## Tech Stack

- **Framework:** Next.js 14 (App Router), TypeScript
- **Database:** SQLite (lightweight, zero-config)
- **AI Integration:** OpenClaw Gateway, Claude API, Codex CLI
- **Deployment:** Docker, Docker Compose
- **UI:** React with real-time state updates

## Credits

Originally built by [**crshdn**](https://github.com/crshdn/mission-control) — I forked it and customized it for my workflow.

## Skills Demonstrated

- Evaluating and extending open source software for personal use
- AI agent integration and orchestration patterns
- Real-time UI updates and streaming
- Docker containerization and deployment
- Adapting existing systems to custom infrastructure

---

> *This is a showcase page for a private repository. Source code available upon request for verified opportunities.*
