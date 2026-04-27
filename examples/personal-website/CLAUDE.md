# My Site

Personal website. Static HTML/CSS/JS. Deployed to Netlify when I drag the folder into the Netlify dashboard (yes, manually — I'll automate it eventually).

## How I like to work

- I'm not a developer. Explain things plainly. Skip jargon when you can, or define it the first time.
- Show me what changed before saving — diff > prose description.
- If you're going to install something, ask first. I don't know what npm packages do.
- Don't refactor what I didn't ask you to refactor. "While I'm here let me also clean up..." has burned me.

## Stack

- HTML, CSS, vanilla JavaScript. No framework.
- A few images in `images/`.
- Netlify hosting.

## Project conventions

- Commits in plain English. No `feat:` / `fix:` prefixes.
- One branch, `main`. I'll worry about branching when the site is bigger.

## Key paths

- `index.html` — homepage
- `about.html` — about me
- `blog/` — blog posts (one HTML file per post)
- `style.css` — site-wide styles
- `images/` — photos

## Things I want you to catch me on

The rules I want enforced even when I forget. Better to write them down here than to keep them in my head.

- If I'm about to break the site (typo in HTML that breaks layout, missing closing tag), warn me before saving.
- If I'm about to commit a giant image (>2MB), tell me to compress it first.
- If I'm about to push something embarrassing (typo in a blog post, broken link, half-finished sentence), flag it.
- I sometimes forget to update the date on a blog post. Notice if I do.
- If I ask you to delete a file, double-check whether anything else links to it before deleting.

## Session start

1. Read `STATE.md` so you know what I was last working on.
2. Run `git status` to see what's uncommitted.
3. Ask me what I want to work on if it's not obvious.

## Session end

When I say "I'm done" or close the session, propose an update to `STATE.md` and wait for me to approve before writing it.
