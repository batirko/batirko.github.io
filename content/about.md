# About — source copy

> Canonical wording for everything the page says about me. The page may cut, never invent.
> Accuracy rules that govern this file live in [facts.md](facts.md). If a design pass needs
> a sentence that isn't here, write it here first, then use it.

## The rule that shapes all of this copy

**The page carries what doesn't change. LinkedIn carries what does.**

No employer names, no job titles tied to a company, no dates, no current-role claims. Those go
stale the moment anything moves, and a stale portfolio is worse than a thin one. The page says
what I work on and how I think about it, then points at LinkedIn for the working history.

This is a hard rule, not a preference. See [facts.md](facts.md) § 2.

## Name and title

Vitalii Batyr — Product Manager, developer platforms.

## One line (for a hero, a meta description, an og:title)

I build platforms for the people who build software, and side projects that keep humans in charge of AI-assisted work.

## Short bio (~55 words — hero or intro block)

I'm a product manager working on developer platforms. My work sits on the surfaces engineers
actually touch: internal developer portals, software catalogs, documentation, self-service
onboarding, and the AI features layered on top of them. Earlier, application security tooling
that plugs into source control and the editor.

## Long bio (~190 words — an about section)

I'm a product manager working on developer platforms. My work sits on the surfaces engineers
actually touch: internal developer portals, software catalogs, documentation, self-service
onboarding, and more recently the AI features layered on top of them. Earlier, application
security tooling that plugs into source control and the editor.

Nine years in product, most of it on tooling other engineers depend on. My strongest opinion
about internal platforms is that most of them are envisioned as products and end up as a pack
of services. Adoption is the test. If the paved road isn't genuinely faster than going around
it, people go around it.

I measure this kind of work by whether engineers come back to it on their own. Adoption and
friction numbers tell you that.

The projects on this page are side work, built in evenings. They circle one question I keep
hitting in my day job: when an agent does part of the job, what stops the person from quietly
losing the thread? Each project answers it differently, and each one is public so the answer
can be argued with.

## The line that hands off to LinkedIn

Needs to appear somewhere near the bio, in whatever voice the design settles on:

> LinkedIn has the current version of the working history.

## The through-line (proposed spine for the page — confirm or replace)

**Human judgment stays with the human; the system keeps the record.**

- **writtten** keeps the AI out of your prose and in the critic's seat.
- **vibecoding-starterpack** puts documentation under CI, so an agent can't drift away from it unnoticed.
- **agentic-job-hunt** records what actually happened after each application, so you can check whether your own scoring predicted anything.
- **mova** hands the learner an agent-run workspace where every word and every error stays in plain files they own.

This is a proposal, not a fact about me. If it feels too neat, the fallback spine is plainer:
four side projects, all built with coding agents, all about developer and knowledge-work
tooling.

## Focus areas, if the design wants a list

Developer platforms and internal developer portals · developer experience · AI in developer
workflows (RAG, MCP, agentic surfaces) · application security integrations · API strategy

## Reference facts — **not page copy**

Kept here so a session doesn't have to go digging, and so nobody mistakes a gap on the page
for a gap in the record. None of this goes on the page.

| Fact | Value |
| --- | --- |
| Years in product | 9 |
| Domains, in order of depth | developer platforms and IDP · developer experience · application security integrations · AI in developer workflows |
| Working history | LinkedIn |

**Education, languages and the working history in detail are deliberately not in this repo.**
This repo is public, and [facts.md](facts.md) § 6 keeps that material off the page. The same
reasoning keeps it out of the files sitting next to the page. I hold it privately; ask me if a
session genuinely needs it.

My CV is also not a source for anything here. It is stale on current employment, and everything
it is good for — employers, titles, dates, metrics — is banned from this page by
[facts.md](facts.md) § 2 anyway.

## Contact

No direct contact details on the page. No email, no phone. Someone who wants to reach me goes
through LinkedIn, which is also where the current history lives.

| Channel | Value | On the page? |
| --- | --- | --- |
| LinkedIn | https://linkedin.com/in/vitaliibatyr | Yes. The primary link. |
| GitHub | https://github.com/batirko | Yes. |
| Email | — | **No.** |
| Phone | — | **No.** |

A design that wants a contact section builds it from those two links. No `mailto:`, no contact
form, no email capture.

## Section labels and colophon — added for the design pass 2026-08-21

Written here before use, per `CLAUDE.md`.

### Section labels

Three, all plain. The masthead carries the name and the one-line, so the top of the page needs
no label of its own.

- **Projects**
- **About** — the bio, which now sits after the projects rather than before them.
- **Elsewhere** — the two links out. Not "Contact", not "Get in touch". See [facts.md](facts.md) § 6.

### Colophon

Closes the page. Everything in it is a fact about this page, checkable by reading the repo.

> Set in IBM Plex Sans and IBM Plex Mono, both served from this repo. Hand-written HTML and
> CSS, no build step, no dependencies, no analytics, and nothing to consent to. Built with a
> coding agent, like everything else here.

No year, and no date of any kind. Rule 2 of [facts.md](facts.md) bans dates, and a dated
colophon is one more thing that goes stale.

### One approved edit to the long bio

The page now runs projects first and the bio after them, so the long bio's last paragraph says
**"The projects above"** rather than "The projects on this page". Same claim, correct pointer.
Nothing else in the bio changes.
