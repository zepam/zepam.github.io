## Quick start — preview locally

1. Open a terminal and change into the repo:

  `cd YOUR-GITHUB-USERNAME.github.io`

2. Start the local Jekyll server with live reload:

  `bundle exec jekyll serve --livereload`

3. Open the site in your browser:

  http://127.0.0.1:4000

## What is this site?

This repository is a Jekyll-powered GitHub Pages site. Content is written in Markdown and rendered by Jekyll using Liquid templates. Styles are authored in `assets/css/style.scss` and compiled into the final site.

Key points:

- Templates live in `_layouts/` (shared layout: `_layouts/default.html`).
- Shared header/footer in `_includes/header.html` and `_includes/footer.html`.
- Collections are stored in folders like `_projects/`, `_talks/`, `_papers/`, `_posters/`, and `_fun/`.
- Per-page metadata (title, date, thumbnail, links, etc.) is set in each item's front matter.
  - What is front matter? Any file that contains a YAML front matter block will be processed by Jekyll as a special file. The front matter must be the first thing in the file and must take the form of valid YAML set between triple-dashed lines. [source](https://jekyllrb.com/docs/front-matter/)

## Site structure (short)

- Homepage: `index.markdown` — loops over collections and renders Education, Current Projects, Talks, Papers, Posters, Fun, and Past Projects.
- Project pages: generated from files in `_projects/`.
- Papers, talks, posters, fun: each collection builds its own pages according to `_config.yml` permalink rules.

## How to add content

- Create a new markdown file in the appropriate collection folder (for example `_projects/` or `_talks/`).
- Add YAML front matter at the top, e.g.:

```yaml
---
title: "My Project"
date: 2025-06-01
thumbnail: /assets/img/my-project-thumb.png
description: "Short one-line description."
---
```

The homepage reads these fields and shows items automatically.

## Styling and assets

- Main CSS: `assets/css/style.scss`.
- Fonts, images, and JS are under `assets/` and `_site/assets/` after building.

## Deployment

This site is hosted with [GitHub Pages](https://docs.github.com/en/pages). The simplest deployment is automatic: push your changes to the publishing branch (usually `main`) and GitHub Pages will build the Jekyll site.

[GitHub Pages for Beginners](https://github.blog/developer-skills/github/github-for-beginners-getting-started-with-github-pages/)

[Getting Started with GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

🧪 [Jekyll](https://jekyllrb.com/)
