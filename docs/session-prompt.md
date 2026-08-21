# Kickoff prompt for the design session

Paste this into a fresh session opened in `~/Projects/vitalii-batyr`. It gives context and
pointers. It deliberately doesn't prescribe a layout, because picking the layout is the work.

---

We're building my personal portfolio page. One page, static, served from GitHub Pages. Four
public side projects and a short bio about me.

The repo is already scaffolded. Everything the page may say is written and verified in
`content/`, and the reasoning is in `docs/`. Start by reading `CLAUDE.md`, then
`docs/concept.md`, `docs/design-brief.md`, and all three files in `content/` before you touch
anything.

**What I need from this session:** the design and build of the page. The copy is done and
isn't yours to rewrite. The structure, the type, the colour, the rhythm and the interaction
are all open, and that's the point.

Use Hallmark for it. It's installed as a skill. `docs/design-brief.md` explains which verb to
run and why the placeholder `index.html` should be ignored rather than redesigned.

**What matters most:** this page has to look made rather than generated. Three of the four
projects on it argue that AI-assisted work should stay accountable to a human. A page that
reads as template output undercuts that argument before anyone finishes the first paragraph.

**Constraints that are genuinely fixed**, all detailed in the brief: no build step and no
dependencies, every path relative, both colour schemes defined, mobile verified from 320px,
and nothing on the page that isn't backed by `content/`.

**The constraint that will shape your design most:** the page names no employers, no job
titles and no dates, and carries no email or phone. The page carries what doesn't change and
LinkedIn carries what does. That takes away the scaffolding a portfolio layout normally leans
on — a logo row, a career timeline, a "currently at" line, a contact form. The four repos and
the writing carry it instead. Design for that rather than trying to route around it.

The four decisions that were open are settled and written up in `docs/plan.md`. The copy in
`content/` already reflects them, so read it as final.

Don't create the GitHub repo, push anything, or turn on Pages. I do that part.
