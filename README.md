# litong2358.github.io

Personal academic website for **Tong Li (Amber)**, Ph.D. student in Computer Science at Virginia Tech.

Live at <https://litong2358.github.io>

This is a **single-page** site. Built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll template (MIT), itself a fork of the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme by Michael Rose.

## Editing the site

| What you want to change | File |
| --- | --- |
| All page content (intro, research interests, news, awards) | `_pages/about.md` |
| Name, sidebar bio, location, email, social links | `_config.yml` (the `author:` block) |
| Profile photo | replace `images/profile.jpg` (square, 512x512) |
| Header nav links (currently none) | `_data/navigation.yml` |

## Adding pages back

The template's Publications / Talks / Teaching / Portfolio / CV sections were removed to keep this a single page. To bring one back:

1. Restore the collection in `_config.yml` under `collections:` and add a matching entry to `defaults:`.
2. Recreate the archive page in `_pages/` (for example `publications.html`) with a `permalink`.
3. Add the page to `main:` in `_data/navigation.yml` so it shows in the header.

Earlier versions of all of these are in git history:

```bash
git log --oneline --diff-filter=D --name-only
git show <commit>:_pages/cv.md > _pages/cv.md
```

## Local preview

Requires Docker:

```bash
docker compose up
```

Then open <http://localhost:4000>. Ctrl-C to stop.

## Deployment

Pushing to `master` triggers `.github/workflows/deploy.yml`, which builds the site and deploys it to GitHub Pages. This requires **Settings → Pages → Source = GitHub Actions** to be set once on the repository.
