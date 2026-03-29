# Look For Work

A proactive codebase analysis agent that scans for the highest-impact improvement opportunities across architecture, security, performance, testing, code quality, and more.

## Usage

```
look-for-work                   # Full codebase analysis
look-for-work security          # Focus on a specific area
look-for-work "the auth flow"   # Focus on a specific concern
```

## How It Works

This agent runs in 4 phases:

1. **Reconnaissance** — Explores the project structure, identifies the stack, reads docs, checks git history, and maps critical areas
2. **Deep Analysis** — Dispatches 6 specialized agents in parallel across two waves
3. **Synthesis & Prioritization** — Deduplicates, cross-references, and prioritizes all findings
4. **Report** — Delivers a structured Codebase Health Report

See `commands/look-for-work.md` for the full workflow and `agents/` for the 6 specialized analyst prompts.
