# Repository Guidelines

## Project Structure & Module Organization
- `Astro_Plain/`: Astro site. Code in `src/` (`pages/`, `components/`, `layouts/`, `styles/`); content in `src/content/blog/`.
- `Astro_design_Grilled squid slices/`: Astro site (path has spaces; quote it). Mirrors `Astro_Plain/` structure.
- `Jekyll_design_Zen/`: Jekyll site. Posts in `_posts/`, pages in `pages/`, layouts in `_layouts/`, includes in `_includes/`, assets in `css/` and `launcher/`.
- `Hexo_design_CHaN/`: Hexo site. Site config `_config.yml`; theme/layouts under `CHaN/layout/`; assets in `CHaN/source/`.

## Build, Test, and Development Commands
- Astro (per subfolder): `npm ci && npm run dev` (serve), `npm run build` (static build), `npm run preview` (serve build). Example: `cd 'Astro_design_Grilled squid slices' && npm run dev`.
- Jekyll: `bundle install`; `bundle exec jekyll serve` (dev); `bundle exec jekyll build` (site). Requires Ruby + Bundler.
- Hexo: `npm i`; `npx hexo s` (serve); `npx hexo g` (generate); optional `npx hexo clean`.
- Quick checks: Astro `npm run astro -- check`; Jekyll `bundle exec jekyll doctor`; Hexo `npx hexo doctor`.

## Coding Style & Naming Conventions
- Indentation: 2 spaces; UTF-8 encoding.
- Astro/TS: camelCase variables, PascalCase components (e.g., `BaseHead.astro`), kebab-case routes (e.g., `src/pages/blog/[...slug].astro`).
- Content files: `YYYY-M-D-title.md`. Keep frontmatter per `src/content/config.ts`:
  ```yaml
  ---
  title: My Post
  description: Short summary
  pubDate: 2025-01-01
  tags: [tag1, tag2]
  ---
  ```
- HTML/CSS: semantic HTML; minimize inline styles; prefer `global.css` or scoped styles.

## Testing Guidelines
- No unit tests maintained. Acceptance = successful build + local smoke test.
- Verify changed site routes: home, post page, tags, 404, RSS.

## Commit & Pull Request Guidelines
- Commits: prefer Conventional Commits (e.g., `feat(astro-plain): add tag page`).
- PR description: affected subprojects, summary, steps to verify; link issues. Include before/after screenshots for visual changes.
- Keep diffs focused; avoid unrelated reformatting.

## Security & Configuration Tips
- Never commit secrets. Review deploy/base URLs in `astro.config.mjs`, `src/consts.ts`, and `_config.yml` before publishing.
- Large binaries: avoid; prefer external hosting. Place images in each project’s asset dirs.
