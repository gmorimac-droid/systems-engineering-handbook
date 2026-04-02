# Systems Engineering Handbook

Repository skeleton for a MkDocs-based **Systems Engineering Handbook**.

## Included

- full `docs/` information architecture
- starter `mkdocs.yml`
- `requirements.txt`
- GitHub Actions deployment workflow
- `overrides/` directory for future theme customizations

## Local setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

## Build

```bash
mkdocs build
```

## Deploy

The repository includes a basic GitHub Actions workflow for deployment to GitHub Pages.
