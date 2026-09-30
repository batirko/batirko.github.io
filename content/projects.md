# Projects — source copy

> Four projects, in the order I'd put them on the page. Every claim here was read out of the
> project's own README or its GitHub metadata on 2026-08-21. Accuracy rules: [facts.md](facts.md).
>
> **Ordering rationale, settled 2026-08-21:** Agentic Workspaces first, then writtten, mova,
> vibecoding-starterpack, agentic-job-hunt. The first two both open in one click, which is what
> the first slot is for. Agentic Workspaces leads because it is the newest and the only one of
> the five that is itself a website.
>
> **Updated 2026-09-30:** whatatake goes third, straight after writtten, on Vitalii's call. That
> keeps the three live products together at the top, each one a click away.
>
> The numbered headings below are in the order they were researched, not page order.

---

## 1. writtten

**Live:** https://writtten.com · **Repo:** https://github.com/batirko/writtten
**Licence:** Apache-2.0 · **Public**

### One line

You write every word. The AI never touches your prose, it reads alongside you and points out what you missed.

### Card copy (~45 words)

Most AI writing tools generate text for you to edit. writtten does the opposite. A live feed
of observations runs beside your document as you revise, flagging contradictions, unclear
passages, unsupported claims and missing topics. There is no "Apply suggestion" button, and
there never will be.

### Longer copy (~110 words, if a section gets more room)

It has become very easy to hand your thinking to an AI: you ask, it writes, you accept. In
knowledge work the thinking is the job, and the document is just what it leaves behind, so
that habit erodes the judgment that made you good at it. writtten keeps you in the writing
seat and puts the AI in the critic's seat.

Observations come from a fixed list, not open-ended chatter: contradictions, unclear meaning,
unsupported claims, undefined jargon, missing topics, structure and flow, strategic tensions.
It stays quiet while you draft and speaks up once the text settles, which is when scrutiny
helps instead of interrupting.

### The detail worth showing

Hover a flagged passage and both sides of a contradiction light up at once. One section
commits to a Q2 launch, another to Q3. writtten notices; you decide what to do about it.

### Stack

React · TypeScript · TipTap / ProseMirror · local-first PWA, IndexedDB · bring-your-own-key
(Gemini, OpenAI, Anthropic), called straight from the browser

### Status (say it plainly, don't dress it up)

Early and actively developed. The core loop works. It's open-sourced to get the idea
scrutinised and to find collaborators.

### Asset available

`~/Projects/writtten/docs/launch/hero-loop.gif` — a real product loop, 960px wide. Also served
from the repo on GitHub. Best single visual on this page.

---

## 2. mova

**Repo:** https://github.com/batirko/mova · **GitHub template** · **Public**

### One line

A language-learning workspace run by your AI coding agent, in plain files you own.

### Card copy (~45 words)

You pick the language and the goal. The agent interviews you, builds a curriculum and a study
plan, then teaches, drills, and tracks every word and every error you get wrong. Chat is the
only thing you operate. Everything it records stays on your machine.

### Longer copy (~110 words)

*mova* (мова) is Ukrainian for "language". You copy the template, open it in a coding agent,
and say "set up my workspace". A few minutes of questions and the agent builds your profile,
curriculum and plan on its own.

Three words carry an ordinary week. **lesson** is the full session: everything due, then new
material, a graded check, then practice aimed at exactly what the check missed. **drill** is
short practice with no new material. **review** is the weekly replan. Seven more verbs cover
writing practice, mock exams, tutor sessions and pulling in template updates.

The hub, the deck and the profile page are read, never typed into.

### Why it exists (state this — it's the honest origin)

It started from my own language learning. I wanted the drilling to adapt to the errors I
actually make, and I wanted the record of every word and every mistake to stay in files I own
rather than inside somebody's app.

Say it at roughly that length. Don't name the language, the exam, or the reason behind it.

### The detail worth showing

Session length is a budget you agree, not a promise the tool makes. You say how long you have;
the set gets sized to fit, and cut before it's offered if it doesn't.

### Stack

Node ≥20 and git · plain markdown and HTML you can open from disk · agent-agnostic (Claude
Code, opencode, Codex, Antigravity) · self-contained offline pages, no CDN, no external fonts

### Status

Works end to end. Seven languages start straight away; any other language adds about half an
hour while the agent builds a grammar pack first.

