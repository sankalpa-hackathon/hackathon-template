# Architecture (Simple Flow)

Keep this page short and visual. Update docs/architecture.png with a clean diagram that matches the flow below.

## One-Glance Flow
- **User** -> opens the app (web or mobile)
- **Frontend** -> validates input, shows UI, calls backend via HTTPS
- **Backend/API** -> handles auth, business logic, rate limits
- **Services / DB / LLM** -> stores data, runs queries, calls external APIs/AI
- **Response** -> backend returns result, frontend displays success or error

## What to Fill In
- **Frontend**: framework, hosting, state management, key libraries.
- **Backend**: language/framework, main endpoints, background jobs (if any).
- **Data**: database type, ORM/migrations, backups/retention, what PII is stored.
- **External APIs/LLMs**: names and why you use them.
- **Auth**: signup/login method, session/JWT strategy, roles/permissions.

## Reliability Quick Notes
- Logging/metrics: where you send them (console, cloud logs).
- Timeouts/retries/rate limits: values or defaults.
- Error handling: what the user sees; fallbacks (cached value, friendly message).

## Risks to Call Out
- Top 3 risks (e.g., latency from LLM/API, data quality, cost). Add one-line mitigations.

## Deploy (Keep It Simple)
- Host anywhere (Vercel, Netlify, Render, Fly, Railway, etc.) — pick what you know.
- Single environment is fine for a hackathon; just note the URL.
- Manual deploy is OK; no CI/CD or rollback plan required here.