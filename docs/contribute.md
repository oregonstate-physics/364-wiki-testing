---
tags: [guide]
---

# How to Contribute

> Goal: practice making contributions to a GitHub repo that show up on a wiki-like site.

## 1) Workflow (student)
1. Create a branch or fork the repo.
2. Add a Markdown page under `docs/` or a notebook under `docs/notebooks/`.
3. Update `mkdocs.yml` → `nav` to include your new page.
4. Commit & push your branch; open a Pull Request.
5. After your PR is merged, the site will be published.

## 2) Writing pages in Markdown
Create a file, e.g. `docs/example.md`:

```markdown
# Example Page

Write in Markdown. You can add headings, lists, images, and code blocks.
```

Add it to `mkdocs.yml`:

```yaml
nav:
  - Home: index.md
  - Contribute: contribute.md
  - Example: example.md
```

## 3) Adding a Jupyter Notebook page
Place your notebook here: `docs/notebooks/<your-name>.ipynb`.
Then add it to `mkdocs.yml`:

```yaml
nav:
  - Demo Notebook: notebooks/intro.ipynb
  - Your Notebook: notebooks/your-name.ipynb
```

### Tips for cleaner diffs
- Clear outputs before committing (or rely on build-time execution if the instructor enables it).
- Keep notebooks small and focused.

## 4) Preview locally
```bash
pip install -r requirements.txt
mkdocs serve
```

## 5) Deploy (instructor)
The simplest method is:
```bash
mkdocs gh-deploy
```
This publishes to the `gh-pages` branch. In repo **Settings → Pages**, set Source to **GitHub Actions** or to the published branch.
