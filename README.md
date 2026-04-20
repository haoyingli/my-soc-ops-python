# Mergington High School Activities API

A lightweight FastAPI project that powers a simple **activities signup experience** for students.

- Browse available extracurricular activities
- Sign up students by email
- Explore both a web UI and OpenAPI docs

## Why this project?

This repo is intentionally small and approachable, making it a great sandbox for:

- learning FastAPI fundamentals
- practicing API + frontend integration
- experimenting with secure, incremental code changes

## Quickstart

```bash
pip install -r requirements.txt
uvicorn src.app:app --reload
```

Then open:

- App: http://localhost:8000
- Swagger UI: http://localhost:8000/docs
- ReDoc: http://localhost:8000/redoc

## API at a glance

| Method | Endpoint | Purpose |
| --- | --- | --- |
| GET | `/activities` | Return all activities with schedules and participants |
| POST | `/activities/{activity_name}/signup?email=student@mergington.edu` | Sign up a student for an activity |

## Project layout

- `src/app.py` – FastAPI routes and in-memory data
- `src/static/app.js` – frontend API calls and signup flow
- `src/static/index.html` / `src/static/styles.css` – UI shell and styling

## Notes

- Data is stored **in memory** and resets on restart.
- This project intentionally avoids a database/ORM to stay focused on API behavior.

---

Built for the `haoyingli/my-soc-ops-python` learning project.
