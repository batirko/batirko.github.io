# Concept — what this site is

## In one sentence

One page that shows four things I built and enough about me to know why I built them.

## Who reads it

In rough order of who actually lands here:

1. **A hiring manager or recruiter** who got my CV and typed my name into a search box. They
   have two minutes and one question: is this person's work real?
2. **Someone who found one of the repos** and clicked through to see what else there is.
3. **Me**, pasting the link into an application form's "portfolio" field.

All three want the same thing first: proof that something exists and works. Links to live
things and to real repos are the load-bearing content. The prose supports them.

## What it is not

- **Not a CV, and not an employment history.** The page names no employers, no titles and no
  dates. Those live on LinkedIn, which the page links. A second copy of a working history is
  a second thing to keep current, and it always loses.
- **Not a blog.** No posts, no feed, no newsletter capture. If that changes, it's a separate
  decision.
- **Not a case-study site.** Each project gets a card's worth of copy and a link. Anyone who
  wants depth reads the README, which is already long and already good.
- **Not a lead magnet.** No analytics, no cookie banner, no tracking, no email capture.
  Nothing to consent to.

## The bar it has to clear

The audience is engineers and the people who hire product managers for engineering tooling.
Both groups have seen a thousand generated portfolio pages. A page that looks generated
undercuts everything on it, particularly the argument that runs through all four projects.

So the design isn't decoration here, it's part of the claim. That's why Hallmark is the
method rather than a template. See [design-brief.md](design-brief.md).

## The rule that follows from all of that

**The page carries what doesn't change. LinkedIn carries what does.**

What I work on and how I think about it holds for years. Where I work does not. So the bio
describes focus and opinion, then hands off to LinkedIn for the current version.

The payoff is that the page needs no maintenance when a job changes, and it can never be
quietly wrong about where I am. The cost is that it carries less credibility on its own, which
the four repos are there to make up for.

There are also no direct contact details, in any form. LinkedIn and GitHub are the only two
links out. See [../content/facts.md](../content/facts.md) § 6.

## Success

I'm comfortable pasting the URL into an application form without adding a sentence of
explanation.

## Constraints that shape everything

- **Static.** GitHub Pages, no server, no build step, no dependencies to keep patched.
- **One page.** A second page is a decision to make later, not a default.
- **Handwritten HTML and CSS.** Small enough that a framework costs more than it gives.
- **Content is separate from design.** The words live in `content/`. A redesign never
  rewrites them, and never invents new ones. See [../content/facts.md](../content/facts.md).
