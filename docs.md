# Docs — [Project Name]

> Quick reference for Claude and new contributors.
> List your main functions, their location, and what they do.
> Claude reads this BEFORE touching any file, so keep it accurate.
> 
> Rule: if you add a function that other files might call, add it here.

---

## Authentication

| Function | File | Description |
|---|---|---|
| `getUser()` | `src/lib/auth.ts` | Returns current authenticated user or null |
| `requireAuth()` | `src/lib/auth.ts` | Middleware — throws 401 if no session |
| `signOut()` | `src/lib/auth.ts` | Clears session and redirects to /login |

---

## Database

| Function | File | Description |
|---|---|---|
| `supabase` | `src/lib/supabase.ts` | Supabase client (use this, not a new instance) |
| `getUserById(id)` | `src/lib/db/users.ts` | Fetch user row by UUID |
| `createRecord(table, data)` | `src/lib/db/records.ts` | Insert with validation |

---

## API Routes

| Endpoint | File | Description |
|---|---|---|
| `POST /api/chat` | `src/pages/api/chat.ts` | Main LLM call — accepts {message, history} |
| `GET /api/user` | `src/pages/api/user.ts` | Returns current user profile |
| `POST /api/webhook` | `src/pages/api/webhook.ts` | Stripe webhook handler |

---

## UI Components

| Component | File | Props |
|---|---|---|
| `<ChatWindow>` | `src/components/ChatWindow.tsx` | `{messages, onSend}` |
| `<Header>` | `src/components/Header.tsx` | `{user}` |
| `<Button>` | `src/components/ui/Button.tsx` | `{variant, onClick, children}` |

---

## Utilities

| Function | File | Description |
|---|---|---|
| `formatDate(date)` | `src/lib/utils.ts` | ISO string → "Jan 12, 2025" |
| `truncate(str, n)` | `src/lib/utils.ts` | Truncate string to n chars with ellipsis |
| `sleep(ms)` | `src/lib/utils.ts` | Promise-based delay |

---

## Backend (if applicable)

| Function | File | Description |
|---|---|---|
| `get_user(id, db)` | `backend/routers/users.py` | Fetch user from DB |
| `call_llm(prompt, model)` | `backend/utils/llm.py` | Wrapper for Anthropic/OpenAI call |
| `validate_input(data)` | `backend/utils/validation.py` | Pydantic input validation |

---

## Environment Variables

| Variable | Where used | Required |
|---|---|---|
| `ANTHROPIC_API_KEY` | `backend/utils/llm.py` | Yes |
| `SUPABASE_URL` | `src/lib/supabase.ts` | Yes |
| `SUPABASE_ANON_KEY` | `src/lib/supabase.ts` | Yes |
| `STRIPE_SECRET_KEY` | `src/pages/api/webhook.ts` | Only for payments |

See `.env.example` for the full list.

---

## Known Gotchas

- [e.g. "The Supabase client uses service role — never expose to the browser"]
- [e.g. "Rate limit: 100 req/min on /api/chat — add delays to batch calls"]
- [e.g. "Stripe webhook must verify signature — don't skip `constructEvent()`"]

---

*Last updated: [date]*
