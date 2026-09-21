# maurice1979.github.io

Jordi Vidal de Llobatera's personal site — https://maurice1979.github.io/

Built with [Quarto](https://quarto.org). Consolidates what used to be two separate,
mostly-unfinished sites (this repo's old Jekyll "Agency" theme, and the `fastblog`
repo's fastpages blog) into one: Home, About, Projects, Blog.

## Structure

- `index.qmd` — home page
- `about.qmd` — about / bio
- `projects.qmd` — project showcase
- `blog.qmd` + `posts/` — blog listing and posts

## Writing a post

Create a new folder under `posts/`, e.g. `posts/my-new-post/index.qmd`, with front matter like:

```yaml
---
title: "My New Post"
description: "One-line summary."
date: "2026-09-21"
categories: [data-engineering]
---
```

Draft posts (hidden from the listing until ready) can be marked with `draft: true`.

## Preview locally

Install [Quarto](https://quarto.org/docs/get-started/), then from the repo root:

```bash
quarto preview
```

## Publishing

Pushing to `master` triggers `.github/workflows/publish.yml`, which renders the
site and deploys it via GitHub Pages' native Actions deployment.

**One-time setup:** in this repo's **Settings → Pages**, set "Build and deployment
→ Source" to **GitHub Actions** (not "Deploy from a branch"). After that, every
push to `master` deploys automatically.