### Asset available

`~/Projects/mova/docs/assets/hub.png` — the workspace hub. Screenshots come from a real
generated workspace with an invented learner.

---

## 3. vibecoding-starterpack

**Repo:** https://github.com/batirko/vibecoding-starterpack · **GitHub template** · **MIT** · **Public**

### One line

A repo scaffold that makes documentation fail CI when it drifts.

### Card copy (~45 words)

Give a coding agent a task and it does the task. It won't remember last week's decision, and
neither will the next agent. Documentation is the shared memory, and documentation rots. This
template puts the docs under CI, so breaking a convention turns the build red.

### Longer copy (~110 words)

A convention is worthless until something fails when you break it. So two small Vitest files
test the documentation rather than the code. If the plan and the project files disagree about
status, if a roadmap item is missing its routing metadata, if a load-bearing link got
flattened into plain text, `npm test` goes red the same way a type error does.

The rest is three more conventions, each paired with the concrete failure that motivated it:
a plan file that doubles as an agent routing table, a split between docs that describe intent
and docs that describe what's actually built, and rules for keeping parallel agent sessions
out of each other's way.

### The detail worth showing

The war story about the WYSIWYG editor that silently ate the markdown links inside table cells
and left the contract blind, with everything still looking fine. Three layers of defence,
because the failure is invisible until a test names it.

### Stack

TypeScript · Vitest · GitHub Actions · no runtime, it's a scaffold

### Status

Usable now. Fill three files, run `npm install && npm test`.

### Note

This is the template the portfolio repo itself borrows its shape from, in a much lighter form.
Worth saying on the page if there's room for a wink.

---

## 4. agentic-job-hunt

**Repo:** https://github.com/batirko/agentic-job-hunt · **Public**

### One line

An opinionated job search pipeline that runs inside Claude Code, calibrated against its own results.

### Card copy (~45 words)

It scans job boards, screens the results by title at no token cost, evaluates the survivors
against your actual background, writes tailored CVs and cover letters, tracks every
application, and then tells you whether the scores you assigned beforehand predicted anything
at all.

### Longer copy (~110 words)

Scanning and triage never call a model, so the expensive step only runs on roles that survived
two free filters.

The part that matters most is outcomes. A tracker status collapses "rejected after the CV
screen" and "rejected after four rounds" into the same symbol. Recording them separately is
what lets the analysis tell you whether a score you assigned before applying predicted
anything. On the search this was built from, the answer was mostly no, and finding that out
changed the strategy more than any feature did.

Forked from career-ops and rebuilt across roughly 350 applications and 270 evaluations.

### The detail worth showing

The honest finding: the scores didn't predict much. A tool that reports its own method as
weak is doing the job.

### Stack

Node 18+ · Claude Code · Playwright · optional Go dashboard · Greenhouse, Ashby, Lever,
Comeet, Workable and public LinkedIn

### Status

In daily use. It's the pipeline behind my own search.

### Note on framing

The repo is public and the page links it, so a reader can infer an active job search from its
README. Decided 2026-08-21: that's acceptable, and the page doesn't draw attention to it. Lead
this card on the calibration idea, which is the interesting part, and let the search be
background.

---

## 5. Agentic Workspaces

**Site:** https://agentic-workspaces.com · **Repo:** not public
**Licence:** MIT

> Added 2026-08-21. Every claim below was read out of that repo's `README.md`, `docs/concept.md`,
> `docs/plan.md`, `site/README.md` and `package.json` on 2026-08-21.
>
> **Two facts here are not yet true and the page must not claim them until they are.** The repo
> is private, and the site is not published. See **Status, and what blocks it** below.

### One line

A front door for agentic workspaces: the repos you clone and work inside, findable by the job
you need one for.

### Card copy — what a workspace is (~55 words)

An agentic workspace is a repo you clone to live in rather than to run. You open a coding agent
inside it and it arrives equipped: commands to run, instructions to follow, folders to file
into. Then it accumulates, both what it learns about your work and the work itself. Your copy
diverges from the original permanently, and that is the point.

Sources: `README.md` opening paragraph, and the site's own hero copy in `site/dist/index.html`
("Clone one, open your agent inside, and it arrives equipped").

