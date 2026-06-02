# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Arthur Chan's AI advisory website built with MkDocs (Material theme) and hosted on GitHub Pages. Content covers speech recognition consulting, LLMs, NLP publications, and resources.

## Commands

```bash
# Local preview
mkdocs serve

# Build
mkdocs build --clean

# Build and deploy
mkdocs build --clean && cp -r site/* . && git add . && git commit -m "Update" && git push origin main
```

## Architecture

**Dual-structure**: source markdown lives in `docs/`, built HTML goes to `site/`, then copied to the repo root for GitHub Pages serving.

- Edit only files under `docs/` — root HTML files are generated artifacts
- `mkdocs.yml` controls navigation order, theme, and extensions
- `images/` holds static assets (logo, photos); reference them in markdown as `../images/filename`

### Nav structure (from `mkdocs.yml`)

```
Home → docs/index.md
About → docs/about.md
Full bio → docs/fullbio.md
Publications → docs/publications.md
AI Portfolio → docs/ai_portfolio.md
Resources → docs/resources.md, docs/learning-dl-top5.md, docs/book-recommendations.md
```

### Known quirks

- `mkdocs.yml` has `site_url: https://arthurchan.github.io/my-blog` — this appears incorrect; the real URL is `https://arthchan2003.github.io/`.
- `extra_css: [assets/custom.css]` is declared in `mkdocs.yml` but `docs/assets/custom.css` does not exist — create it if custom styles are needed.
- Root directories `mlportfoilio/` and `contactme/` are stale artifacts from earlier deploys; they have no corresponding source in `docs/`.

### Available markdown extensions

`toc` (with permalink), `footnotes`, `attr_list`, `admonition`, `pymdownx.superfences`, `pymdownx.details`
