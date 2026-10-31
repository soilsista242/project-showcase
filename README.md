# AquaHolder Caribbean Trial Platform

Vite + React + TypeScript frontend for the **AquaHolder Caribbean 2026** programme (Soil Sista R&D Portal).

## Quick start (demo prototype)

```bash
cp .env.example .env.local
npm install
npm run dev
```

By default `VITE_ENABLE_DEMO_PROTOTYPE=true` and the existing clickable participant UI runs at http://127.0.0.1:5173/.

Set `VITE_ENABLE_DEMO_PROTOTYPE=false` to show the Phase 0 foundation shell only.

## Supabase (Phase 0–1)

1. Install Docker and the [Supabase CLI](https://supabase.com/docs/guides/cli).
2. From the repo root:

```bash
npx supabase start
npx supabase db reset
```

3. Copy the API URL and anon key from `npx supabase status` into `.env.local`.
4. Run RLS proofs:

```bash
npx supabase db execute --file supabase/tests/phase1_rls_tests.sql
```

See `docs/PHASE-0-1-FOUNDATION.md` and `docs/ARCHITECTURE-AND-IMPLEMENTATION-PLAN.md`.

## Scripts

| Command | Purpose |
|---------|---------|
| `npm run dev` | Dev server |
| `npm run build` | Typecheck + production build |
| `npm run preview` | Preview production build |
| `npm run lint` | Oxlint |
# project-showcase
