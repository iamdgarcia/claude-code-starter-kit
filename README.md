# Claude Code Starter Kit

**The fastest way to set up Claude Code correctly — secure, context-aware, and ready to code.**

A free template from [The Learning Curve](https://iamdgarcia.substack.com) — hands-on AI engineering, no hype.

---

## What's inside

| File | What it does |
|---|---|
| `CLAUDE.md` | Project instructions Claude reads every session — rules, architecture, current focus |
| `.claudeignore` | Stops Claude from reading secrets, build artifacts, and large binaries |
| `.claude/settings.json` | Global security permissions — blocks `.env` and credential files at the permission level |
| `file-tree.md` | Document your project structure so Claude understands it without reading every file |
| `docs.md` | Quick reference of your main functions — Claude reads this before touching any file |

---

## Why this matters

By default, Claude Code reads everything — including your `.env` files with real API keys.

This starter kit fixes that out of the box, and gives Claude enough context to actually understand your project instead of asking you to explain it every session.

**Without this kit:**
- Claude reads your secrets
- Claude asks "what does this project do?" every time
- Claude edits the wrong file because it doesn't know your structure
- You waste 10 prompts on context instead of code

**With this kit:**
- Secrets are blocked at the permission level
- Claude knows your architecture, rules, and current focus from session 1
- Your function reference means Claude finds existing code instead of rewriting it
- You spend prompts on the actual work

---

## Setup — 3 steps

**Step 1 — Copy this kit into your project root**

```bash
# Clone the starter kit
git clone https://github.com/iamdgarcia/claude-code-starter-kit my-project
cd my-project

# Or copy individual files into an existing project
cp CLAUDE.md .claudeignore docs.md file-tree.md /path/to/your/project/
mkdir -p .claude && cp .claude/settings.json /path/to/your/project/.claude/
```

**Step 2 — Fill in the blanks**

Open each file and replace the `[placeholder]` sections:

- `CLAUDE.md` → project name, stack, architecture, current focus
- `file-tree.md` → your actual directory structure
- `docs.md` → your main functions and where they live

Takes 15 minutes. Worth every second.

**Step 3 — Add to `.gitignore` if needed**

`.claude/settings.json` is safe to commit (no secrets). Add it to git so your team uses the same security config.

```bash
git add CLAUDE.md .claudeignore .claude/settings.json file-tree.md docs.md
git commit -m "chore: add Claude Code starter kit"
```

---

## Optional: global security config

To protect your secrets across **all** projects (not just this one), copy `settings.json` to your home directory:

```bash
mkdir -p ~/.claude
cp .claude/settings.json ~/.claude/settings.json
```

Claude Code will load this for every project automatically.

---

## Keeping it updated

The kit only works if you keep it current. Set a habit:

- **After adding a file** → update `file-tree.md`
- **After writing a shared function** → add it to `docs.md`
- **Starting a new feature** → update "Current Focus" in `CLAUDE.md`
- **Deploying to prod** → update "Stage" in `CLAUDE.md`

---

## What to build next

Once your Claude Code setup is solid, the next step is designing your agent before you code it.

→ **Agent Design Canvas** — the Notion template for planning agent persona, tools, memory, and failure modes before writing a single line. [Get it on Gumroad](https://iamdgarcia.gumroad.com)

→ **Agentic AI for Beginners** — free course covering agent loops, memory, RAG, multi-agent systems, and production. [Start here](https://github.com/iamdgarcia/tlc_agents_training)

→ **Agent Blueprints** — one-click deployable agent templates on Netlify. [Browse blueprints](https://github.com/iamdgarcia/the-learning-curve)

---

## From The Learning Curve

**[Subscribe on Substack](https://iamdgarcia.substack.com)** — hands-on AI engineering projects, no hype.

**[YouTube](https://www.youtube.com/@TheLearningCurveAI)** — video walkthroughs and deep-dives.

**[GitHub](https://github.com/iamdgarcia/the-learning-curve)** — all blueprints, courses, and projects.

---

*MIT License — fork it, adapt it, ship it.*
