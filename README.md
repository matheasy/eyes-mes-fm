# eyes.mes.fm: EyesIsWatchin App Lab

Steve's space for apps. Everything in this repository is published at **https://eyes.mes.fm**
about a minute after it lands on the `main` branch (its own Vercel project, separate from mes.fm).

## How it is laid out

- `index.html` = the home page with a card per app.
- One folder per app: `my-app/index.html` (plus its own `.js`, `.css`, images) is served at `eyes.mes.fm/my-app/`.
- Plain HTML / CSS / JavaScript works as-is. No build step is needed.

## Making an app with Grok

1. In Grok, connect GitHub (Settings -> Connectors -> GitHub) and allow it access to this repository,
   or use Grok Build's **Export to GitHub** on a finished app.
2. Ask Grok for the app as a single folder, e.g. "make a dice roller as `dice/index.html`, plain HTML/CSS/JS,
   no build step", and have it commit to `main` of `matheasy/eyes-mes-fm`.
3. Add a card for it to `index.html` (Grok can do that in the same commit).
4. Wait ~1 minute and open `https://eyes.mes.fm/<folder>/`.

No Grok connector? Open the repository on github.com -> **Add file -> Upload files**, drop the folder in,
then **Commit changes**. That publishes it the same way.

## Rules of thumb

- Keep secrets (API keys, passwords) out of this repository: it is public.
- If a change breaks the site, go to the repository's **Commits**, open the last good one and use
  **Revert**, or ask Grok to undo its last commit.
