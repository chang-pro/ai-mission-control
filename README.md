# Mission Control — AI Agent Orchestration Dashboard

![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat-square&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Repo](https://img.shields.io/badge/Source-Private-orange?style=flat-square)

**I took [crshdn's Mission Control](https://github.com/crshdn/mission-control) and turned it into the central hub for all my AI agent operations.** Create tasks, plan with AI, dispatch to agents, and watch them execute in real-time.

---

## Why I Needed This

I run Claude Code, Codex, and custom agents across multiple projects. Without a dashboard, it was chaos — agents running in random terminals, no visibility into what's happening, no way to queue work. Mission Control gave me a visual interface to orchestrate all of it.

## What I Customized

The original Mission Control is a great foundation. Here's what I built on top:

### OpenClaw Gateway Integration
- Connected Mission Control to my **OpenClaw setup** via WebSocket
- Tasks created in the dashboard can be dispatched directly to Claude Code or Codex on my Mac Mini build server
- Real-time streaming of agent output back to the dashboard — I can watch agents work live

### Custom Task Templates for My Projects
- Pre-built task templates for common operations across my projects:
  - *"Bug fix in Ringora"* → auto-loads project context and dispatches
  - *"Run trading bot backtest with config X"* → dispatches with the right parameters
  - *"Deploy Orleans Cleaning to Vercel"* → runs the full deploy pipeline
- Each template knows which project it belongs to, what context to load, and which agent to use

### Agent Monitoring & History
- Dashboard shows all running agents, their current task, and real-time output
- Full history of completed tasks with logs, duration, and outcomes
- Failed tasks are flagged with error context for quick debugging

### Docker Deployment
- Containerized the whole setup with Docker Compose for easy deployment on my build server
- Single `docker compose up` to get the full dashboard running

## Architecture

```
┌──────────────────────────────────────────┐
│            Mission Control UI             │
│   Task Board │ Agent Monitor │ History    │
│      Next.js 14 + React + TypeScript      │
└──────────────────┬───────────────────────┘
                   │ WebSocket
                   ▼
┌──────────────────────────────────────────┐
│           OpenClaw Gateway                │
│    Agent Dispatch │ Task Queue │ Logs     │
└──────────────────┬───────────────────────┘
                   │
          ┌────────┴────────┐
          ▼                 ▼
   ┌────────────┐   ┌─────────────┐
   │   SQLite   │   │  AI Agents  │
   │  (Tasks,   │   │  Claude Code│
   │   History) │   │  Codex CLI  │
   └────────────┘   └─────────────┘
```

## Tech Stack

`Next.js 14` · `TypeScript` · `SQLite` · `WebSocket` · `Docker` · `OpenClaw Gateway` · `Claude API` · `Codex CLI`

## Credits

Forked from [**crshdn/mission-control**](https://github.com/crshdn/mission-control). I customized it with my OpenClaw integration, project-specific task templates, and agent monitoring.

---

> *Closed source. Source code available for serious inquiries.*
