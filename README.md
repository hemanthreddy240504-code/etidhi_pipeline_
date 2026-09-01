# EtiDhi Pipeline Intelligence Tracker

A learning-focused full-stack demo with a FastAPI backend, SQLite database, and responsive frontend. It includes dummy pipeline data and analytics to make the application more useful than an Excel tracker.

## Features
- Company CRUD (create, edit, delete)
- SQLite persistent database (`pipeline.db`)
- Company profile: industry, city, website, employee band
- EtiDhi partner: KOGO / Contineu / Other
- Expected signup value and probability
- Pipeline stages
- Account owner + supporting team members
- Client POC details
- Lead source, dates, next action and notes
- Search and filters
- KPI dashboard
- Weighted pipeline forecast
- Pipeline by stage, partner, owner and industry
- Expected signup trend by month
- Stale-opportunity alert (no contact >14 days)

## Run locally
1. Install Python 3.10+
2. Open terminal in this folder
3. `python -m venv .venv`
4. Windows: `.venv\\Scripts\\activate`  | macOS/Linux: `source .venv/bin/activate`
5. `pip install -r requirements.txt`
6. `uvicorn app.main:app --reload`
7. Open http://127.0.0.1:8000

The first run automatically seeds 15 dummy companies. Delete `pipeline.db` and restart if you want to reset the dummy data.

## API
- GET `/api/companies`
- POST `/api/companies`
- PUT `/api/companies/{id}`
- DELETE `/api/companies/{id}`
- GET `/api/analytics`
- GET `/docs` for FastAPI Swagger docs

## Next production steps
- Authentication / role-based permissions
- PostgreSQL instead of SQLite
- Audit history for stage/value changes
- Activity timeline and reminders
- CSV/Excel import and export
- Actual partner/client master tables with foreign keys
- Deployment to a cloud host
- Automated tests and CI/CD
