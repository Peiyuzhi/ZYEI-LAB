# Repository Guidelines

## Project Structure & Module Organization
- `index.html` is the primary landing page with embedded CSS and JavaScript.
- `about.html` and `team.html` are standalone pages, following the same static, inline-style pattern.
- Static assets live at the repo root (example: `Robot.mp4`).
- Deployment/SEO configuration is also in the root: `vercel.json`, `robots.txt`, `sitemap.xml`.
- `package.json` contains metadata only; there is no build pipeline.

## Build, Test, and Development Commands
- `vercel deploy` — deploys the static site to Vercel.
- Local preview: use any static server. Example:
  ```bash
  python3 -m http.server 8000
  ```
  then open `http://localhost:8000/index.html`.

## Coding Style & Naming Conventions
- Keep HTML/CSS/JS inline per page unless refactoring is explicitly planned.
- Indentation is 4 spaces in HTML, CSS, and inline scripts; match existing style.
- Use and extend the CSS custom properties in `:root` for color, spacing, and theme consistency.
- Bilingual text uses `data-zh`/`data-en` or `data-*-content` attributes; update both translations together.
- Prefer lowercase filenames and short, descriptive names for new pages.

## Testing Guidelines
- No automated tests are configured.
- Manual checks should include: desktop/mobile layout, navigation/scroll behavior, carousel interactions, and language switching (if edited).
- Verify SEO artifacts remain accurate when adding or renaming pages (`sitemap.xml`, `robots.txt`, meta tags).

## Commit & Pull Request Guidelines
- Recent commits are short and lowercase, often with a scope prefix like `seo:` (e.g., `seo: add meta tags`). Follow this pattern.
- PRs should include a concise summary, list of modified pages (e.g., `index.html`, `about.html`), and screenshots for any visual changes.
- Call out SEO or i18n updates explicitly so reviewers know to verify metadata and translations.

## Deployment & Configuration Notes
- `vercel.json` serves files directly from the repository root with no build step.
- Keep `robots.txt` and `sitemap.xml` aligned with any new or removed pages.
