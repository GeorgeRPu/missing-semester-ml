# Missing Semester ML — Agent Guide

## Project overview

A JupyterBook-based educational website covering practical ML topics (MLOps, EDA, experiment tracking, etc.) that are rarely taught in university courses or online curricula. Modelled after [MIT Missing Semester](https://missing.csail.mit.edu/).

## Tech stack

- **JupyterBook 2.x** — static site generator (MyST-based engine)
- **GitHub Actions** — builds and deploys to GitHub Pages on push to `main`
- **Custom CSS** (`_static/custom.css`) — MIT Missing Semester colour palette and typography

## Repository structure

```
.
├── _config.yml          # JupyterBook site configuration
├── _toc.yml             # Table of contents (add new pages here)
├── requirements.txt     # Python dependencies
├── intro.md             # Homepage / landing page
├── _static/
│   └── custom.css       # Theme overrides (fonts, purple palette)
├── .github/
│   └── workflows/
│       └── deploy.yml   # GitHub Pages deployment workflow
└── modules/             # Course content (not yet created)
```

## Development

Install dependencies and build locally:

```bash
pip install -r requirements.txt
jupyter-book build .
# Open _build/html/index.html in a browser
```

## Adding content

1. Create a Markdown (`.md`) or Jupyter notebook (`.ipynb`) file under `modules/`
2. Register it in `_toc.yml`
3. Run a local build to verify

## Conventions

- Keep `_toc.yml` in sync with any new or removed pages — JupyterBook will error on missing files
- Do not commit `_build/` (it is gitignored by JupyterBook)
- Notebook execution is set to `"off"` in `_config.yml`; include pre-executed outputs if you want them rendered
