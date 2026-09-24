# Personal Portfolio

A static portfolio built with Markdown, HTML, CSS, and GitHub Pages-compatible Jekyll. The pages share reusable layouts and includes; there is no application server, database, contact-form backend, or client-side framework.

## Before publishing

1. In `_config.yml`, replace `your-github-username` in `url` with your actual GitHub username. Keep `baseurl: ""` for a user site named `<username>.github.io`.
2. Replace every bracketed placeholder in the Markdown pages and configuration with details you want to share. Do not publish the placeholder work-history entry.
3. Add a public email address only if you are comfortable making it visible to everyone. A `mailto:` link requires visitors to have an email app.
4. Review all content and the site title/description before publishing.

## Edit the site

- `index.md`, `about.md`, `work-experience.md`, and `contact.md` contain page content.
- `_config.yml` contains site metadata and the navigation links.
- `_layouts/default.html` and `_includes/` contain the shared page structure.
- `assets/css/main.css` contains the responsive styles; `assets/favicon.svg` is the favicon.
- `PLAN.md` records the approved implementation plan and is excluded from the generated site.

Use Markdown for page copy. Internal page links should use Jekyll's `relative_url` filter so they work with GitHub Pages routing.

## Preview locally

Install Ruby and Bundler, then run these commands from the repository root:

```sh
bundle install
bundle exec jekyll serve
```

Open the local address printed by Jekyll. To build the static output without starting the preview server:

```sh
bundle exec jekyll build
```

The generated site is written to `_site/`, which is ignored by Git.

## Run Lighthouse

1. Open the local preview in Chrome.
2. Open Developer Tools and select **Lighthouse**.
3. Run an audit for **Mobile** and **Desktop**, with Performance, Accessibility, Best Practices, and SEO selected.
4. Review and resolve any findings, then rerun the audits.

The target is 90 or higher in all four categories on both viewport profiles. Scores depend on the final content and the browser environment.

## Publish with GitHub Pages

1. Create a public repository named `<your-github-username>.github.io`.
2. Commit this site's files directly at the repository root and push them to the `main` branch.
3. In the repository's **Settings → Pages**, choose **Deploy from a branch**, then select `main` and `/(root)`.
4. Save the setting and wait for GitHub Pages to finish its first deployment.

GitHub Pages builds this Jekyll site directly from the selected branch and root; no generated `_site/` folder or separate application is needed in the repository.