# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is Arthur Chan's AI advisory website built with MkDocs and hosted on GitHub Pages. The site showcases Arthur's AI expertise, consulting services, publications, and resources related to speech recognition, language models, and NLP.

## Build and Deployment Commands

### Build the site
```bash
mkdocs build --clean
```

### Update and deploy to GitHub Pages
```bash
mkdocs build --clean
cp -r site/* .
git add .
git commit -m "Update"
git push origin main
```

### Development server
```bash
mkdocs serve
```

## Architecture

The site uses a dual-structure approach:
- **Source files**: Markdown content in `docs/` directory, configured via `mkdocs.yml`  
- **Generated site**: Built HTML in `site/` directory, then copied to root for GitHub Pages hosting

### Key directories:
- `docs/`: Source markdown files for all pages
- `site/`: Generated HTML output from MkDocs build
- `images/`: Static assets including logo and images
- Root HTML files: Deployed versions copied from `site/`

### Content structure:
- Homepage (`docs/index.md`): AI advisory services and expertise
- About sections: Personal bio and detailed background
- Portfolio (`docs/ai_portfolio.md`): AI projects and experience
- Resources: Learning materials and book recommendations
- Publications: Academic and professional publications

## Configuration

The site uses Material theme for MkDocs with:
- Blue color scheme with dark/light mode toggle
- Inter font for text, Fira Code for code blocks  
- Navigation tabs and integrated table of contents
- Search highlighting and markdown extensions

## Workflow

1. Edit markdown files in `docs/` directory
2. Run `mkdocs build --clean` to generate site
3. Copy contents of `site/` to root directory with `cp -r site/* .`
4. Commit and push changes to deploy via GitHub Pages

The site is configured to serve from the repository root, which is why generated files are copied there after building.