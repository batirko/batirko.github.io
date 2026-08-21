# vitalii-batyr

A one-page portfolio, served as a static site from GitHub Pages.

Four public side projects and a short bio. Hand-written HTML and CSS. No build step, no
dependencies, no analytics.

## Run it

Open `index.html` in a browser. That's the whole toolchain.

For a local server, if you want one:

```bash
python3 -m http.server 8000
```

## Where things are

| Path | What it holds |
| --- | --- |
| `index.html` | The page. One file, hand-written. |
| `tokens.css` | Every colour, font, size and space, as named custom properties. |
| `styles.css` | The layout. It declares no literal colour and no literal font. |
| `fonts/` | IBM Plex Sans and IBM Plex Mono, self-hosted, 72 KB, with their licence. |
| `assets/` | Three real product screenshots and one animated loop. |
| `content/` | Every word the page may say, verified against real sources. |
| `docs/` | Concept, plan, and the design brief that the plan now supersedes. |
| `CLAUDE.md` | How to work in this repo. |

Copy is separate from design on purpose. A redesign restructures the page and never rewrites
the words. `content/facts.md` says what may never be claimed and outranks everything else.

## Design

Built with [Hallmark](https://www.usehallmark.com/), an anti-AI-slop design skill for coding
agents. Five projects come first, then the bio, then two links. Each project is a row: name,
one-line and links on the left, prose, screenshot and spec on the right.

Set in IBM Plex Sans and IBM Plex Mono. Charcoal-blue paper with an acid-lime accent, designed
dark and adapted to light. Nothing on the page moves on its own; writtten's loop shows a still
frame until a reader presses play.

`docs/plan.md` decisions 5 to 7 hold the reasoning. `docs/design-brief.md` predates the design
pass and no longer describes the page.

## Deploy

GitHub Pages, serving from `main` at the repository root. `.nojekyll` keeps Pages from running
the site through Jekyll.

The repo is named `batirko.github.io`, so the site serves at `https://batirko.github.io`.
Every path is relative, so nothing needs a base-path config.

## Licence

The code is free to borrow. The content is about a real person and isn't.
