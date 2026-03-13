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

- **Ruby**: 3.4.9+ (managed by [mise](https://mise.jdx.dev/) via `mise.toml`)
- **Jekyll**: 4.4+ (static site generator)
- **Frontend**: Bootstrap 5.3.8+ (CDN) / Google Fonts (Bebas Neue, Source Sans 3, Libre Baskerville)
- **Plugins**: jekyll-sitemap, jekyll-date-localization
- **Hosting**: [Render.com](https://render.com) (static site, build: `bundle exec jekyll build`, publish: `_site`)

## Project Structure

```
_layouts/        # Page templates (default.html, page.html)
_includes/       # Reusable fragments (bios, embeds)
_data/           # Structured content (YAML, CSV)
assets/img/      # Images (band photos, logos, SVGs)
assets/file/     # Downloads (PDFs, ZIPs)
css/styles.css   # Custom styles (design tokens, Bootstrap overrides)
```

## Critical Rules

- **ALWAYS** use `git mv` for file moves/renames
- **NEVER** use Bootstrap 4 classes (use 5.3+ only)
- **NEVER** use `.text-muted` (use `.text-body-secondary` or `.text-body-tertiary`)

## Commands

```bash
bundle exec jekyll serve   # Local dev server (http://localhost:4000)
bundle exec jekyll build   # Build static site to _site/
```

Note: `_config.yml` is NOT hot-reloaded — restart the server after editing it.

## Data Files

Content is managed via data files in `_data/`. Follow the existing formats exactly.

### Concert dates (`_data/past_liveshows.yml`, `_data/upcoming_liveshows.yml`)

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
- Fonts: Bebas Neue (display/headings), Source Sans 3 (body), Libre Baskerville (serif accents)
- Responsive images: `band.jpg` (desktop), `band-xs.jpg` (mobile ≤768px)

## Accessibility

- **Images**: `alt=""` if decorative, descriptive `alt` if meaningful
- **Icon-only links**: `aria-label` when no visible text (social media icons, etc.)
