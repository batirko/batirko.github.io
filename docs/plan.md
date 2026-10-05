# Plan

Small project. Three phases, then it's done and only gets touched when a project changes.

## Phase 0 — scaffold ✅ done 2026-08-21

- [x] Content researched from the four repos and from `career-ops`, written into `content/`
- [x] Accuracy rules pulled forward from the CV rules into `content/facts.md`
- [x] Concept, design brief and this plan written
- [x] Placeholder `index.html` that deploys and reads correctly with no design applied
- [x] Local git repo initialised

## Phase 1 — design ✅ done 2026-08-21

- [x] Ran the Hallmark Design flow. Decisions 5 to 7 below record what came out of it.
- [x] Copied the two real screenshots into `assets/` and wired them in
- [x] Verified at 320, 375, 414, 768, 1024, 1440 and 1920px, in light and dark
- [x] Checked every line of the page against [`../content/facts.md`](../content/facts.md)

**What the page is now.** Projects first, then the bio, then two links. Each project is a row:
name, one-line and links on the left, prose, screenshot and spec on the right. Set in IBM Plex
Sans and IBM Plex Mono, served from `fonts/`. Dark charcoal-blue paper with an acid-lime
accent, adapted to a light counterpart. Nothing on the page moves on its own.

**Seven projects**, since 2026-10-05. Agentic Workspaces leads, then writtten, whatatake,
research-and-learn, mova, vibecoding-starterpack, agentic-job-hunt. Five of the seven carry a
screenshot. Decisions 10 and 11 say what the sixth and seventh cost.

### 8. One description paragraph per project, 180 to 350 characters ✅ 2026-08-21

Each card carries one paragraph, not two. The wording and the measured counts are in
[`../content/projects.md`](../content/projects.md) § The card paragraph, along with what each
one dropped.

The constraint does two jobs. It forces every card to make a single claim, and it holds the
page at 4,581px on a 1280×900 desktop — 5.1 screens with five projects and three screenshots,
where two paragraphs each ran 5.8.

**A card that grows past 350 characters is the signal to cut, not to widen the range.** The
longer copy each card used to carry is still in `content/projects.md`, so nothing is lost.

## Phase 2 — publish ✅ done 2026-08-21

**Live at https://batirko.github.io.**

- [x] Confirmed every outbound link resolves, including agentic-workspaces.com, which went up
      the same day
- [x] Created the public repo `batirko.github.io`
- [x] Pages serves from `main` at the root, HTTPS enforced, build green
- [ ] Open the live URL on a phone before telling anyone
- [ ] Add the URL to the LinkedIn profile and to the GitHub profile

### The published history starts at one commit, on purpose

The scaffold history carried reference material this repo shouldn't publish: education, the
languages, and paths into a private repo. Deleting the file would not have removed it, because
git keeps the history. So the material was cut, and the public history was created fresh from
the redacted tree.

**The full original history is preserved locally on the `private-history` branch. Never push
it.** If you ever need what was cut, it is there.

`content/about.md` now says what is deliberately absent and why, so a future session doesn't
read the gap as an oversight and go looking to fill it.

## Decisions — settled 2026-08-21

### 1. Repo name is `batirko.github.io` ✅

The site lives at `https://batirko.github.io`. That spends the one user site GitHub allows per
account, deliberately: this is the page most likely to want that URL.

The local folder stays `~/Projects/vitalii-batyr`. Folder name and repo name don't have to
match. Every path in the site is relative, so nothing needs a base-path config.

### 2. The page names no employers, and carries no direct contact details ✅

**The page carries what doesn't change. LinkedIn carries what does.**

No company names, no job titles tied to a company, no dates, no claims about where I work now.
The bio describes what I work on and how I think about it, then hands off:

> LinkedIn has the current version of the working history.

No email address and no phone number, in any form. That includes a `mailto:` behind a button,
an obfuscated address, and a contact form. LinkedIn and GitHub are the only two links.

The page also doesn't announce that I'm looking for work. Linking `agentic-job-hunt` lets a
reader infer it from that repo's README, which is fine, and the page doesn't draw attention
to it either way.

Two things follow. The page needs no maintenance when a job changes, which is most of the
point. And my CV stops being a source for anything here: it's stale on current employment, and
everything it's good for is banned from this page anyway.

Full rules: [`../content/facts.md`](../content/facts.md) § 2 and § 6.

### 3. No citizenship, relocation or language-study story ✅

Too personal for a permanent public page.

**mova still gets its honest origin**, stated generically: it started from my own language
learning, and I wanted the record of every word and every mistake to stay in files I own. No
naming of the language, the exam, or the reason behind it. Wording is in
[`../content/projects.md`](../content/projects.md).

### 4. No custom domain ✅

`https://batirko.github.io` is the URL. Revisit only if the page ever outgrows it.

### 5. Projects come before the bio ✅ superseded decision, 2026-08-21

`design-brief.md` said the page opens with who I am. It doesn't. The order is: a short intro
that is the masthead, then the four projects, then the bio, then the two links.

The reason is length and attention. A reader with two minutes wants proof the work is real
before they want a biography. The brief's order was written during the scaffold and wasn't a
considered call.

