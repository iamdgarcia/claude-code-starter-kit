# File Tree — [Project Name]

> Keep this updated. Claude uses it to understand your project structure
> without reading every file. Update it after adding or moving files.
> 
> Tip: generate with `find . -not -path '*/node_modules/*' -not -path '*/.git/*' | sort`

```
project-root/
│
├── CLAUDE.md                    ← Claude Code instructions (this project's rules)
├── .claudeignore                ← Files Claude should never read
├── .claude/settings.json        ← Global security permissions
├── file-tree.md                 ← This file
├── docs.md                      ← Function/module reference
│
├── README.md                    ← Project overview for humans
├── .env.example                 ← Required env vars (no real values)
│
├── src/                         ← Main source code
│   ├── components/              ← [describe: e.g. React UI components]
│   │   ├── Header.tsx
│   │   └── ...
│   ├── pages/                   ← [describe: e.g. Next.js route pages]
│   │   ├── index.tsx
│   │   └── api/
│   │       └── ...
│   ├── lib/                     ← [describe: e.g. shared utilities, API clients]
│   │   ├── supabase.ts          ← Supabase client (service role)
│   │   ├── stripe.ts            ← Stripe client
│   │   └── utils.ts             ← General helpers
│   └── types/                   ← TypeScript type definitions
│       └── index.ts
│
├── backend/                     ← [if separate backend exists]
│   ├── main.py                  ← FastAPI app entry point
│   ├── routers/                 ← Route handlers
│   ├── models/                  ← DB models / Pydantic schemas
│   └── utils/                   ← Backend helpers
│
├── tests/                       ← Test files
│   ├── unit/
│   └── integration/
│
├── public/                      ← Static assets
└── docs/                        ← Documentation
```

---

## Key Directories Explained

| Directory | Purpose | Who touches it |
|---|---|---|
| `src/components/` | [describe] | Frontend work |
| `src/lib/` | [describe] | Shared across frontend/backend |
| `backend/routers/` | [describe] | API endpoints only |
| `tests/` | [describe] | Any feature change |

---

## Off-Limits Directories

| Directory | Reason |
|---|---|
| `legacy/` | Deprecated — do not modify |
| `node_modules/` | Auto-generated — never edit |

---

*Last updated: [date]*
