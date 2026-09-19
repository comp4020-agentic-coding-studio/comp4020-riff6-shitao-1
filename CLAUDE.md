# You are riffing on someone else's prototype

This repo is a copy of [`comp4020-ass2-shitao`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao) at
`765b3580` --- shitao's crit agent's shipped prototype for `06-a2-retro`.
The copy is yours; their repo is untouched and off limits.

**The brief is to take this somewhere it hasn't been.** Not to restart it, not
to polish it, and not to finish the agent's to-do list. Read how they directed
the agent, find the thing the prototype implies but doesn't do, and build
that. You have the session's half-hour, so pick something you can get live.

**Nothing here is marked.** No cutoff, no reflection, no `PROCESS.md` entry,
no crit sweep, no repo of your own on the line. That is the point --- the
interesting move is the one you wouldn't risk in your own graded repo.

**What you show at the share-back** is the live site plus
`git diff riff-start`. Push early and keep `main` green.

**The agent's own spec tests are `spec/course-brief.test.ts` and `spec/data-integrity.test.ts`.** They encode the crit brief,
not yours, and they gate the deploy --- a red check means no live site to show
at the share-back. If your riff moves past that brief, change them or delete
them; keep `spec/invariants.test.ts` green, since that one is true of any good
site.

Everything below this line was written for that crit submission. The marks,
the cutoff, the private-repo phase, the weekly `start` skill and the
reflection are all done, and none of it governs what you do here. Read it for
how they worked, not for what you owe.

---

# Working on SLOP1450

This is "Instruments for Mark-Making" — a fictional twelve-week course. Every
page has to hold the fiction: no real institution, no real course code, no
leaked real-world URLs. Read the brief and spec on the course website before
changing scope; don't restate them here.

## The actual failure mode on this repo

Every bug found so far has been a page that is individually valid — passes the
schema, builds clean, renders fine — but disagrees with a different page it's
supposed to agree with, or carries the wrong emphasis for a reader who isn't
cross-checking it. `pnpm check` cannot see this class of bug by construction:
nothing in it compares one page's claim against another's. The only thing that
has ever caught it is reading the whole site cold, and reading it with a
different question each time — a plain fact cross-reference, a hunt for
leftover template-author prose, a prospective-student read, a literal replay of
the brief's own marking walkthrough — has each caught something a prior framing
missed. Don't treat one clean pass as proof the site is clean; vary the framing
before concluding there's nothing left to find.

## Rendering gotchas specific to this template

- **Markdown emphasis only renders where content passes through the
  markdown/remark pipeline.** `SpecList` (rendering a `spec:` frontmatter
  array) and any raw prose written directly in a `.astro` template's body
  interpolate as plain text — `*for*` shows up as literal asterisks, `---`
  shows up as three literal dashes. Use a real "—" character in `.astro`
  template prose, and plain text with no markdown syntax in `spec:` arrays.
- Course code stays `SLOP1450` — only the leading digit is ours to change, and
  `spec/course-brief.test.ts` holds the assigned three digits fixed.

## What's deliberately not automated

Tone, emphasis, and whether a forward reference actually gets paid off later
are marker judgement calls, not schema checks — encoding them would just be
checking a paraphrase of the brief instead of the brief itself. `spec/` holds
only the facts a build can verify unattended: the course code, that published
assessment weights total 100, and that at least one lecture's deck actually
built.
