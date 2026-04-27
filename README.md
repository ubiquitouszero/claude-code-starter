# Claude Code Starter Kit

A small set of files to drop into a new repo so Claude Code is useful from session one.

Pairs with:

- **[AI-Native Engineering](https://workiscode.com/articles/ai-native-engineering)** — the *why*. The doctrine behind this whole approach.
- **[Power Using Claude Code](https://notes.ath.how/claude-code-9ab6f0b2/)** — the *how*. Practitioner reference: install, talking to it, common moves.
- **This starter kit** — the *now*. What to actually drop in your repo.

Read the first two before you use this. It's a half-hour total and you'll get more out of every Claude session afterward.

## What's in here

| File | What it does |
|------|--------------|
| `CLAUDE.md` | Tells Claude what your project is, how you like to work, and what to catch you on. Claude reads this every session. **The most important file.** |
| `STATE.md` | A scratchpad for "where am I right now." Claude writes it, you approve. Claude reads it next session and you're back in context fast. |
| `.claude/settings.json` | Pre-approves common safe commands (ls, git status, cat, etc.) so you stop getting interrupted by permission prompts for routine stuff. |
| `.gitignore` snippet | Keeps your personal `.claude/settings.local.json` out of git. |
| `examples/` | Two filled-in CLAUDE.md + STATE.md sets — a [personal website](examples/personal-website/) and a [data scripts folder](examples/data-script/). Use them to calibrate what good looks like. |

## How to use it

1. Click **"Use this template"** at the top of the GitHub page to make your own copy. (Or `git clone` and `rm -rf .git` if you prefer.)
2. Open `CLAUDE.md` and replace the `[BRACKETED]` placeholders. Look at `examples/` for what filled-in versions look like. Five minutes here saves hours later.
3. Open `STATE.md` and write one or two lines about what you're working on. (Or skip it — Claude will offer to write the first one for you.)
4. Run `claude` in the repo. It'll pick up `CLAUDE.md` automatically.

That's it.

## Why these files exist (the actual reason)

You're allowed to be lazy. You're allowed to forget what folder a thing is in, what command runs the tests, what you decided three days ago. Cognitive debt is yours to manage — if you want to not know, that's your call.

The point of these files isn't to *force you* to be more disciplined. The point is to **give Claude enough context to catch you when you ask for something dumb**. Delete the wrong file? Claude should notice it's referenced elsewhere. About to commit data that's gitignored for a reason? Claude should stop you. Push to a branch you said was sacred? Claude should ask.

That only works if Claude knows what's true about your project. The files give it that picture. The "Things I want you to catch me on" section in `CLAUDE.md` is the most important part — it's where you arm Claude to be your safety net.

## Things to know

- **Permission prompts are training wheels.** Start with the defaults in `settings.json`. As you find yourself approving the same command over and over, add it to your personal allowlist (in `.claude/settings.local.json`, not `settings.json` — keep your personal stuff out of the shared file). Don't blanket-allow `Bash(*)` — that removes the safety net you set up.
- **`settings.json` vs `settings.local.json`.** `settings.json` is shared (committed to git, applies to anyone who clones your repo). `settings.local.json` is personal (gitignored, just for you). Add personal command allows there.
- **STATE.md is for Claude.** Not for you. Claude writes it at session end with your approval, reads it at session start, and is back in context fast. The point isn't your typing — it's that next-session Claude knows where you actually are.
- **You don't need ADRs, sessions, runbooks, or story points to start.** Add discipline when the pain of not having it shows up. Not before.

## When you outgrow this

If you're running serious multi-month projects, having repeated production incidents, or working across many repos that need consistent patterns, look into the heavier moves — architecture decision records (ADRs), session docs, root cause analyses, runbooks. They're worth it for serious projects, overkill for hobby ones. The [AI-Native Engineering](https://workiscode.com/articles/ai-native-engineering) doctrine has the full version.

## License

MIT — see [LICENSE](LICENSE). Use it, fork it, adapt it. No attribution required (but appreciated).
