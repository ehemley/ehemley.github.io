# Emerson Hemley's academic website

Personal site for a math PhD student at Penn, live at https://ehemley.github.io.
Built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme.

## How it publishes

- Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site
  and publishes it to the `gh-pages` branch. The live site updates a few minutes later.
- Never edit the `gh-pages` branch directly.
- Check a deploy with `gh run list --workflow=deploy.yml --limit 3`.
- The theme's Prettier and `broken-links.yml` workflows were removed at the owner's
  request (they failed on every push). Live-site link checking still runs via
  `broken-links-site.yml`.

## Workflow the owner wants

1. Make the requested edit.
2. Preview it locally (the `site` server in `.claude/launch.json`, http://localhost:4000)
   and show the affected page before committing.
3. Commit with a short, plain message (e.g. "add Hodge atoms talk to notes").
4. **Ask before pushing.** Pushing publishes to the public site.
5. After pushing, confirm the deploy workflow succeeded.

Keep edits small and in the existing style. Don't touch theme internals (`_layouts`,
`_includes`, `_sass`, `_plugins`, workflows) unless asked.

## Where content lives

| What | File | Notes |
|---|---|---|
| Homepage / bio | `_pages/about.md` | Body text below the front matter. Email written as `ehemley[at]sas.upenn.edu`. |
| Publications & notes ("writing") | `_pages/publications.md` | **Hand-written Markdown lists**, not generated from BibTeX. Two sections: `## publications` and `## notes`. Some notes are commented out with `<!-- -->` (hidden drafts). |
| PDFs of notes | `assets/pdf/` | Link from pages as `../assets/pdf/NAME.pdf`. |
| Teaching | `_pages/teaching.md` | Bulleted list, newest first. |
| Seminar page | `seminar.md` (repo root) | `/seminar/`, not in the navbar (`nav: false`). Linked from about page. Has a schedule table. |
| Blog posts | `_posts/YYYY-MM-DD-slug.md` | Use LaTeX with `$$...$$` (kramdown/MathJax), for both inline and display math. |
| News items | `_news/` | Currently unused template items; news is off on the homepage. |
| Travel | `_pages/travel.md` | In the navbar (`nav: true`). Two sections: `### upcoming` and `### past`, newest first. |
| Social links | `_data/socials.yml` | |
| Site settings, name | `_config.yml` | |
| Images | `assets/img/` | `prof_pic.jpg` is the profile photo slot (currently disabled in about.md). |

Navbar: pages with `nav: true` appear, ordered by `nav_order`
(writing = 2, teaching = 4, travel = 5).

`_bibliography/papers.bib` still holds the template placeholder entry and is not
used by the writing page.

## Local preview

- `bundle exec jekyll serve --livereload` (or start the `site` preview server).
- A full build takes ~15 s. Sass deprecation warnings and
  "Terser Exception: source sequence is illegal/malformed utf-8" are pre-existing and harmless.
- `CLAUDE.md` is in the `exclude:` list in `_config.yml` so it isn't published; keep it there.
