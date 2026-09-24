# Portfolio Site Plan

## Goal

Create a responsive, accessible personal portfolio for GitHub Pages as a user site (`<username>.github.io`), published from the `main` branch and repository root.

## Pages and features

- Home, About, Work Experience, and Contact pages written in Markdown with YAML front matter.
- Shared Jekyll layout, navigation, footer, and SEO include.
- Semantic HTML, responsive single-column CSS, sitemap, and favicon.
- No backend, form processing, blog, trackers, framework, or unnecessary JavaScript.
- README with editing, local preview, and Lighthouse instructions.

## Technical approach

Use GitHub Pages-compatible Jekyll conventions, with `_config.yml`, `_layouts/`, `_includes/`, and `assets/` directly in the repository root. Keep content in Markdown and presentation in reusable HTML/CSS. Configure an empty `baseurl` and use Jekyll URL filters for internal links.

## Assumptions and placeholders

- Use a light-only theme and system font stack until you provide preferences.
- Mark all personal biography, employment, and project details as placeholders; invent no claims or metrics.
- Do not display an email address unless you later provide one and confirm it may be public.
- Use a clearly marked GitHub username placeholder until the real username is provided.
- The current generated pnpm/TypeScript workspace scaffold will be replaced by the static Jekyll site at the repository root.

## Verification

Check root-level file placement, build compatibility with GitHub Pages, navigation links, and layouts at 375px and 1280px. Run Lighthouse and target at least 90 in Performance, Accessibility, Best Practices, and SEO.