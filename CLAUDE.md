# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal academic website for Sena Tanaka, built with [Quarto](https://quarto.org/) and hosted on GitHub Pages at `stpolisci.github.io`. It is a static HTML site rendered from `.qmd` (Quarto Markdown) source files.

## Commands

```bash
# Preview the site locally with live reload
quarto preview

# Build the site (output goes to _site/)
quarto render

# Render a single page
quarto render index.qmd
```

## Architecture

- **`_quarto.yml`** — Project configuration: site title, navbar links, HTML theme (`cosmo` + `brand`), and global CSS.
- **`_site/`** — Generated output directory (do not edit manually; regenerated on `quarto render`).
- **`.qmd` files** — Source content pages. Each has a YAML front matter block (`---`) with at minimum a `title` field.

### Pages

| File | URL path |
|------|----------|
| `index.qmd` | `/` (Home) |
| `about/about.qmd` | `/about/` |
| `cv/cv.qmd` | `/cv/` |
| `research/research.qmd` | `/research/` |
| `notes/notes.qmd` | `/notes/` |

### Styling

- `styles.css` — Custom CSS applied globally (referenced in `_quarto.yml` under `format.html.css`).
- Theme is Quarto's `cosmo` Bootstrap theme with a `brand` layer on top.

## Content Editing

All content is written in Quarto Markdown (`.qmd`), which is a superset of Pandoc Markdown. After editing `.qmd` files, run `quarto render` or use `quarto preview` for a live-reloading dev server.