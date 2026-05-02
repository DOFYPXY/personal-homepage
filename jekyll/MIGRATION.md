# Hugo (Wowchemy) → Jekyll (al-folio) migration

This `jekyll/` folder is an al-folio site populated with content ported from the
Hugo Academic site living in the parent directory. Both trees coexist on the
`migrate-jekyll-al-folio` branch so you can preview and compare before
committing to the switch.

## What was ported

| From (Hugo)                                              | To (Jekyll)                                |
| -------------------------------------------------------- | ------------------------------------------ |
| `content/authors/admin/_index.md` (bio, affiliation)     | `_pages/about.md`                          |
| `content/authors/admin/avatar.jpg`                       | `assets/img/prof_pic.jpg`                  |
| `content/publication/{memoization,specification,transformer}` | `_bibliography/papers.bib` (3 entries) |
| `content/publication/memoization/memoization.pdf`        | `assets/pdf/memoization.pdf`               |
| `static/uploads/CV.pdf`, `static/uploads/full-CV.pdf`    | `assets/pdf/CV.pdf`, `assets/pdf/full-CV.pdf` |
| `config/_default/{config,params,menus}.yaml` (selected)  | `_config.yml`, `_data/socials.yml`         |

## What was dropped

- Wowchemy demo publication `content/publication/example/` (placeholder).
- Wowchemy demo blog post `content/post/getting-started/` (placeholder; the
  site's nav already pointed `Blog` at the external `http://dofy.top`).
- al-folio sample collections we don't use: `_books/`, `_projects/`,
  `_teachings/`, `_news/`, all sample posts under `_posts/`, and the
  corresponding `_pages/` (books, projects, teaching, news, repositories,
  profiles, dropdown, about_einstein).
- al-folio sample data files (`coauthors.yml`, `citations.yml`,
  `repositories.yml`, `venues.yml`, `cv.yml` Einstein example).

## What still needs your eyes

1. **About page** — `_pages/about.md` carries over your Hugo bio verbatim.
   Update the year/affiliation if needed.
2. **CV page** — `_pages/cv.md` shows just a title plus a PDF download button.
   If you want a structured rendered CV, fill in `_data/cv.yml` (RenderCV YAML)
   or `_data/resume.json` (JSONResume).
3. **Publication metadata** — abstracts and links carried over, but I had to
   guess the Arxiv ID for the POPL26 transformer paper (your Hugo frontmatter
   reused the LOUD arxiv link `2512.06442` for both papers; please correct).
4. **Socials** — `_data/socials.yml` only has email + GitHub. Add Google
   Scholar / LinkedIn / etc. when ready (see al-folio docs).
5. **`url` / `baseurl`** — set to `https://dofypxy.github.io` with empty
   `baseurl` for a user GitHub Pages site. Change if you deploy elsewhere.

## Building locally

al-folio needs Ruby 3.x — your system Ruby is 2.6, so the easiest path is the
official Docker image:

```bash
cd jekyll
docker compose pull
docker compose up
# site at http://localhost:8080
```

If you'd rather install Ruby 3 natively (e.g. `brew install ruby@3.3`), then:

```bash
cd jekyll
bundle install
bundle exec jekyll serve
```

## Deploying

al-folio ships a GitHub Actions workflow (`.github/workflows/deploy.yml`) that
builds and pushes to `gh-pages`. To use it:

1. Move the contents of `jekyll/` to the repo root (delete or archive Hugo
   files: `content/`, `config/`, `static/`, `themes/`, `go.mod`, `go.sum`,
   `netlify.toml`, etc.).
2. Push to `master`. The Action will build with the right Ruby version and
   publish to `gh-pages`.
3. In GitHub repo settings → Pages, set source to the `gh-pages` branch.

The current Netlify config (`netlify.toml` at repo root) is Hugo-specific and
should be removed if you switch to GitHub Pages, or replaced with a
Jekyll-aware build command if you stay on Netlify.
