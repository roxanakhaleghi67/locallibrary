# LocalLibrary — Django practice project

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) ![Django](https://img.shields.io/badge/Django-5.0-092E20)

A minimal Django 5 application scaffold for a local library catalogue, created as a
learning project with `django-admin startproject`.

## Current state

| Part | Status |
| --- | --- |
| Project configuration (`locallibrary/settings.py`, `urls.py`, `asgi.py`, `wsgi.py`) | Complete, runs |
| `catalog` app registration | Complete (`catalog.apps.CatalogConfig`) |
| Models (author, book, genre, book instance) | **Not implemented** — `models.py` is the generated stub |
| Views, URLs, templates | **Not implemented** — stubs only |
| Admin registration | **Not implemented** |

In short: the project runs, but the catalogue features are still to be written. This README
describes it as it is rather than as it will be.

## Requirements

- Python 3.10+
- Django 5.0 (see `requirements.txt`)

```bash
python -m pip install -r requirements.txt
```

## Run locally

```bash
python manage.py migrate
python manage.py runserver
```

Then open <http://127.0.0.1:8000/>. The database file (`db.sqlite3`) is created on first
migrate and is intentionally **not** tracked in git.

## Project structure

```text
locallibrary/
  manage.py
  locallibrary/     # settings, URLs, WSGI/ASGI entry points
  catalog/          # the application: models, views, urls, admin, migrations
```

## Notes

- `SECRET_KEY` and `DEBUG=True` in `settings.py` are development defaults. Move them to
  environment variables before deploying.
- Tests: `python manage.py test` runs the (currently empty) test suite.

## Next steps

Define the catalogue models, register them in the admin, add list/detail views and
templates, then cover the models and views with tests.

## License

MIT — see [LICENSE](LICENSE). © Roxana Khaleghi
