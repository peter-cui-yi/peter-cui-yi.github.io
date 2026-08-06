# Yi Cui — Academic Website (Academic Pages)

Built with the [Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll
template and pre-filled with my CV data (publications, projects, teaching, CV). Deploys free on
GitHub Pages.

---

## 1. Identity — already filled in ✓

`_config.yml` is set to GitHub user **peter-cui-yi** (site URL, repository, GitHub link) and your
Google Scholar profile. Your site will live at **https://peter-cui-yi.github.io**.

## 2. Deploy to GitHub Pages

1. Create a **public** repo named exactly **`peter-cui-yi.github.io`**.
2. Push this folder to it:
   ```bash
   git init
   git add .
   git commit -m "Academic homepage"
   git branch -M main
   git remote add origin https://github.com/peter-cui-yi/peter-cui-yi.github.io.git
   git push -u origin main
   ```
3. Repo **Settings → Pages → Build and deployment → Source: GitHub Actions**.
   The included workflow (`.github/workflows/pages.yml`) builds and deploys automatically; the
   first run takes a few minutes. Your site is then live at **https://peter-cui-yi.github.io**.

   *Fallback:* if you prefer, pick **Source: Deploy from a branch → main / root** instead — the
   `github-pages` gem in the `Gemfile` lets GitHub build it the classic way.

## 3. Optional TODOs (search the repo for `TODO`)

| File | What to add |
|---|---|
| `_config.yml` → `googlescholar` | your Google Scholar profile URL (adds the Scholar icon) |
| `_config.yml` → `orcid`, `linkedin` | ORCID / LinkedIn if you have them |
| `_publications/*.md` → `paperurl` | uncomment and add real paper/arXiv PDF links |
| `images/profile.png` | swap the generated "YC" monogram for a real photo (keep the name) |

---

## Where the content lives

| Path | Content |
|---|---|
| `_pages/about.md` | homepage (bio, research, news) |
| `_publications/` | one Markdown file per paper |
| `_portfolio/` | projects (Construction-Site VLM, RedDust) |
| `_teaching/` | teaching assistant roles |
| `_pages/cv.md` | CV page (auto-pulls publications + teaching; links the PDF) |
| `files/` | `Yi_Cui_CV.pdf`, `Yi_Cui_CV_CN.pdf` |
| `_data/navigation.yml` | top menu |

Site-wide identity (name, sidebar bio, links, theme) is in `_config.yml`. To change the look, set
`site_theme` to one of: `default`, `air`, `sunrise`, `mint`, `dirt`, `contrast`.

## Editing without git

You can edit any `.md`/`.yml` file directly on github.com (pencil icon). Each commit re-triggers
the Pages build.

## Local preview (optional)

Requires Ruby 3.x:
```bash
bundle install
bundle exec jekyll serve -l -H localhost   # → http://localhost:4000
```
