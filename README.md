[![Releases](https://img.shields.io/badge/Releases-v1.0.0-blue?logo=github)](https://github.com/Amr-MMoussa/Next-js-Boilerplate-main/releases)

# Next.js 15 Boilerplate: App/Page Router, Tailwind, TypeScript

[![Next.js](https://img.shields.io/badge/Next.js-15-black?logo=next.js&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.5-blue?logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-4.0-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Drizzle ORM](https://img.shields.io/badge/Drizzle-ORM-9cf)](https://orm.drizzle.team/)
[![Playwright](https://img.shields.io/badge/Playwright-Test-ff0080?logo=playwright)](https://playwright.dev/)
[![Storybook](https://img.shields.io/badge/Storybook-UI-ff4785?logo=storybook)](https://storybook.js.org/)
[![Vitest](https://img.shields.io/badge/Vitest-Testing-6e4cff)](https://vitest.dev/)

A full-featured starter for Next.js 15. It supports both App Router and Page Router patterns, Tailwind CSS 4, TypeScript, and a strong developer toolchain. Use this repo to bootstrap new projects or to learn modern Next.js patterns.

Demo and downloads:
- Download the latest release package and run the included installer from: https://github.com/Amr-MMoussa/Next-js-Boilerplate-main/releases
  - On the releases page, pick the asset named like nextjs-boilerplate-vX.Y.Z.tar.gz or setup.zip and run the included setup script (for example ./install.sh).

Features 🚀
- Next.js 15 support with App Router and Page Router.
- Tailwind CSS 4 + PostCSS.
- TypeScript template and strict types.
- ESLint + Prettier for consistent code style.
- Husky + Lint-Staged for pre-commit checks.
- Drizzle ORM for type-safe database access.
- Vitest + Testing Library for unit tests.
- Playwright for end-to-end tests.
- Storybook for UI components.
- Commitlint for commit message rules.
- VSCode settings and recommended extensions.
- Sentry integration for error tracking.
- CI-ready scripts and example workflows.

Why this boilerplate? 🎯
- It pairs Next.js best practices with tools that scale.
- It uses modern stacks used in production.
- It focuses on developer experience and maintainability.
- It offers a complete test and CI setup so you can ship with confidence.

Badges and quick links
- Releases: [![Releases](https://img.shields.io/badge/Releases-Download-blue?logo=github&style=for-the-badge)](https://github.com/Amr-MMoussa/Next-js-Boilerplate-main/releases)
- Use the Releases page to download the packaged installer or build artifacts. Pick the asset that matches your needs and run the included setup script.

Quick start (Local) ⚙️
1. Download the release asset from the Releases page:
   - Choose the asset named nextjs-boilerplate-vX.Y.Z.tar.gz or nextjs-boilerplate-vX.Y.Z.zip.
   - Extract the archive and run the installer script that ships with the release (example below).
2. Or clone the repo for development:
```bash
git clone https://github.com/Amr-MMoussa/Next-js-Boilerplate-main.git
cd Next-js-Boilerplate-main
pnpm install          # or npm install / yarn
cp .env.example .env.local
pnpm dev              # starts the dev server
```
3. If you downloaded the release package:
```bash
# example commands, adjust for the specific asset name
tar -xzf nextjs-boilerplate-vX.Y.Z.tar.gz
cd nextjs-boilerplate
chmod +x install.sh
./install.sh
```
The release asset includes an installer script. Run the script to scaffold local config and install dependencies.

Environment variables
- Copy the example env file to create your local config:
```bash
cp .env.example .env.local
```
- Edit .env.local with your values:
  - DATABASE_URL - connection string for your DB.
  - NEXT_PUBLIC_SENTRY_DSN - Sentry DSN for client reports.
  - SENTRY_AUTH_TOKEN - server-side Sentry token.

Project layout
- /app — App Router routes and layouts.
- /pages — Page Router routes.
- /components — UI components and primitives.
- /ui — shared design system and Storybook stories.
- /db — Drizzle ORM schema and migration files.
- /tests — unit and integration tests.
- /.github — CI workflows and issue templates.
- /scripts — utility scripts (migrations, seed, deploy).
- /storybook — Storybook config and stories.
- /playwright — Playwright tests and config.

Scripts (package.json)
- dev — start Next.js in dev mode.
- build — production build.
- start — start server from production build.
- lint — run ESLint.
- format — run Prettier.
- test — run tests with Vitest.
- test:coverage — run tests and produce coverage.
- e2e — run Playwright tests.
- storybook — start Storybook.
- build-storybook — build Storybook static site.
- migrate — run Drizzle migrations.
- seed — seed the dev database.

Testing and quality
- Unit tests: Vitest + Testing Library.
- E2E: Playwright with example tests.
- Storybook: component catalog with knobs and examples.
- Linting: ESLint configured for Next + TypeScript.
- Formatting: Prettier with shared rules.
- Pre-commit: Husky runs Lint-Staged to check files.

Database and Drizzle ORM
- Use Drizzle for typed queries and migrations.
- Migrations live in /db/migrations.
- Run migrations:
```bash
pnpm migrate
```
- Seed the database:
```bash
pnpm seed
```
- The example uses SQLite for local dev by default. Update DATABASE_URL for Postgres or MySQL.

CI and Git hooks
- CI workflows in .github/workflows include:
  - lint
  - test
  - e2e
  - storybook build
- Husky hooks run on commit and push for lint and test checks.
- Commitlint enforces conventional commits.

Storybook and UI dev
- Start Storybook:
```bash
pnpm storybook
```
- Build Storybook for a static site:
```bash
pnpm build-storybook
```
- Use stories for design reviews and component QA.

Playwright
- Playwright lives in /playwright with sample tests.
- Run Playwright:
```bash
pnpm e2e
```
- CI uses Playwright to run tests against a headless browser.

Sentry integration
- Client and server integrate with Sentry when DSN is provided.
- Add NEXT_PUBLIC_SENTRY_DSN to .env.local for frontend traces.
- Add SENTRY_AUTH_TOKEN and other server vars for server-side uploads.

VSCode and developer setup
- .vscode recommends extensions for ESLint, Prettier, Tailwind CSS, and TypeScript.
- Workspace settings lock editor.formatOnSave and formatter settings.
- Use the included devcontainer for consistent local dev in Docker.

Customization checklist
- Replace placeholder names and metadata in package.json.
- Update scripts to fit your deploy model.
- Pick your database and update DATABASE_URL.
- Adjust Tailwind config for your design tokens.
- Add Sentry DSN and other secrets via your CI secret store.

Contributing 🛠️
- Follow the commit message guidelines enforced by Commitlint.
- Run tests and linters before opening a PR.
- Use the issue templates for bug reports and feature requests.
- Add small, focused changes. Write tests when you add logic.

Maintainers
- Main repo: Amr MMoussa and contributors.
- For release downloads and packaged assets, visit the Releases page:
  https://github.com/Amr-MMoussa/Next-js-Boilerplate-main/releases
  - On that page pick the asset named like nextjs-boilerplate-vX.Y.Z.* and run the included installer (for example ./install.sh).

Changelog and releases
- See the Releases page for tagged versions and packaged assets.
- Download the installer asset on a release to create a local scaffold and to run any included migrations or setup tasks.

License
- The project uses the MIT License. See LICENSE file for details.

Common commands reference
- Install deps:
```bash
pnpm install
```
- Dev server:
```bash
pnpm dev
```
- Build:
```bash
pnpm build
pnpm start
```
- Lint and format:
```bash
pnpm lint
pnpm format
```
- Tests:
```bash
pnpm test
pnpm test:coverage
```

Troubleshooting
- If you see build errors, run lint and tests to isolate issues.
- Verify .env.local values for DB and Sentry.
- Use the release installer to set up the project when you want a local scaffold without cloning the full repo.

Resources and links
- Next.js docs: https://nextjs.org/docs
- Tailwind CSS: https://tailwindcss.com/docs
- TypeScript: https://www.typescriptlang.org/docs
- Drizzle ORM: https://orm.drizzle.team/
- Playwright: https://playwright.dev/
- Storybook: https://storybook.js.org/
- Vitest: https://vitest.dev/

Contact and support
- Open issues or pull requests on GitHub.
- For release downloads and packaged installers see:
  https://github.com/Amr-MMoussa/Next-js-Boilerplate-main/releases

<!--[end of README] -->