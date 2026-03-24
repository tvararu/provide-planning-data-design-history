# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build and run

- `npm run build` builds the site to `_site/`
- `npm start` builds then serves with live reload
- `npm run test` runs Standard (JS code style linter)

## Adding posts

Posts live in `app/posts/` as `YYYY-MM-DD-slug.md` with YAML front matter (title, description, date, screenshots, tags). Images go in `app/images/slug/` with `01-`, `02-` prefixes.

Generate a post from a folder of images: `node scripts/generate.js slug`

## Forking / changing GitHub org

This repo was forked from [x-govuk/govuk-design-history-template](https://github.com/x-govuk/govuk-design-history-template). If you move it to a different GitHub org or rename it, update `url` and `pathPrefix` in `eleventy.config.js` to match the new GitHub Pages URL.

## Tech stack

- Eleventy 3 static site generator with Nunjucks templates
- `@x-govuk/govuk-eleventy-plugin` provides GOV.UK Design System styling
- Site config in `eleventy.config.js`, templates in `app/_layouts/`, components in `app/_components/`
- Images are passthrough-copied from `app/images/` to the site root
