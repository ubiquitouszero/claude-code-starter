# Bookkeeping Scripts

A folder of small Python scripts I use to wrangle data for taxes and bookkeeping. Each script does one thing: pull a CSV, parse it, output something cleaner.

## How I like to work

- I want to understand what a script is doing. Add inline comments where the logic isn't obvious. Plain English, not "increments counter."
- Don't over-engineer. If a script is 30 lines, keep it 30 lines. No classes, no abstractions, no "what if we want to extend this later."
- When you change a script, run it on `data/sample.csv` and show me the output before we call it done.
- I can't read regex. If you write one, comment what it matches in plain English.

## Stack

- Python 3.12.
- `pandas` for the heavier scripts, plain stdlib (`csv`, `json`, `pathlib`) for the simple ones.
- No virtual env yet. I install with `pip install --user`. The venv setup confused me.
- Scripts run from the command line: `python scripts/whatever.py`.

## Project conventions

- One file per script. Filename describes what it does (`split_quarterly_invoices.py`, not `processor.py`).
- Output goes to `output/` (gitignored).
- Input data goes to `data/` (gitignored, has personal stuff).
- `data/sample.csv` is the one exception. Fake data for testing, NOT gitignored.
- Commits in plain English.

## Key paths

- `scripts/`: the actual Python scripts
- `data/`: input CSVs (gitignored)
- `output/`: generated files (gitignored)
- `data/sample.csv`: fake data for testing

## Things I want you to catch me on

The rules I want enforced even when I forget. Better to write them down here than to keep them in my head.

- If I'm about to write a script that reads from `data/` and writes to `data/`, stop me. Output goes to `output/`.
- If I'm about to commit anything from `data/` or `output/`, stop me. Real data should never end up in git. The `.gitignore` should prevent this but check anyway.
- If a script needs a new pip package, tell me what it does and what other packages it pulls in before installing.
- Don't trust my numbers. If I say "this should give me 12 rows" and you get 11, tell me, don't quietly continue.
- If I ask you to delete a script, check whether any other script imports from it first.

## Session start

1. Read `STATE.md` so you know what I was last working on.
2. Run `ls scripts/` so you know what scripts exist.
3. Ask me what I want to work on if it's not obvious.

## Session end

When I say "I'm done", propose a `STATE.md` update and wait for my approval before writing it.
