# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Communication rules

- Luôn trả lời bằng tiếng Việt có dấu.
- Trả lời ngắn gọn, dễ hiểu.
- Không dùng từ ngữ kỹ thuật, trừ khi người dùng chỉ định.
- Xưng hô: tự xưng "tôi", gọi người dùng là "bạn".

## Project status

This repository (`gpa-tracker`, remote `origin` → `github.com/datdinh66/new-track`) has only been scaffolded from a template. There is no application code, package manifest, build system, linter, or test suite yet, so there are no build/lint/test commands. The `.gitignore` anticipates a JavaScript/Node front-end toolchain (Vite/Next/Nuxt/SvelteKit output dirs) with optional Python helper scripts, but no stack has been chosen. When a stack is added, update this file with its commands (including how to run a single test) and the architecture.

## Development process (Waterfall)

The project follows the waterfall model. Finish each phase before starting the next:

1. **Requirements** — `PRD.md` is the source of truth for what to build.
2. **Business flow design** — draw the business flows as Mermaid `flowchart` diagrams, derived from `PRD.md`.
3. **Implementation & automated testing** — build the features and write automated tests.
4. **User acceptance testing** — done by the user; wait for their confirmation before moving on.
5. **Deploy** — deploy to Vercel.

Tracking files (keep them up to date):

- `PLAN.md` — project plan by phase, with the tasks in each phase.
- `STATUS.md` — current phase and progress, technical decisions (with reasons), and changes compared with the original plan/PRD. Update it whenever a phase changes, a decision is made, or the plan deviates.

## Workflow conventions

Project slash commands live in `.claude/commands/` and define the expected git workflow:

- `/git-branch <name>` — branch off `main` using feature/bug naming (e.g. `feature/...`, `bugfix/...`). Do work on branches, not directly on `main`.
- `/commit` — commit with a message summarizing the changes.
- `/merge` — merge the current branch into `main`: require a clean working tree, `git pull origin main` first, and ask the user before resolving conflicts.
- `/push <branch>` — confirm with the user before pushing to `main`.
- `/learn-by-mistake` — record mistakes and fixes in `common_errors.md`, grouped by error category (create the file if missing).
- `/wrap-up` — at session end, log issues via `/learn-by-mistake` and update the **Project structure** section below (level 1–2 only).
- `/new-project` — only for cloning the template into a fresh project; do not run it here now that the project exists.

## Project structure

- `.claude/commands/` — project slash commands (git workflow, session wrap-up)
- `.gitignore`
- `CLAUDE.md`
- `PLAN.md` — project plan by phase
- `STATUS.md` — current status, technical decisions, changes from the original plan
