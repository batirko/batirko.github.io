# Design brief — for the Hallmark pass

> **The design pass has run. Read this as history, not as instructions.**
>
> This file was written during the scaffold, before anyone had looked at a design. Two of its
> calls were overturned once there was something to look at, and `docs/plan.md` decisions 5 to
> 7 are now the record:
>
> - **Order.** The page runs projects first, then the bio. This file says the opposite.
> - **Tone.** This file asks for something closer to a well-set README. The page went the
>   other way: a dark-first grotesk, not an editorial serif. Four candidate directions in the
>   editorial register were rejected as too official.
>
> What still holds, unchanged and outranking everything: the hard constraints in this file, and
> [`../content/facts.md`](../content/facts.md). Those are about what is true and what is
> private, not about taste.

Hallmark is installed at `~/.claude/skills/hallmark/`
(source: https://www.usehallmark.com/, `npx skills add nutlope/hallmark`).

## Which verb to run

Run the **default Design flow** from this brief. Do not run `hallmark redesign` against the
placeholder `index.html` in this repo.

The placeholder exists to prove the deploy works and to hold the content in a readable order.
It has no structure worth preserving, and feeding it to `redesign` anchors the result to a
layout nobody chose. Read the content, then design from the brief.

`hallmark study <url>` is fair game first if you want to pull DNA from a page I admire, but
only from a page I name. Don't go shopping.

## What Hallmark needs from this repo, and where it is

Hallmark won't invent copy. It's in the skill's own contract: *"Invent product copy. If the
user hasn't given you the words, ask."* The words are already written.

| It needs | Read |
| --- | --- |
| Every word the page may say | [`content/about.md`](../content/about.md), [`content/projects.md`](../content/projects.md) |
| What it must never say | [`content/facts.md`](../content/facts.md) |
| Audience, non-goals, the bar | [`concept.md`](concept.md) |
| Real images it may use | see **Assets** below |

## The brief

**Vitalii Batyr — a one-page portfolio.** A product manager who works on developer platforms,
showing four public side projects and a short bio. The audience is engineers and the people who
hire PMs for engineering tooling. The page has to look made rather than generated, because
three of the four projects argue that AI-assisted work should stay accountable to a human, and
a generated-looking page argues the opposite.

**One thing to absorb before you start.** This page names no employers, no job titles, no
dates, and carries no email or phone number. That's deliberate: the page carries what doesn't
change, LinkedIn carries what does. It removes the credibility scaffolding a portfolio layout
normally leans on — a logo row, a career timeline, a "currently at" line, a contact form. The
four repos and the writing have to carry it instead. Design for that rather than around it.

Tone: direct, technical, unsentimental. Confident without selling. Closer to a well-set
README than to a startup landing page.

## Hard constraints

1. **Static, no build step.** Hand-written HTML and CSS, served straight from the repo by
   GitHub Pages. No npm install, no bundler, no framework. If a dependency feels necessary,
   raise it instead of adding it.
2. **All paths relative.** The site serves at `https://batirko.github.io`. No leading `/` on
   any href or src, so the page also opens correctly straight from disk.
3. **Self-contained where it's cheap.** Self-host any font file rather than calling Google
   Fonts; a system stack is fine too. No CDN scripts, no analytics, no third-party requests.
   The page should render from disk.
4. **Light and dark.** `prefers-color-scheme`, both directions defined, `body` gets an explicit
   background. A visible toggle is optional.
5. **Mobile floor.** Hallmark's own non-negotiables apply: verified at 320, 375, 414 and
   768px, no horizontal scroll, no two-line clickable text.
6. **Tokens, not literals.** Colours and font families come from named `:root` custom
   properties. This is a Hallmark rule already; it also keeps a later re-theme to one block.
7. **No invented anything.** Numbers, testimonials, logo walls, star counts, "trusted by".
   Read [`content/facts.md`](../content/facts.md) first, in full.
8. **No employers, no titles, no dates, no contact details.** No company names anywhere, no
   career timeline, no "currently at", no `mailto:`, no contact form, no email in any
   obfuscated form, no phone. The only two outbound personal links are LinkedIn and GitHub.
   `content/facts.md` § 2 and § 6 are the full rule and they outrank any layout.
9. **Accessible by default.** Real landmarks, one `h1`, visible focus states, contrast that
   passes in both themes.

## Structure — decided, and deliberately open

**Decided:** the page opens with who I am, then the four projects, then the two links out.
Nothing else competes for the top.

The closing section is two links, LinkedIn and GitHub. It is not a contact section and should
not be built as one. No form, no address, no "get in touch" button that opens a mail client.

**Open, and yours to pick:** the macrostructure. Hallmark's job is to pick one that fits the
brief rather than defaulting to hero → three cards → CTA. Some that plausibly fit this
content, without prejudice: **catalogue**, **index-first**, **long-document**, **specimen**,
**portfolio-grid**. Rule them in or out from the content, not from this list.

**Ruled out: stat-led.** It needs real numbers to carry the page and there aren't any. The
only true cross-project number is one GitHub star.

**Also ruled out: anything built around a timeline, a logo row, or a "currently at" line.**
Constraint 8. A macrostructure that wants a career spine is the wrong pick here.

## Assets — real, and already on disk

Both are genuine product screenshots. Copy them into this repo rather than hotlinking.

| File | What it shows |
| --- | --- |
| `~/Projects/writtten/docs/launch/hero-loop.gif` | writtten's core loop, 960px. A contradiction between two sections lights up on both sides at once. The strongest single visual available. |
| `~/Projects/mova/docs/assets/hub.png` | mova's workspace hub: days to exam, units done, items due, what to do next. |

If the design uses them, wrap them in a `<figure>` with a real caption. Hallmark forbids
re-drawn browser chrome and fake window frames; these images don't need any.

Nothing for vibecoding-starterpack or agentic-job-hunt. Both are terminal-and-markdown
projects. Set their type well rather than inventing a picture for them.

## Before you hand it back

Run Hallmark's own pre-emit self-critique and stamp the six scores in the stylesheet, as the
skill requires. Then check the page against [`content/facts.md`](../content/facts.md) line by
line. A design that reads beautifully and claims something untrue is a failed pass.
