# Development Guide

**D-BORA** — Site vitrine du groupe de rock (d-bora.fr) — GitHub: `bobmaerten/d-bora.fr`

**Core Principle:** Code should be so simple and clear that reading it feels like reading well-written documentation. Elegant. Self-explanatory.

## Project Overview

Static site for D-BORA, a rock band from Hauts-de-France. Built with Jekyll and Bootstrap 5.3. We prioritize **simplicity, clarity, and maintainability**.

### Comments

Code should speak for itself. Don't comment _what_ — comment _why_.

- **Don't** restate what the code does
- **Do** explain non-obvious _why_ — workarounds, surprising constraints
- **Don't** leave commented-out code — delete it, git has the history
- **Do** update or remove comments that no longer match the code's behavior

**Boy scout rule:** When modifying code, take the opportunity to simplify nearby legacy — remove dead code, flatten unnecessary abstractions. Don't be afraid to delete what's no longer needed.

## Communication Standards

- Expert French dev team (20+ years IT, bilingual FR/EN)
- Direct and concise — no verbose explanations
- French with embedded English tech terms in GitHub/Claude Code responses
- English for code, comments, documentation

## Tech Stack

- **Ruby**: 3.4.12+ (managed by [mise](https://mise.jdx.dev/) via `mise.toml`)
- **Jekyll**: 4.4+ (static site generator)
- **Frontend**: Bootstrap 5.3.8 and fonts (Bebas Neue, Source Sans 3), all self-hosted: no third-party request before first paint, no visitor IP sent to Google
  - Bootstrap: `assets/bootstrap/bootstrap.min.{css,js}` — to upgrade, replace both files from `https://cdn.jsdelivr.net/npm/bootstrap@<version>/dist/` and check their SRI hashes against getbootstrap.com
  - Fonts: latin subsets in `assets/fonts/` (woff2, Source Sans 3 is variable), declared with `@font-face` at the top of `css/styles.css`
- **Plugins**: jekyll-sitemap, jekyll-date-localization
- **Hosting**: [Render.com](https://render.com) (static site, build: `bundle exec jekyll build`, publish: `_site`)

## Project Structure

```
_layouts/        # Page templates (default.html, page.html)
_includes/       # Reusable fragments (bios, embeds)
_data/           # Structured content (YAML, CSV)
assets/img/      # Images (band photos, logos, SVGs)
assets/file/     # Downloads (PDFs, ZIPs)
assets/fonts/    # Self-hosted woff2 fonts
assets/bootstrap/ # Self-hosted Bootstrap
css/styles.css   # Custom styles (design tokens, Bootstrap overrides)
```

## Critical Rules

- **ALWAYS** use `git mv` for file moves/renames
- **NEVER** use Bootstrap 4 classes (use 5.3+ only)
- **NEVER** use `.text-muted` (use `.text-body-secondary` or `.text-body-tertiary`)
- **Commits:** AI help goes in an `Assisted-by: <model> [<tool>]` trailer, never `Co-Authored-By`

## Commands

```bash
bundle exec jekyll serve   # Local dev server (http://localhost:4000)
bundle exec jekyll build   # Build static site to _site/
```

Note: `_config.yml` is NOT hot-reloaded — restart the server after editing it.

## Data Files

Content is managed via data files in `_data/`. Follow the existing formats exactly.

### Concert dates (`_data/past_liveshows.yml`, `_data/upcoming_liveshows.yml`)

`when` is the local (Paris) hour followed by `Z`: it is rendered as typed (`timezone: Etc/UTC` in `_config.yml`).

```yaml
- when: 2025-11-14T19:00:00Z
  title: Live au V&B
  address: V&B Aulnoy-les-Valenciennes
```

### SoundCloud tracks (`_data/soundclouds.csv`)

```csv
title,id
Rebelle,1942665195
```

### YouTube videos (`_data/videos.csv`)

```csv
title,id
Et si Dieu... (oct.24),JJ6Oa-SmPWs
```

## CSS & Styling

- **Bootstrap utilities in HTML first** — only write custom CSS when utilities cannot achieve the design
- **Flat selectors** — avoid deep nesting
- **Semantic naming** — `.btn-xl` not `.big-orange-button`
- Design tokens in `:root` — use `var(--color-accent)`, `var(--color-gold)`, `var(--color-text)`, etc.
- Fonts: Bebas Neue (display: headings, nav, buttons, dates), Source Sans 3 (all running text) — two families, no third
- Hero photo: `band.jpg` (3:2, 2000px, faces in the top quarter) and `band-xs.jpg` (same photo, 1000px) for mobile, shown whole above the text, not cropped
- Photos: two sizes per photo, `name.jpg` and `name-sm.jpg` (half width), served with `srcset`/`sizes`. Export with `magick in.jpg -auto-orient -resize 1600x1600\> -strip -interlace Plane -sampling-factor 4:2:0 -quality 78 out.jpg` (macOS `sips` ignores the quality setting)

## Accessibility

- **Images**: `alt=""` if decorative, descriptive `alt` if meaningful
- **Icon-only links**: `aria-label` when no visible text (social media icons, etc.)
