# Mission Control — AI Agent Orchestration Dashboard

![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat-square&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Repo](https://img.shields.io/badge/Source-Private-orange?style=flat-square)

**A real-time dashboard for creating tasks, planning with AI, dispatching work to agents, and watching them execute.** Think project management meets AI orchestration.

---

## Features

- **Task Management** — Create, prioritize, and organize tasks with full CRUD operations
- **AI Planning** — Use AI to break down complex tasks into actionable subtasks
- **Agent Dispatch** — Assign tasks to AI agents and monitor their progress in real-time
- **Live Monitoring** — Watch agents work with streaming status updates
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
   │   SQLite   │   │  AI Agents  │
   │  (Tasks,   │   │  (Claude,   │
   │   State)   │   │   Codex)    │
   └────────────┘   └─────────────┘
```

## Tech Stack

- **Framework:** Next.js 14 (App Router), TypeScript
- **Database:** SQLite (lightweight, zero-config)
- **AI Integration:** Claude API, Codex CLI
- **Deployment:** Docker, Docker Compose
- **UI:** React with real-time state updates

## Skills Demonstrated

- Full-stack application architecture
- AI agent integration and orchestration patterns
- Real-time UI updates and streaming
- Docker containerization and deployment
- Task queue and state management design

---

> *This is a showcase page for a private repository. Source code available upon request for verified opportunities.*