### 6. Direction: dark-first, grotesk, lime ✅ 2026-08-21

Picked from five candidate directions, each a typeface and a palette together, because the
face carries more of the feel than the colour does. Four earlier candidates in an editorial
register were rejected as too official.

- **Type.** IBM Plex Sans for the name, titles and prose. IBM Plex Mono for every label, spec
  value, caption and the colophon. Two families, both self-hosted from `fonts/`, 72 KB total.
- **Colour.** Charcoal-blue paper at OKLCH 19%, acid lime accent at hue 130. Designed dark and
  adapted to light.
- **The known cost.** Lime can't hold its contrast on a light ground. Light mode runs the
  accent at OKLCH 48%, which reads olive rather than lime. That was accepted knowingly. There
  is no brighter green available at that lightness; the gamut runs out.

### 7. Nothing moves, and the one animation asks first ✅ 2026-08-21

No scroll animation, no entrance, no hover motion. writtten's loop is a real animated GIF, and
it loads as a still frame with a button that plays it. A page arguing that people should stay
in charge of AI-assisted work shouldn't start moving without being asked.

That button is the only script on the page: fifteen lines, inline, no dependency. Without
JavaScript the still frame shows and no dead control appears.

### 9. The screenshots are links ✅ 2026-08-21

Readers reach for a screenshot expecting it to open the thing it shows, so it does. Each of
the three figures wraps its image in a link to the same place the identity column already
points: Agentic Workspaces and writtten to their live sites, mova to its repo.

Nothing new was written for it. The image keeps its description as its alt text, which is also
what a screen reader announces for the link, so the change adds no copy and needs no
`content/` entry. On hover and on focus the hairline border takes the accent; the picture
itself doesn't move, so decision 7 still holds. Page height is unchanged at 4,581px.

### 10. whatatake goes third, with a screenshot ✅ 2026-09-30

Vitalii asked for it straight after writtten. That puts the three live products together at the
top, each one a click away. The copy and its sources are in
[`../content/projects.md`](../content/projects.md) § 6.

The card follows every rule the others do. Its paragraph is 273 characters, and its figure is
a real take's page on the live site, linked to the site's front page.

**It costs 0.9 of a screen.** The page grew from 4,580px to 5,380px on a 1280×900 desktop, so
from 5.1 screens to 6.0. The card's text and spec take 423px of that, and the figure 377px.
Without the figure the page would be 5.6 screens. Vitalii's target is 2 to 5 screens, and six
projects in the current row layout can't meet it either way. The next lever is a layout change,
not shorter copy.

The repo is private and has no licence, so the card carries **Live** and no **Source**, like
Agentic Workspaces. Its Repo row says `Private.` and promises nothing more.

writtten's figure now carries two controls: the image opens the site, and the button below it
plays the loop. The button sits outside the link, so neither one catches the other's click.

### 11. research-and-learn goes fourth, with a screenshot ✅ 2026-10-05

Vitalii asked for the repo to be added. Placement was left open, so it sits after the three live
products and ahead of mova: it's the newest public repo, and like Agentic Workspaces and mova it
is a workspace you clone and work inside. Moving it is a one-block cut and paste. Copy and
sources are in [`../content/projects.md`](../content/projects.md) § 7.

The card follows every rule the others do. Its paragraph is 305 characters. Its figure is the
top 720px of the repo's own topic-page screenshot, and the caption says the guide behind it is a
demo with an invented case. The image links to the repo, because there's no live site.

**It costs 0.9 of a screen, and the page is now 6.9.** The page grew from 5,380px to 6,178px on
a 1280×900 desktop, measured with every image loaded. The card takes 798px. Decision 10 already
said the row layout can't reach Vitalii's 2 to 5 screens at six projects, and seven makes it
worse. The next lever is still a layout change, not shorter copy.

## Standing rules

- **The words live in `content/`.** A design change never rewrites them and never adds new
  ones. New copy is written into `content/` first, then used.
- **No employers, no titles, no dates, no email, no phone.** Decision 2 above, enforced by
  `content/facts.md` § 2 and § 6. This is the rule most likely to be broken by a design pass
  reaching for a credibility signal.
- **[`content/facts.md`](../content/facts.md) outranks everything**, including this plan and
  anything a design pass wants for the sake of a layout.
- **No build step, no dependencies.** If either becomes necessary, that's a conversation, not
  a commit.
- **When a project's README changes materially, the card here goes stale.** Re-read the README
  and update `content/projects.md` before touching the page.
- **When the Agentic Workspaces repo goes public**, that card changes twice:
  its `Repo` row becomes `Public · MIT`, and it gains a `Source` link beside `Live`. Until
  then the private repo is the reason that card has one link where the others have two.
- **If the whatatake repo opens**, add a `Source` link beside `Live` and put its licence in
  the `Repo` row. It has no licence file today.
- **If the take in the whatatake figure is ever taken down**, recapture the figure from another
  take with a verdict. `content/projects.md` § The whatatake figure says why the take has to be
  a neutral one.
- **Never put the index's own counts on this page.** They are read from a crawl and move every
  time it runs. `content/projects.md` § 5 explains it.
