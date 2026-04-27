# Claude Code Starter Kit

A small set of files to drop into a new repo so Claude Code is useful from session one.

Assumes you've already installed Claude Code and read [Power Using Claude Code](https://notes.ath.how/claude-code-9ab6f0b2/).

## What's in here

| File | What it does |
|------|--------------|
| `CLAUDE.md` | Tells Claude what your project is, how you like to work, and what to avoid. Claude reads this automatically every session. **The most important file.** |
| `STATE.md` | A scratchpad for "where am I right now." Optional but recommended. Update at the end of a session so the next one starts fast. |
| `.claude/settings.json` | Pre-approves common safe commands (ls, git status, cat, etc.) so you stop getting interrupted by permission prompts for routine stuff. |
| `.gitignore` snippet | Keeps your personal `.claude/settings.local.json` out of git. |

## How to use it

1. Copy the four files into the root of your repo.
2. Open `CLAUDE.md` and replace the `[BRACKETED]` placeholders. This takes 5 minutes and pays off every session afterward.
3. Open `STATE.md` and write one or two lines about what you're working on.
4. (Optional) Add the `.gitignore` snippet to your existing `.gitignore` if you have one.
5. Run `claude` in the repo. It'll pick up `CLAUDE.md` automatically.

That's it.

## Things to know

- **`CLAUDE.md` is the highest-leverage file you'll ever write.** Spend 5 minutes on it now, save hours later. Update it whenever you correct Claude on the same thing twice.
- **Permission prompts are training wheels.** Start with the defaults in `settings.json`, add more as you find yourself approving the same command repeatedly. Don't blanket-allow `Bash(*)`.
- **STATE.md is for you, not Claude.** It works because you have to write it. The act of writing "where am I" forces you to actually know.
- **You don't need ADRs, sessions, runbooks, or story points to start.** Add discipline when the pain of not having it shows up. Not before.

## When you outgrow this

If you start having repeated incidents, complex multi-session projects, or want institutional memory across many repos, look into the heavier patterns: architecture decision records, session docs, root cause analyses. They're worth it for serious projects, overkill for hobby ones.
