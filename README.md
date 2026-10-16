# Rehabit PT

A Django application for a physical therapy clinic, including appointment booking, a patient portal, and staff charting.

## Local setup

Requires Python and pip. From this directory, run:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Open http://127.0.0.1:8000/.

## Configuration

The application reads these environment variables:

- `DJANGO_SECRET_KEY`: use a unique secret for deployment.
- `DJANGO_DEBUG`: defaults to `True` for local development; set to `False` for deployment.
- `DJANGO_ALLOWED_HOSTS`: comma-separated hostnames; defaults to `127.0.0.1,localhost`.

The local SQLite database, virtual environments, uploaded files in `media/`, and `.env` files are excluded from Git. A fresh checkout starts with a new database after running migrations. Back up existing databases and uploads separately.
