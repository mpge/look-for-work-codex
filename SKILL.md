---
name: look-for-work
description: Proactive codebase analysis agent that scans for the highest-impact improvement opportunities across architecture, security, performance, testing, code quality, and more. Use when asked to "look for work", audit a codebase, or find what to fix next.
metadata:
  short-description: Proactive codebase analysis across 15 dimensions
---

# Look For Work

Proactively scan this codebase and identify the highest-impact improvement opportunities, then present an actionable prioritized roadmap.

> If you owned this codebase, what would you fix first?

## Workflow

Run the full analysis from `commands/look-for-work.md`. It executes in 4 phases:

1. **Reconnaissance** — Explore the project structure, stack, docs, git history, and critical areas
2. **Deep Analysis** — Dispatch 6 specialist agents in parallel (see `agents/`)
3. **Synthesis** — Deduplicate, cross-reference, and prioritize findings (P0-P3)
4. **Report** — Deliver a structured Codebase Health Report

## Agents

Each agent in `agents/` covers a specific dimension:

| Agent | Focus |
|-------|-------|
| `architecture-analyst` | SOLID, coupling, modularization, boundaries |
| `security-analyst` | OWASP Top 10 audit |
| `performance-analyst` | N+1, memory, blocking ops, caching, algorithms |
| `quality-analyst` | Code smells, refactor ROI |
| `reliability-analyst` | Tests, concurrency, observability, deployment |
| `landmine-detector` | Hidden bugs, edge cases, production failures |

## Priority Matrix

| Priority | Criteria |
|----------|----------|
| **P0 — Fix Now** | Security vulnerabilities, data loss risks, production landmines |
| **P1 — Fix Soon** | Performance bottlenecks, reliability gaps, test coverage holes |
| **P2 — Plan For** | Architecture improvements, high-ROI refactors |
| **P3 — Backlog** | Code quality improvements, nice-to-haves |

## Usage

If the user specifies a focus area, weight all agent prompts toward that area.
