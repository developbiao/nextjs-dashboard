# Repository Guidelines

## Project Structure & Module Organization
This repository is a Next.js App Router project. Application entry points live in `app/page.tsx` and `app/layout.tsx`. UI components and styles are organized under `app/ui/` (including CSS modules like `*.module.css` and shared styles in `app/ui/global.css`). Data helpers and types live in `app/lib/`, while API-style routes are defined in `app/query/route.ts` and `app/seed/route.ts`. Static assets belong in `public/`. Project-wide configuration is in `next.config.ts`, `tailwind.config.ts`, and `postcss.config.js`.

## Build, Test, and Development Commands
Use `pnpm` (see `pnpm-lock.yaml`). Key scripts:
- `pnpm dev`: run the local development server (turbopack enabled).
- `pnpm build`: create a production build.
- `pnpm start`: run the production server after a build.

## Coding Style & Naming Conventions
The codebase is TypeScript + React. Follow the existing two-space indentation and keep React components in PascalCase. Filenames in `app/ui/` use kebab-case (for example, `acme-logo.tsx`), while route files follow Next.js conventions (`page.tsx`, `layout.tsx`, `route.ts`). Styling is primarily Tailwind CSS; keep utility class ordering readable and place reusable styles in `app/ui/global.css` or CSS modules when appropriate.

## Testing Guidelines
No test framework is configured yet. If you add tests, keep them close to the feature (for example, `app/ui/__tests__/button.test.tsx`) and add a `pnpm test` script with clear instructions in the README or this file.

## Commit & Pull Request Guidelines
Current history shows short, descriptive commit messages. Keep messages concise and in plain language (for example, "css styling"). For PRs, include a brief summary, note how you verified changes, attach screenshots for UI updates, and link relevant issues if applicable.

## Configuration & Secrets
Copy `.env.example` to `.env.local` and fill in local values (database URLs and auth secrets). Do not commit `.env.local`. For local auth, `AUTH_URL` defaults to `http://localhost:3000/api/auth`.
