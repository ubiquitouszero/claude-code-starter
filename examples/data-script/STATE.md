# State

**Last updated:** 2026-04-20

## What I'm working on

A new script `merge_bank_csvs.py` that takes the monthly bank CSV exports and merges them into one annual file with a normalized column order. Banks export columns in slightly different orders depending on the export date, which is annoying.

## Where I left off

- Script reads all files in `data/bank/` and merges them. Works for the 2025 files.
- Hit a problem with the December 2024 file — the "Description" column was renamed to "Memo" in the bank's UI sometime in early 2024. Older files use "Memo", newer ones use "Description".
- Half-built a column-renaming step but got stuck on whether to also normalize date formats (some files are MM/DD/YYYY, others YYYY-MM-DD).

## Decisions in flight

- Pandas vs plain `csv` module. Started in pandas but only using `read_csv` and `concat`. Could probably do this in 20 lines of stdlib. Leaning toward stdlib for the rewrite.
- Whether to detect column-name changes automatically or hardcode a mapping. Hardcoding is simpler, but a new bank statement next month might break it.

## Things to remember

- The European-bank exports use a comma decimal separator instead of a period. Haven't handled that yet — will break.
- I think I have one more bank account I haven't pulled CSVs for. Check before running the final merge.
