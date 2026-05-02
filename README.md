# Set You Free

Streamlit application for automated structured literature search across multiple databases and preprint servers.

The app is designed to support review workflows by searching external sources, helping with cross-reference search, removing likely duplicates, and exporting results for structured review tools such as Rayyan or CADIMA.

## Features

- Search workflow for structured literature review.
- Cross-reference search based on references found in search results.
- Duplicate reduction across multiple sources.
- Study selection and result review pages.
- Export-oriented workflow for downstream review tools.

## Repository Layout

- `src/home.py` - Streamlit app entry point.
- `src/pages/` - Streamlit multipage workflow:
  - search
  - study selection
  - results
- `src/utils/` - search engine, site configuration, and shared constants.
- `pyproject.toml` - Poetry project metadata.
- `poetry.lock` - locked dependency set used for the local `.venv`.

## Local Setup

```bash
poetry install --no-root
poetry run python --version
```

Poetry is configured on this machine to create the virtual environment inside the project as `.venv/`.

## Run

```bash
poetry run streamlit run src/home.py
```

## Dependency Notes

- Python 3.10 is currently used for the local `.venv`.
- The app depends on `findpapers` from the `develop` branch of `ChristianGerloff/findpapers`.
- `poetry.lock` is intentionally tracked so the app can be recreated more reliably.

## Secrets and Local Configuration

Do not commit API keys, private tokens, or personal search credentials. Keep local configuration in ignored files or environment variables.

## Authors

Christian Gerloff, Leon Lotter, Kashyap Maheshwari

## Citation

If you use Set You Free, cite:

Gerloff C., Lotter L., & Maheshwari K. (2020). Set You Free: Automated Structured Literature Search.
