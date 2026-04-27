# [PROJECT NAME]

[One sentence: what this project does and who uses it.]

## How I like to work

[The single highest-leverage section. Tell Claude what you care about so it doesn't have to guess. A few examples — keep what fits, replace the rest.]

- Direct answers, no preamble. Skip the "Great question!" stuff.
- Show me the diff before applying big changes.
- If you don't know, say so. Don't guess at file paths or API shapes.
- Ask before installing new dependencies.
- Don't refactor what I didn't ask you to refactor.

## Stack

[List the main tools/languages/frameworks. Example: Python 3.12, FastAPI, Postgres, Vite + React frontend.]

## Project conventions

- [Commit format, e.g. `type(scope): message` — feat / fix / docs / refactor]
- [Branch naming, e.g. `feat/short-description`]
- [Code style notes, e.g. "use type hints everywhere", "no default exports"]

## Key paths

- [Source: `src/`]
- [Tests: `tests/`]
- [Config: `config/`]

## Commands

- [Run dev server: `npm run dev`]
- [Run tests: `pytest`]
- [Lint: `ruff check .`]

## Things I want you to catch me on

[Project rules you want consistently enforced even when you forget. Better to write them down once than to remember them every session. Add to this whenever you correct Claude on the same thing twice — that's the project brain telling you it needed that rule written down.]

- Don't push to `main` directly. Always open a PR.
- Don't commit secrets. Check `.env.example` for what should be in `.env`.
- [Add things here as you discover them.]

## Session start

1. Read `STATE.md` to see where I left off.
2. Run `git status` and `git log -5` to see what's recent.
3. Ask me what I want to work on if it's not obvious.

## Session end

When I say "I'm done" (or it's clear we're wrapping), propose an update to `STATE.md` and wait for my approval before writing it. Don't write the file silently — show me the diff first.
