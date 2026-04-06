# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Artifacts

### Arab Atelier — Luxury Menswear (`artifacts/arab-atelier`)
- React + Vite frontend-only app at `/` (previewPath: `/`)
- Full luxury menswear landing page for Arab Atelier brand
- Sections: Loader, Nav, Hero, Ticker, Editorial Intro, Philosophy (3D sphere), Collection Grid (tilt cards), Runway Strip, Bespoke (3D cube), Stats, Editorial Quote, Newsletter, Footer
- Fonts: Cormorant Garamond, Montserrat, Cinzel (Google Fonts)
- Animations: Framer Motion throughout, CSS 3D transforms
- Color palette: deep indigo/violet bg, ivory text, gold + crimson accents

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
