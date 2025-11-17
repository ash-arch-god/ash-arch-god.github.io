# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project overview

- Name: **Student Test Portal**.
- Purpose: Web application where an admin uploads and schedules tests; students log in, take assigned tests, and submit answers; admin reviews results and basic statistics.
- Source: Summarized from `README.md`.

## Commands and workflows

**Current state:** This repository currently contains only `README.md` and `.gitignore` and does **not** define any build, lint, or test tooling yet (no `package.json`, `pyproject.toml`, `go.mod`, etc.).

Once implementation is added, update this section with concrete commands. Until then, use the following checklist when tooling appears:

- **JavaScript/TypeScript (Node/React/etc.)**
  - Look for `package.json`.
  - Typical commands to document here (examples; replace with actual scripts once present):
    - Install deps: `npm install` or `pnpm install` or `yarn install`.
    - Start dev server: `npm run dev`.
    - Build: `npm run build`.
    - Lint: `npm run lint`.
    - Tests (all): `npm test` or `npm run test`.
    - Single test (Jest/Vitest): `npm test -- <pattern>`.
- **Python (Django/FastAPI/etc.)**
  - Look for `pyproject.toml` or `requirements.txt`.
  - Typical commands to document here (examples; replace with actual project commands):
    - Create venv: `python -m venv .venv`.
    - Install deps: `pip install -r requirements.txt` or `pip install -e .`.
    - Run app: framework-specific (e.g. `uvicorn app:app --reload` or `python manage.py runserver`).
    - Tests (pytest): `pytest` and `pytest path/to/test_file.py -k test_name` for a single test.
- **Other stacks**
  - For other ecosystems (Java, Go, .NET, etc.), once their config files (`pom.xml`, `go.mod`, `*.csproj`, etc.) appear, add build, lint, and test commands here.

When you add real tooling, **replace the example commands above with the actual project-specific commands** instead of appending them.

## Architecture and code structure

**Current state:** There is no application source code in the repository yet, so high-level architecture cannot be described.

Once code exists, update this section to briefly describe the big-picture structure, for example:

- Main application entrypoints (e.g. web server, SPA entry file, or backend service startup).
- Separation between admin functionality (test management, scheduling, results/stats views) and student functionality (authentication, test-taking UI, submission flows).
- Data access layer (e.g. ORM models or database access modules) and how tests, questions, options, answers, and results are represented.
- Any shared domain modules or utility layers used across admin and student flows.

Avoid enumerating every file; focus on how major modules and services interact.

## How future Warp agents should update this file

- After initial implementation lands, revisit `WARP.md` to:
  - Replace placeholder command examples with the real dev, build, lint, and test commands.
  - Add a concise architecture overview that reflects the actual code layout.
- Keep the focus on **project-specific** details (tooling, architecture, non-obvious workflows) rather than generic advice.
