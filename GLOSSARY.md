# Glossary

Plain-English definitions of every term used in this starter kit. You don't need to memorize it. Read entries when something is unfamiliar.

## Files this template uses

**CLAUDE.md** - A markdown file in your repo that Claude reads at the start of every session. It tells Claude who you are, what the project is, and how you like to work. Think of it as the instruction manual Claude reads before you talk.

**STATE.md** - A markdown file that captures where you left off last session: what you were working on, what's next, what's blocking you. Claude reads it at session start and proposes updates at session end. The "save game" file for your project.

**.claude/** - A hidden folder Claude Code looks for in your repo. Holds Claude-specific settings. The leading dot makes it hidden in most file browsers; you may need to enable "show hidden files" to see it.

**settings.json / settings.local.json** - Two configuration files inside `.claude/`. `settings.json` is shared (committed to git, applies to anyone who clones your repo). `settings.local.json` is personal (gitignored, only on your machine). Put personal command approvals in `.local`.

## Claude Code concepts

**Session** - One run of Claude Code, from when you start it until you exit. Claude's memory of the conversation only lives within a session. That's why STATE.md exists, to carry context across sessions.

**Context** - In the Claude sense: the text Claude can "see" right now (your messages, file contents it has read, tool results). It has a finite size. When it fills up, older messages get summarized or dropped. Different from the everyday meaning of the word.

**Allowlist** - A list of commands Claude can run without asking you to approve each time. The opposite of a blocklist. Lives in `settings.json` and `settings.local.json`.

**Permission prompt** - When Claude wants to run a command that isn't on the allowlist, it pauses and asks. You can approve once, approve always, or deny.

**Agent / subagent** - A separate Claude session that runs a focused subtask in the background and reports back. Useful for "go research this without cluttering my main conversation."

**Hook** - A shell command that runs automatically in response to a Claude Code event (for example, before a tool runs, or after a session ends). Configured in `settings.json`. Advanced. Most beginners don't need to write any.

**MCP server** - A separate program that gives Claude extra tools (Slack, Google Drive, a database, etc.). MCP stands for Model Context Protocol. Optional. Most beginners don't need this on day one.

## Programming and git terms (for non-programmers)

**Repo / repository** - A folder of files tracked by git, a version-control system. Contains a hidden `.git/` folder with the history of every change. Every project on GitHub is a repo.

**Commit** - A single saved snapshot of your changes, with a short message describing what changed. Like a checkpoint in a video game.

**Branch** - A separate line of work in your repo. Lets you experiment without affecting the main version.

**main** - The default name for the primary branch. The "official" version of the project. Convention: don't push broken code here.

**PR / pull request** - A formal proposal to merge changes from one branch into another (usually into `main`). Lets others review before the changes land.

**Diff** - A view that shows exactly what changed between two versions of a file: lines added (`+`), lines removed (`-`). Useful for reviewing before you save or commit.

**Markdown** - A plain-text format with simple rules for formatting (`**bold**`, `# headings`, `- bullets`). Files end in `.md`. The template is entirely markdown.

**Dependency** - A piece of code your project relies on that someone else wrote (a library or package). Adding one means downloading and trusting that code.

**Dotfile** - Any file or folder whose name starts with a dot. Hidden by default in most file browsers.
