# Claude Code — Project Instructions

> This file is automatically loaded by Claude Code at the start of every session.
> Keep it updated as your project evolves. The better this file, the better Claude performs.

---

## Project Overview

**Name:** [Your Project Name]
**Stack:** [e.g. Next.js + FastAPI + Supabase]
**Purpose:** [One sentence: what this project does]
**Stage:** [e.g. MVP / Beta / Production]

---

## Architecture

[Describe your high-level architecture here. Example:]

```
Frontend (React/Vite) → API (FastAPI) → Database (Postgres/Supabase)
                                      → External APIs (Stripe, etc.)
```

Key files to understand the codebase:
- `file-tree.md` — full project structure
- `docs.md` — main functions and where to find them

---

## Coding Rules

- **Language:** [e.g. TypeScript strict mode / Python 3.11+]
- **Style:** [e.g. Prettier + ESLint / Black + Ruff]
- **Tests:** [e.g. Pytest / Vitest — run before committing]
- **Commits:** Conventional commits (`feat:`, `fix:`, `docs:`, `chore:`)

### DO
- Read `docs.md` before touching any shared utility
- Keep files under 300 lines — split if larger
- Write one function per concern
- Update `docs.md` and `file-tree.md` after adding new files

### DO NOT
- Read or process `.env` files — they contain real secrets
- Modify `package-lock.json` or `poetry.lock` directly
- Add dependencies without asking first
- Touch files outside the scope of the current task

---

## Security Rules

- **NEVER** read, log, or repeat the contents of `.env`, `.env.*`, `*.pem`, `*.key`
- **NEVER** suggest hardcoding API keys or secrets in source files
- **STOP** immediately if you encounter credentials and tell the user
- All secrets go in `.env.local` (dev) or environment variables (prod)

---

## Current Focus

[Update this section every session. Tell Claude what you're working on:]

- Working on: [feature / bug / refactor]
- Do not touch: [file or module currently off-limits]
- Known issues: [anything Claude should be aware of]

---

## Project-Specific Context

[Add anything Claude needs to know that isn't obvious from the code:]

- [e.g. "The `legacy/` folder is deprecated — don't touch it"]
- [e.g. "We use Supabase RLS — all queries must go through the service role client"]
- [e.g. "The API rate limit is 100 req/min — add delays to batch operations"]

---

## Useful Commands

```bash
# Install deps
npm install / pip install -r requirements.txt

# Run dev
npm run dev / uvicorn main:app --reload

# Run tests
npm test / pytest

# Lint
npm run lint / ruff check .

# Build
npm run build
```

---

*Last updated: [date] by [you]*
