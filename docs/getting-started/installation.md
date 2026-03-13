# Installation

## From PyPI

```bash
pip install airqoair
```

## From This Repository

```bash
pip install -e ".[dev]"
```

## Docs Dependencies

To build the documentation site locally:

```bash
python -m pip install -r requirements-docs.txt
python -m mkdocs serve
```

The site configuration lives in `mkdocs.yml`.

## Recommended local workflow

For package work:

```bash
pip install -e ".[dev]"
python -m pytest tests
```

For documentation work:

```bash
python -m pip install -r requirements-docs.txt
python -m mkdocs serve
```

## GitHub Pages deployment

To build the site locally without publishing it:

```bash
python -m mkdocs build --strict
```

The repository publishes docs automatically from `main` using GitHub Actions:

```bash
.github/workflows/deploy-docs.yml
```

In the repository settings, GitHub Pages should be configured to use `GitHub Actions` as the source.

Do not use `Deploy from a branch` with the `docs/` folder for this site. That serves the raw Markdown files and bypasses the MkDocs Material theme, which makes the published site look unstyled compared with `mkdocs serve`.

For this repository, the published site URL is:

```text
https://wabinyai.github.io/airqoair-project/
```

If you need the site to live at `https://airqoair-project.github.io/book/`, that requires a different GitHub owner/repository setup or a custom domain configuration outside this repository.
