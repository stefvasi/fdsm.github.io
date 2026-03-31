# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal website for Stefanos Skialivas (www.stefanosskialivas.com). Static site built with Jekyll from scratch — no theme gem. Dark, minimal design using DM Mono. Hosted on GitHub Pages.

## Build & Development Commands

```bash
bundle install            # Install dependencies
bundle exec jekyll serve  # Local dev server at http://localhost:4000 (auto-regenerates)
bundle exec jekyll build  # Build static site to _site/
```

## Architecture

This site was built from scratch replacing an earlier Millennial-theme-based site (`fdsm.github.io`).

- **No theme gem** — all layouts, includes, and styles are custom
- **Layouts**: `_layouts/` — `default.html` (base), `home.html` (grid of post cards), `post.html`, `page.html`, `category.html`
- **Includes**: `_includes/` — `head.html`, `header.html`, `footer.html`
- **Styles**: Single SCSS file at `assets/css/main.scss` — no partials, everything in one file
- **Content**:
  - `_posts/` — posts (format: `YYYY-MM-DD-title.md`), categorized as `performances`, `research`, `music`, or `mixtapes`
  - `pages/` — static pages (about, contact, music, research, live-performances, mixtapes, optical-scores, publications)
  - `index.html` — home page with paginated post grid
- **Configuration**:
  - `_config.yml` — site-wide build settings, default og:image
  - `_data/settings.yml` — menu items, social links
- **Plugins**: jekyll-paginate, jekyll-sitemap, jekyll-feed, jekyll-seo-tag
- **Dependencies**: sass-embedded pinned to ~> 1.80.0 (macOS 13 compatibility)
- **Custom domain**: `CNAME` points to `www.stefanosskialivas.com`

## Design

- Dark background (#0a0a0a), light text (#c8c8c8)
- DM Mono font throughout (Google Fonts)
- Uppercase site title, nav links, and post meta
- Blinking cursor after site name
- Post grid with image tiles on home/category pages
- GLightbox for image lightbox (loaded via CDN)
- MathJax loaded conditionally (only when `mathjax: true` in front matter)
- Mobile nav toggle using `///` button
- No Font Awesome — social links are plain text

## Content Conventions

- Posts use YAML front matter: `layout`, `title`, `author`, `categories`, `tags`, `image`
- Images go in `assets/img/` (subdirectories for multi-image posts, e.g. `Octopus_main_post/`)
- Menu pages defined in `_data/settings.yml` under `menu:`
- Dates displayed as `YYYY.MM.DD`
- Publications page exists but is hidden from menu
