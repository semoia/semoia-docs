# Repository Guidelines

## Project Structure & Module Organization
- `docs.json` is the Mintlify config and navigation source of truth.
- Top-level MDX pages live in the repo root (for example `index.mdx`, `quickstart.mdx`, `support.mdx`).
- Sectioned content is grouped in folders: `features/`, `mcp/`, `snippets/`, and `user-manual/`.
- Static assets are in `images/`, `logo/`, and `favicon.svg`.

## Build, Test, and Development Commands
- `npm i -g mint`: Install the Mintlify CLI (required for local preview).
- `mint dev`: Run the docs locally at `http://localhost:3000`.
- `mint dev --port 3333`: Run the local server on a custom port.
- `mint broken-links`: Scan for broken internal/external links.
- `npm mint update`: Update the Mintlify CLI if preview and prod drift.

## Coding Style & Naming Conventions
- Content is MDX. Match existing formatting and component usage in nearby pages.
- Use kebab-case for new file names (for example `features/new-capability.mdx`).
- Prefer short, task-focused frontmatter titles and descriptions.
- Use an MDX-aware formatter (Prettier + MDX extension) when editing.

## Testing Guidelines
- There is no automated test suite. Use `mint dev` for manual review and `mint broken-links` before submitting changes.

## Commit & Pull Request Guidelines
- Commit messages follow Conventional Commit prefixes seen in history: `docs:`, `fix:`, `feat:`, `refactor:`.
- PRs should include a short summary, link any related issues, and note doc navigation changes if `docs.json` was updated.
- Include screenshots for visual changes (for example hero images or embedded UI).

## Configuration & Deployment Notes
- Navigation, tabs, and branding live in `docs.json`; keep it in sync with new/renamed pages.
- Production deploys are triggered by pushes to the default branch via the Mintlify GitHub app.
