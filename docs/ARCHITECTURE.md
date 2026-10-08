# Architecture — mubaidjavaid Portfolio

## Intent

Portfolio site for M Ubaid Javaid: selected work, Evolvo delivery gallery, writing, and contact. Next.js + GSAP with a carefully designed SVG/asset system.

## System shape

App Router portfolio with static assets under `assets/` and content under `data/` / `docs/`.

## Stack decisions

- Next.js
- React
- TypeScript
- GSAP
- Tailwind CSS
- TanStack Query

## Boundaries

- Secrets stay in environment variables / secret managers — never in git.
- Client bundles only receive public configuration (`NEXT_PUBLIC_*` / `VITE_*`).
- Tenant or role checks belong in middleware / server layers, not UI-only gates.
- Heavy or long-running work should not run inside short-lived serverless handlers unless designed for it.

## Quality bar

- Prefer typed contracts at API and domain boundaries.
- Ship a vertical slice (auth → persisted outcome) before a broad feature surface.
- Document trade-offs in PRs when changing data models or auth.

