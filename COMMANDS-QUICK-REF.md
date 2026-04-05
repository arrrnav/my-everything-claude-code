# Commands Quick Reference

> 48 slash commands. Type `/` in any Claude Code session to invoke.

---

## Core Workflow

| Command | What it does |
|---------|-------------|
| `/plan` | Restate requirements, assess risks, write step-by-step implementation plan — **waits for your confirm before touching code** |
| `/tdd` | Enforce test-driven development: scaffold interface → write failing test → implement → verify 80%+ coverage |
| `/code-review` | Full code quality, security, and maintainability review of changed files |
| `/build-fix` | Detect and fix build errors — delegates to the right build-resolver agent automatically |
| `/verify` | Run the full verification loop: build → lint → test → type-check |
| `/quality-gate` | Quality gate check against project standards |

---

## Testing

| Command | What it does |
|---------|-------------|
| `/tdd` | Universal TDD workflow (any language) |
| `/e2e` | Generate + run Playwright end-to-end tests, capture screenshots/videos/traces |
| `/test-coverage` | Report test coverage, identify gaps |

---

## Code Review

| Command | What it does |
|---------|-------------|
| `/code-review` | Universal code review |
| `/python-review` | Python — PEP 8, type hints, security, idiomatic patterns |
| `/santa-loop` | Adversarial dual-review — two independent reviewers must both approve before code ships |

---

## Feature Planning (PRP Workflow)

| Command | What it does |
|---------|-------------|
| `/prp-plan` | Analyse codebase and create a comprehensive feature implementation plan |
| `/prp-prd` | Generate a Product Requirements Document for a feature |
| `/prp-implement` | Execute a PRP implementation plan step-by-step |
| `/prp-commit` | Commit completed PRP work with structured commit message |
| `/prp-pr` | Open a pull request for a completed PRP feature |

---

## Planning & Architecture

| Command | What it does |
|---------|-------------|
| `/plan` | Implementation plan with risk assessment |
| `/orchestrate` | Guide for tmux/worktree multi-agent orchestration |

---

## Integrations

| Command | What it does |
|---------|-------------|
| `/jira` | Jira integration — create, update, and link issues from the terminal |

---

## Session Management

| Command | What it does |
|---------|-------------|
| `/save-session` | Save current session state to `~/.claude/session-data/` |
| `/resume-session` | Load the most recent saved session and resume from where you left off |
| `/sessions` | Browse, search, and manage session history |
| `/checkpoint` | Mark a checkpoint in the current session |
| `/aside` | Answer a quick side question without losing current task context |
| `/context-budget` | Analyse context window usage — find token overhead, optimise |

---

## Learning & Improvement

| Command | What it does |
|---------|-------------|
| `/learn` | Extract reusable patterns from the current session |
| `/learn-eval` | Extract patterns + self-evaluate quality before saving |
| `/evolve` | Analyse learned instincts, suggest evolved skill structures |
| `/promote` | Promote project-scoped instincts to global scope |
| `/instinct-status` | Show all learned instincts (project + global) with confidence scores |
| `/instinct-export` | Export instincts to a file |
| `/instinct-import` | Import instincts from a file or URL |
| `/skill-create` | Analyse local git history → generate a reusable skill |
| `/skill-health` | Skill portfolio health dashboard with analytics |
| `/rules-distill` | Scan skills, extract cross-cutting principles, distill into rules |

---

## Refactoring & Cleanup

| Command | What it does |
|---------|-------------|
| `/refactor-clean` | Remove dead code, consolidate duplicates, clean up structure |
| `/prompt-optimize` | Analyse a draft prompt and output an optimised version |
| `/prune` | Delete pending instincts older than 30 days that were never promoted |

---

## Docs & Research

| Command | What it does |
|---------|-------------|
| `/docs` | Look up current library/API documentation via Context7 |
| `/update-docs` | Update project documentation |
| `/update-codemaps` | Regenerate codemaps for the codebase |

---

## Loops & Automation

| Command | What it does |
|---------|-------------|
| `/loop-start` | Start a recurring agent loop on an interval |
| `/loop-status` | Check status of running loops |
| `/claw` | Start NanoClaw v2 — persistent REPL with model routing, skill hot-load, branching, and metrics |

---

## Project & Infrastructure

| Command | What it does |
|---------|-------------|
| `/projects` | List known projects and their instinct statistics |
| `/harness-audit` | Audit the agent harness configuration for reliability and cost |
| `/eval` | Run the evaluation harness |
| `/model-route` | Route a task to the right model (Haiku / Sonnet / Opus) |
| `/pm2` | PM2 process manager initialisation |
| `/setup-pm` | Configure package manager (npm / pnpm / yarn / bun) |

---

## Quick Decision Guide

```
Starting a new feature?             → /prp-plan or /plan, then /tdd
Code just written?                  → /code-review
High-stakes change?                 → /santa-loop
Build broken?                       → /build-fix
Need live docs?                     → /docs <library>
Session about to end?               → /save-session or /learn-eval
Resuming next day?                  → /resume-session
Context getting heavy?              → /context-budget then /checkpoint
Want to extract what you learned?   → /learn-eval then /evolve
Running repeated tasks?             → /loop-start
Jira ticket to file?                → /jira
```
