
# Class Wiki (MkDocs + Material + Jupyter)

A minimal teaching scaffold where students contribute Markdown or Jupyter notebooks to a GitHub repo and see their changes reflected on a wiki-like site.

## Quick start

```bash
# 1) Clone the repo
# 2) (Optional) Create & activate a virtualenv
pip install -r requirements.txt
mkdocs serve   # http://127.0.0.1:8000
```

## Add a page
- Create a Markdown file under `docs/` (e.g., `docs/my-page.md`).
- Add it to the `nav` section of `mkdocs.yml`.

## Add a Jupyter notebook page
- Save an `.ipynb` in `docs/notebooks/` (e.g., `docs/notebooks/lesson.ipynb`).
- Add it to `nav` in `mkdocs.yml`.

### (Optional) Execute notebooks on build
In `mkdocs.yml` you can enable execution:

```yaml
plugins:
  - mkdocs-jupyter:
      execute: true
      kernel_name: python3
```

## Deploy to GitHub Pages (simplest)
From your machine:

```bash
mkdocs gh-deploy
```

This publishes the site to the `gh-pages` branch of the repository.

## GitHub Actions (optional, auto-deploy)
Uncomment the provided workflow in `.github/workflows/deploy.yml` and push to `main` to auto-deploy via GitHub Pages.

## Student workflow
1. Fork or create a branch.
2. Add/edit files in `docs/` (Markdown) or `docs/notebooks/` (notebooks).
3. Update `mkdocs.yml` `nav`.
4. Open a Pull Request.
5. After merge, the site is deployed.
