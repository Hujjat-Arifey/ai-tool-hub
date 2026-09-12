# AFI Tool Hub — Dev Setup

This project uses Flask + PostgreSQL. By default the app reads `DATABASE_URL` from the environment. Example values are in `.env.example`.

Run a local Postgres with Docker Compose:

```bash
docker-compose up -d
```

Set environment variables and run the app (PowerShell):

```powershell
$env:DATABASE_URL='postgresql://postgres:postgres@localhost:5432/postgres'
$env:FLASK_APP='app.py'
$env:SECRET_KEY='replace-with-a-secure-secret'
.venv\Scripts\Activate.ps1
python -m flask run
```

If you prefer Docker-only, start Postgres with `docker-compose up` and point your local Flask to the DB as above.