**One deliberate departure from the source wording.** `docs/concept.md` in that repo says a repo
you clone "not to *run* but to *live in*". That is the "Not X, but Y" construction, which
[facts.md](facts.md) § 5 bans outright on this page. Rewritten to "clone to live in rather than
to run", which says the same thing. Don't restore the original phrasing here.

### The detail worth showing — what the site does (~60 words)

Skills and plugins have marketplaces. These repos have none, so people find them by accident:
a fork graph, a thread, a link in someone's post. The index is the front door. You arrive with
a job, a job hunt or a dissertation or a campaign or a second brain, and you browse the
workspaces other people have already shaped around it.

Sources: `README.md` ("Skills and plugins have marketplaces. These repos have none. This is the
index."), `docs/concept.md` § The problem, and the eleven subjects the live site lists, which
include Job hunt, Second brain, Research & science, Content & marketing and Teaching & study.

### The method, deliberately not the lead

Earlier drafts opened on the four inclusion rules, the refusal to order by stars, and the
published error rate. Vitalii cut that on 2026-08-21: the page should say what a workspace is
and what the site is for, not how the corpus is built.

One trace of it survives, in the **Status** row, because it tells a reader why the list is
worth trusting: every entry is found by a crawler rather than added by hand. The rest stays
here as reference.

- Four inclusion rules, and exactly four. If a fifth were ever needed to keep them coherent,
  the project stops and publishes that finding instead of adding one.
- No sort by stars anywhere. Across the star range, popular and unpopular repos qualify at
  rates you cannot tell apart.
- The index publishes its own error rate, and prints nothing rather than a stale figure.

### Why it exists

A new kind of repo appeared: one you fork not to run but to live in. Skills and plugins have
marketplaces and these have none, so people find them by accident. The harder problem sat
underneath, and it was a number: nobody knew how many existed, not within an order of magnitude.

The governing rule of the project is **evidence before infrastructure**. The research phase was
allowed to end in "no", and the index was only built because the count came back large enough
to justify it.

### Stack

TypeScript · Node &ge;20 · Vitest · a static generator over one JSON file, no framework and no
client-side fetching · GitHub Actions

### The link back to another project on this page

It was stood up from `vibecoding-starterpack`. Worth a line if the design has room, and it is
true: the docs contract, the plan-as-routing-table and the CI-tested documentation all came
from that template.

### Status, and the one link it carries

Settled 2026-08-21. **The site goes public; the repo stays private.** So this is the one card on
the page with a **Live** link and no **Source**.

Status line:

> Live and actively developed. Every entry is found by a crawler rather than added by hand.

Third spec row, which answers the question the missing Source link raises:

> **Repo** — Private while it's being built.

That line stays true until the repo opens. When it opens, swap the row to `Public · MIT` and add
the Source link.

**One check before this page is published:** open https://agentic-workspaces.com and confirm it
resolves. Nothing else on the page depends on a host that went up the same day.

### On the counts

The index reports its own size, and the numbers move every time the crawler runs. As read on
2026-08-21: 1,280 indexed, 868 originals, 412 copies of another entry, 499 listed, 11 subjects.

**These do not belong on the portfolio page.** They are true today and stale next week, and a
portfolio that quotes a live counter is a portfolio that goes quietly wrong. The interesting
claim is the method, not the size. If a number is ever wanted here, "over a thousand repos" is
the durable form, since the crawler only adds.

### Asset available

`site/dist/index.html` in that repo builds the real front page, so a screenshot is a genuine
product capture rather than a mockup. It shows live counts, so caption it as the index rather
than as a fixed figure.

---

## 6. whatatake

**Live:** https://whatatake.com · **Repo:** https://github.com/batirko/whatatake, private, no
licence file

> Added 2026-09-30. Every claim below was read on 2026-09-30 out of that repo's `CLAUDE.md`
> (§ Status and § Hard invariants), `docs/concept.md`, `docs/architecture.md` and
> `package.json`, out of `gh repo view batirko/whatatake`, and off the live site's home page
> and its How it works page at https://whatatake.com/about.
>
> **Don't source from that repo's `README.md`.** It still describes Phase 0, before any app
> existed, and it promises a calibration journal the product has since hidden.

### One line

Takes about the future, kept on the record: who said it, when, and how it aged.

Source: the site's own lead sentence, on its home page and its How it works page: "whatatake
keeps takes about the future on the record: who said it, when, and how it aged."

### Card paragraph

The paragraph itself sits with the others under **The card paragraph** below. Each of its
sentences comes from one of these:

- "You write down what someone says will happen: your own take, a friend's or someone
  public's." How it works, § What this is.
- "Write it however you'd say it, or paste a link. We draft the details for you to check."
  How it works, § Logging a take. The concept doc says the same: AI drafts a take from what you
  write, and you check the draft before logging it.
- "Its words can't be edited after that." How it works, § What this is.
- "When the date arrives, we remind you to record what happened." How it works, § The verdict.
- **No model decides the verdict** is hard invariant 3 in that repo: AI proposes, humans
  resolve, and a verdict is never finalised without a person. Today no AI touches a verdict at
  all; verdict research waits until after that project's Phase 3.

### Why it belongs on this page

The About section says every project circles one question: when an agent does part of the
job, what stops the person from losing the thread? whatatake's answer is the verdict. AI drafts
the take, and a person always decides how it aged. That's why the card ends on the verdict.

### The detail worth showing

A take's page after its verdict. The post it quotes is kept as it was logged, so the take
survives the post being deleted, and the verdict is added with its own date.

### Stack

Next.js · TypeScript · Supabase Postgres · Drizzle · Gemini for the drafts · Vercel ·
notifications by email through Resend, or by a Telegram bot

### Status

> Live, early and actively developed. It's free to use, and no money moves through it.

"Early" is the honest word. That repo records that its public-surface phase closed short of
its traffic goal. The second sentence is the site's own, from How it works § Whose project
this is.

### Repo row

> **Repo** — Private.

That's all that's true today. Unlike Agentic Workspaces, nothing says this repo will open, so
the row makes no promise. If it opens, add a **Source** link and put its licence in the row.

### What not to say

- **"It's the record, not the bet."** That repo's governing principle, and a "Not X, but Y"
  construction, which [facts.md](facts.md) § 5 bans on this page.
- **Calibration, Brier scores or a track record.** The concept doc still lists them, but the
  product hid calibration on 2026-09-13.
- **Stakes, groups or a group-chat bot.** Stakes and groups exist, but they aren't the lead.
  The group-chat surface isn't built.
- **Any count** of takes, users or answers. They move daily.

---

## The card paragraph — one per project, 180 to 350 characters

> Settled 2026-08-21. Each card on the page carries **one** description paragraph, not two.
> Every clause below is cut or condensed from the sections above; nothing new is claimed. The
> character count is the constraint Vitalii set, and it is measured, not estimated.

| Project | Characters |
| --- | ---: |
| Agentic Workspaces | 276 |
| writtten | 295 |
| whatatake | 273 |
| mova | 259 |
| vibecoding-starterpack | 265 |
| agentic-job-hunt | 287 |

### Agentic Workspaces

An agentic workspace is a repo you clone to live in rather than to run: your agent arrives
equipped, and your work accumulates inside. These repos have no marketplace, so people find them
by accident. The index is the front door, and you browse it by the job you need one for.

### writtten

Most AI writing tools generate text for you to edit. writtten does the opposite. A live feed of
observations runs beside your document as you revise, flagging contradictions, unclear passages,
unsupported claims and missing topics. There is no “Apply suggestion” button, and there never
will be.

### whatatake

You log what someone says will happen: your own take, a friend’s or someone public’s. AI drafts
the details from a sentence or a link, and you check them. Once logged, the words can’t be
edited. When the date arrives, you record what happened. No model decides the verdict.

### mova

You pick the language and the goal. The agent interviews you, builds a curriculum, then teaches,
drills and tracks every word and every error you get wrong. It started from my own language
learning: I wanted the record of every mistake to stay in files I own.

### vibecoding-starterpack

Give a coding agent a task and it does the task. It won’t remember last week’s decision, and
neither will the next agent. Documentation is the shared memory, and documentation rots. This
template puts the docs under CI, so breaking a convention turns the build red.

### agentic-job-hunt

It scans job boards, screens by title at no token cost, evaluates the survivors against your
actual background, writes tailored CVs, and tracks every application. Then it tells you whether
the scores you assigned beforehand predicted anything. On the search it was built from, mostly
no.

**What each one dropped, and why it is safe.**

- **Agentic Workspaces** — loses that your copy diverges from the original permanently. The
  strongest single idea, but the paragraph already has to carry both the category and the site.
- **writtten** — nothing. The card copy above was already in range, so it is used verbatim.
- **whatatake** — written straight to the range on 2026-09-30, so nothing was cut. It leaves
  out the quoted post surviving deletion, which the figure caption carries instead.
- **mova** — loses "chat is the only thing you operate" and "everything it records stays on
  your machine". The deck already says *in plain files you own*, which covers the second.
- **vibecoding-starterpack** — nothing. Used verbatim.
- **agentic-job-hunt** — loses cover letters from the list of what it writes, and compresses
  the outcome finding to its last four words.

The second paragraph each card used to carry is still in the sections above. If a card ever
needs more room, that is where the text comes from.


---

## Cross-project facts, for a stats bar or a footer line

Only true numbers. Do not round up, do not add any that aren't here.

| Fact | Value | Checked |
| --- | --- | --- |
| Public repos on the page | 4 | 2026-08-21 |
| Live products | 3 (writtten.com, agentic-workspaces.com, whatatake.com) | 2026-09-30 |
| GitHub templates | 2 (mova, vibecoding-starterpack) | 2026-08-21 |
| Stars | 1 across all four | 2026-08-21 |

**Stars are why there is no social-proof bar on this page.** One star is one star. A
stat-led macrostructure needs real numbers, and these aren't the ones. Pick a structure
that doesn't ask for them.

---

## Figure captions and link labels — added for the design pass 2026-08-21

Written here before use, per `CLAUDE.md`. Every claim below is read off the image itself or
out of a section above.

### Link labels

Two labels, used on every card so a reader learns them once. Both are short enough to stay on
one line at 320px.

| Label | Points at |
| --- | --- |
| **Live** | The running product. Only writtten has one. |
| **Source** | The public repo. |

### The writtten figure

Image: `assets/writtten-loop-still.png`, a still frame from `assets/writtten-loop.gif`. Both
are the real product loop from `~/Projects/writtten/docs/launch/`.

Caption:

> The Timeline section commits to a public launch in Q2. Success metrics commits to Q3.
> writtten flags both passages at once and leaves the decision to the writer.

Checked against the frame: both passages carry the amber highlight, and the open observation
card reads "contradiction". Matches **The detail worth showing** above.

The loop doesn't play on its own. A button starts it, labelled **Play the loop**, and reads
**Stop the loop** while it runs. The still is what loads with the page.

### The Agentic Workspaces figure

Image: `assets/agentic-workspaces.png`, the real front page, captured from a local build of
`site/dist/index.html` in that repo. Not a mockup.

Caption:

> The front page. Each card is one workspace, tagged with the job it was built for. Every count
> is read from the crawl, so they move each time it runs.

Both sentences do a job. The first says what a reader is looking at, which is the point of the
whole card. The second stops anyone reading the live counters as fixed figures, and it is true:
`site/build.ts` derives every one of them from the classified data.

This card carries **Live** and no **Source**, per the section above.

### The mova figure

Image: `assets/mova-hub.png`, resized from `~/Projects/mova/docs/assets/hub.png`.

Caption:

> The workspace hub: days to exam, units done, items due, and what to do next. Every number is
> read from the file that owns it. This one is a generated demo with an invented learner.

The last sentence is not optional. The screenshot names a language and an exam, and the page
must not let a reader take either as mine. Decision 3 in `docs/plan.md` is the rule; the
invented learner is recorded under **Asset available** above.

### The whatatake figure

Image: `assets/whatatake-take.png`, a take's page on the live site at
https://whatatake.com/c/px4nwx7yfry3, captured in light mode on 2026-09-30. Not a mockup.

Caption:

> A take's page after its verdict. The post it quotes is kept as it was logged, and the verdict
> is added with its own date.

Checked against the frame: the quoted post sits under the take with its author and date, the
take reads "Was due 14 Sept 2026", and the verdict box reads "Happened" beside "Resolved 28 Sept
2026".

**Why this take.** Most public takes on the live site are political, from named people. A
portfolio that carries my name shouldn't show a reader one of those and let them guess why I
picked it. This one is about markets, and it already has a verdict, which is the part the card
ends on. The page labels it "Someone else's take", logged by the whatatake account, so it needs
no disclaimer.

The image links to https://whatatake.com, like the identity column, and not to the take. If the
take is ever taken down, the link still works.
