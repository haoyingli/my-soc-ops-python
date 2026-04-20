# Agent Instructions

## Mandatory Development Checklist
Run all three before finishing a code change:
- Lint: `ruff check src` (if unavailable, install with `pip install ruff`)
- Build check: `python -m compileall src`
- Test: `pytest`

## Run and Verify
- Install deps: `pip install -r requirements.txt`
- Run app: `uvicorn src.app:app --reload`
- URLs: `http://localhost:8000`, `http://localhost:8000/docs`

## High-Value Map
- `src/app.py`: API routes + in-memory data
- `src/static/app.js`: frontend API calls + signup flow
- `src/static/index.html`, `src/static/styles.css`: UI shell and styles

## Required Conventions
- No DB/ORM; keep changes simple and local
- Keep frontend/backend contract aligned:
  - `GET /activities`
  - `POST /activities/{activity_name}/signup?email=...`
- Data resets on restart; never assume persistence
- If endpoint behavior changes, update `src/static/app.js` in the same change

## Reference Docs
- [README.md](README.md)
- [src/README.md](src/README.md)
