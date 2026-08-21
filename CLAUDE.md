# CLAUDE.md

Operational guide for agents and humans working in this repo. Read it first, every session.

**What this is:** a one-page portfolio at a GitHub Pages URL. Four public side projects and a
short bio. Static HTML and CSS, no build step, no dependencies.

## The one principle

**The words are researched. The design is now decided, and the split still holds.**

Copy lives in `content/` and is verified against real sources. Design lives in `index.html`,
`tokens.css` and `styles.css`. The design pass has run; `docs/plan.md` decisions 5 to 7 record
what it chose and why.

✅ A design change restructures the page and re-picks type, colour and rhythm, using the copy
as written.
❌ A design change writes a punchier headline because the layout wanted one.

If a layout needs words that aren't in `content/`, write them into `content/` first and check
them against `content/facts.md`. If they can't pass that check, change the layout.

## Document map

| File | Read it when… |
| --- | --- |
| `docs/concept.md` | You need the why: audience, non-goals, what this page refuses to be. |
| `docs/plan.md` | You need the current phase, or the settled decisions and why they went that way. |
| `docs/design-brief.md` | You're about to design or build the page. Read this before Hallmark. |
| `content/about.md` | You need bio, background facts, contact, or the page's spine. |
| `content/projects.md` | You need project copy, links, stack, status, or available assets. |
| `content/facts.md` | **Before writing any user-facing word.** Accuracy and voice rules. |

## Hard invariants

1. **No invented facts.** No metric, testimonial, logo wall or traction number that isn't in
   `content/`. `content/facts.md` is the full rule and it outranks any layout.
2. **No employers, no titles, no dates, no contact details.** No company name appears on the
   page, ever, along with no job title tied to one, no career timeline, no claim about where
   I work now, no email in any form including `mailto:`, no contact form, no phone. LinkedIn
   and GitHub are the only two personal links.

   The page carries what doesn't change; LinkedIn carries what does. `content/facts.md` § 2
   and § 6 are the full rule. This is the invariant a design pass is most likely to break,
   because portfolio layouts reach for logo rows and timelines by default.
3. **No build step and no dependencies.** No npm, no bundler, no framework, no CDN script, no
   analytics, no font CDN. Raise it instead of adding it.
4. **Every path is relative.** No leading `/` on any `href` or `src`, so the page opens
   correctly from disk as well as from `https://batirko.github.io`.
5. **Light and dark are both defined**, and `body` carries an explicit background.
6. **Nothing gets published without me.** Don't create the GitHub repo, don't push to a
   remote, don't enable Pages. Scaffold and design; I press publish. The repo will be named
   `batirko.github.io`, serving at `https://batirko.github.io`.

## Design method

Hallmark, installed at `~/.claude/skills/hallmark/`. The default Design flow has already run,
and `.hallmark/log.json` records the pick. For a change, run `hallmark redesign` against the
current page rather than starting over.

`docs/design-brief.md` predates the design and two of its calls were overturned. Read
`docs/plan.md` decisions 5 to 7 for what the page actually does. The brief's hard constraints
and `content/facts.md` still stand.

## Handing back to me

Assume I've forgotten what the session was about. Lead with what the page now does or looks
like differently, and what decision you need from me. File names are supporting detail.
