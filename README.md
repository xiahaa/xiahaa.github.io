# Xiao Hu — Academic Homepage

Personal academic homepage of Dr. Xiao Hu (胡骁), deployed at
**<https://xiahaa.github.io>**.

This is a **pure static site** (plain HTML + CSS, no build step). GitHub Pages
deploys it automatically via GitHub Actions whenever you push to `main`.

## Repository layout

```
index.html                     # the entire homepage (single page)
css/style.css                  # all styling (classic academic theme, dark mode, print)
images/avatar.jpg              # portrait shown in the header
files/cv.pdf                   # downloadable CV
404.html                       # not-found page
.github/workflows/publish.yaml # static deploy workflow for GitHub Pages
```

## How to update the site

Everything you normally need to change lives in `index.html`:

| To update…        | Do this                                                            |
| ----------------- | ------------------------------------------------------------------ |
| Bio / news        | edit the `<header id="bio">` and `<section id="news">` blocks      |
| Publications      | add a `<li>` under the right `<h3 class="pub-group">` group         |
| Patents           | add a `<li>` inside one of the `<details class="patent-group">`     |
| Experience / etc. | edit the matching `<section>` (`#experience`, `#education`, …)      |
| Photo             | replace `images/avatar.jpg`                                         |
| CV PDF            | replace `files/cv.pdf`                                              |

Then commit and push:

```bash
git add -A
git commit -m "Update publications"
git push
```

The site goes live within ~1 minute (check the **Actions** tab if it doesn't).

## Formatting conventions used in `index.html`

- Your own name in author lists is wrapped in `<strong>…</strong>`.
- Publication entries are `<li>` blocks made of three `<div>`s:
  `.pub-title` / `.pub-authors` / `.pub-venue` (links go inside the venue line).
- "Under review" papers live in the *Preprints & Manuscripts Under Review* group.

## GitHub Pages settings

Repo → **Settings → Pages → Build and deployment → Source: GitHub Actions**
(this is already configured; no change needed).
