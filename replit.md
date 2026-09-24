# Personal Portfolio

A static Jekyll portfolio for GitHub Pages, with Markdown page content and shared HTML layouts/includes.

## Run & Operate

- Install Ruby and Bundler, then run `bundle install`.
- Preview locally with `bundle exec jekyll serve`.
- Build the site with `bundle exec jekyll build`.
- GitHub Pages should publish the `main` branch from `/(root)`.

## Structure

- `index.md`, `about.md`, `work-experience.md`, `contact.md` — page content and YAML front matter.
- `_config.yml` — site metadata, plugin configuration, and navigation.
- `_layouts/` and `_includes/` — shared semantic page structure, navigation, footer, and SEO tags.
- `assets/css/main.css` and `assets/favicon.svg` — responsive styling and favicon.
- `README.md` — editing, preview, Lighthouse, and publishing instructions.
- `PLAN.md` — the approved implementation plan; excluded from the generated site.

## Architecture decisions

- Keep the site at the repository root for GitHub Pages branch publishing.
- Use the `github-pages` gem and its supported `jekyll-seo-tag` and `jekyll-sitemap` plugins.
- Use Markdown for content and CSS for presentation; no application server or client-side framework.
- Keep personal details as explicit placeholders until the owner supplies them.

## User preferences

- Light theme and system font stack are temporary defaults because no visual preferences or biography were provided.
- Do not expose an email address unless the owner later provides one and confirms it may be public.
