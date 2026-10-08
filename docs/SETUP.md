# Setup — mubaidjavaid Portfolio

## Prerequisites

- Node.js 20.x LTS (or the version pinned by the repo)
- Package manager matching the lockfile (npm / pnpm / yarn)
- Git

## Install & run

```bash
npm install
cp .env.example .env.local
npm run dev
```

## Environment

`NEXT_PUBLIC_SITE_URL`, Resend, GA4 as needed — see `.env.example`.

Copy `.env.example` (when present) to `.env.local` / `.env`. Never commit secret files.

## Verify

1. App boots without console crashes.
2. Primary happy-path screen loads.
3. Auth / API health checks pass if present.

## Deploy notes

Prefer Vercel for Next.js frontends. Set **Root Directory** correctly for monorepos. Attach Production + Preview env vars in the host dashboard.

