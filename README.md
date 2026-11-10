# MultiValue Modernization blog

A [Jekyll](https://jekyllrb.com) site using the [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) theme, published with GitHub Pages.

## Layout

| Path | What it is |
|---|---|
| `_config.yml` | Site title, URL, GitHub user name, theme settings |
| `_posts/` | Blog posts, named `YYYY-MM-DD-title.md` |
| `_tabs/` | Sidebar pages: Modernization, Categories, Tags, Archives, About |
| `mv-modernization/technical/` | Stand-alone page: technical edition |
| `mv-modernization/learn/` | Stand-alone page: Learn MultiValue edition |
| `assets/img/` | Avatar and images |
| `.github/workflows/pages-deploy.yml` | Builds and deploys on every push to `main` |

The two pages under `mv-modernization/` have no front matter, so Jekyll copies them as they are, with their own design and without the Chirpy sidebar. The **Modernization** tab links to both.

## Publish on GitHub Pages

1. `_config.yml` is already set for the `clarityascend` account.
2. Create a repository named `clarityascend.github.io`.
3. Push this folder to its `main` branch:
   ```sh
   git init -b main
   git add .
   git commit -m "Initial Chirpy site"
   git remote add origin https://github.com/clarityascend/clarityascend.github.io.git
   git push -u origin main
   ```
4. In the repository, open **Settings › Pages** and set **Source** to **GitHub Actions**.
5. The **Build and Deploy** workflow publishes the site at `https://clarityascend.github.io`.

## Run locally

Needs Ruby 3.1 or later and Bundler.

```sh
bundle install
bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000>.

## Write a post

Create `_posts/2026-11-10-my-post.md`:

```markdown
---
title: "My post"
date: 2026-11-10 09:00:00 +0000
categories: [MultiValue]
tags: [universe]
---

Post text in Markdown.
```
