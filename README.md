# Zhoucheng’s blog

A lightweight GitHub Pages blog using Jekyll. Articles are Markdown files; no JavaScript framework or database is required.

## Publish

1. Create a public GitHub repository named `lizhoucheng.github.io`. If it already exists, inspect and preserve its current content before adding this blog.
2. Upload the **contents** of this folder to the repository root, including `_layouts`, `assets`, `_drafts`, and `_config.yml`. Commit to `main`.
3. Set `url` in `_config.yml` to `https://lizhoucheng.github.io`. Leave `baseurl` empty for this repository name.
4. In repository **Settings → Pages**, choose **Deploy from a branch**, branch **main**, folder **/(root)**, and Save.
5. Check the Pages build under **Actions**, then visit `https://lizhoucheng.github.io` once it finishes. Initial publication may take several minutes.

## Add a post

Copy `_drafts/your-first-post.md` into `_posts/` and name it `YYYY-MM-DD-your-post-title.md`. Use today’s date or an earlier date. Edit the title, description, category, and article body, then commit. The homepage updates automatically. Future-dated articles and files in `_drafts` stay unpublished by default.

Example front matter:

```yaml
---
layout: post
title: "What I learned building an agent"
description: "A short description of the article."
categories: [AI, Agents]
---
```

## Customize

- Introduction: `index.html`
- About page: `about.md`
- Title and site description: `_config.yml`
- Colors and typography: `assets/style.css`
- Shared navigation and footer: `_layouts/default.html`

## Optional local preview

With Ruby and Bundler installed, run `bundle install`, then `bundle exec jekyll serve`. Open the local address printed in the terminal.

Setup reference: https://docs.github.com/en/pages/quickstart
