# Claude Code Starter Kit

A small set of files to drop into a new repo so Claude Code is useful from session one.

## Before this kit

This kit assumes you already have Claude Code installed and can run `claude` in a terminal. If that sentence didn't fully make sense, install first and come back. The files here only do their job once Claude Code is up and running on your machine.

Start with one of these:

- [Claude Code 101](https://anthropic.skilljar.com/claude-code-101). Anthropic's free interactive course. Best if you want guided, hands-on.
- [Claude Code Quickstart](https://code.claude.com/docs/en/quickstart). The official install and first-run docs. Best if you just want the steps.
- [CC for Everyone](https://ccforeveryone.com/). Free community course, no coding experience required. Best if you're brand new to this whole world.

Once `claude` runs in your terminal, come back here.

---

Pairs with:

- **[AI-Native Engineering](https://workiscode.com/articles/ai-native-engineering).** The *why*. The doctrine behind this whole approach.
- **[Power Using Claude Code](https://notes.ath.how/claude-code-9ab6f0b2/).** The *how*. Practitioner reference: install, talking to it, common moves.
- **This starter kit.** The *now*. What to actually drop in your repo.

Read the first two before you use this. It's a half-hour total and you'll get more out of every Claude session afterward.

## What's in here

| File | What it does |
| ---- | ------------ |
| `CLAUDE.md` | Tells Claude what your project is, how you like to work, and what to catch you on. Claude reads this every session. **The most important file.** |
| `STATE.md` | A scratchpad for "where am I right now." Claude writes it, you approve. Claude reads it next session and you're back in context fast. |
| `GLOSSARY.md` | Plain-English definitions of every Claude Code term used in this kit. Read entries when something is unfamiliar. You don't need to memorize it up front. |
| `.claude/settings.json` | Pre-approves common safe commands (ls, git status, cat, etc.) so you stop getting interrupted by permission prompts for routine stuff. |
| `.gitignore` snippet | Keeps your personal `.claude/settings.local.json` out of git. |
| `examples/` | Two filled-in CLAUDE.md + STATE.md sets. One for a [personal website](examples/personal-website/), one for a [data scripts folder](examples/data-script/). Use them to calibrate what good looks like. |

## How to use it

1. Click **"Use this template"** at the top of the GitHub page to make your own copy. (Or `git clone` and `rm -rf .git` if you prefer.)
2. Run `claude` in the new repo and say **"help me set this up."** Claude will read the templates, see the brackets, and walk you through filling them in one section at a time, proposing each update for your approval before writing. No find-and-replace, no fighting with markdown.
3. That's it. Claude has the project brain populated and is ready to work.

If you'd rather fill the templates in by hand, look at the [`examples/`](examples/) folder for what filled-in versions look like. The walked-through path is faster.

## Why these files exist

Think of them as the project's **brain**. An external memory the project carries so you don't have to.

You shouldn't have to remember which folder things live in, what command runs the tests, what you decided three days ago, or what conventions you set last week. The system remembers it for you. When something happens that you don't remember (a quirk of the deploy, a decision about which library to use, the reason a file is structured a certain way), the project brain has it written down. Claude reads the brain at the start of every session, so the project's memory comes back online before you do.

This is the basic version. `CLAUDE.md` is the persistent context (who, what, how). `STATE.md` is the working memory (where you are right now). `settings.json` is the muscle memory (what's safe to do without asking). Together they replace "I should remember to..." with "the system already knows."

The bigger version of the same idea (architecture decision records, session docs, runbooks, root cause analyses) lives in [AI-Native Engineering](https://workiscode.com/articles/ai-native-engineering). Add those when the pain of not having them shows up. Until then, this is enough.

## Things to know

- **Permission prompts are training wheels.** Start with the defaults in `settings.json`. As you find yourself approving the same command over and over, add it to your personal allowlist. Use `.claude/settings.local.json`, not `settings.json`, so your personal stuff stays out of the shared file. Don't blanket-allow `Bash(*)`. The prompts are how the project keeps track of what it's actually OK with.
- **`settings.json` vs `settings.local.json`.** `settings.json` is shared (committed to git, applies to anyone who clones your repo). `settings.local.json` is personal (gitignored, just for you). Add personal command allows there.
- **STATE.md is the project's working memory.** Claude proposes the update at session end, you approve. Next session, Claude reads it first and you're back in context.
- **You don't need ADRs, sessions, runbooks, or story points to start.** Add discipline through code when the pain of not having it shows up. Not before.

## When you outgrow this

If you're running serious multi-month projects, having repeated production incidents, or working across many repos that need consistent patterns, look into the heavier moves: architecture decision records (ADRs), session docs, root cause analyses, runbooks. They're worth it for serious projects, overkill for hobby ones. The [AI-Native Engineering](https://workiscode.com/articles/ai-native-engineering) doctrine has the full version.

## License

MIT. See [LICENSE](LICENSE). Use it, fork it, adapt it. No attribution required (but appreciated).
