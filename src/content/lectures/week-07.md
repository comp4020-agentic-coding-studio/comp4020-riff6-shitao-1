---
title: One path for every hand
description:
  Unifying mouse, touch and keyboard isn't an accessibility add-on — it's
  what a correctly-built instrument does anyway
week: 7
date: 2027-04-05
teachers:
  - rowan-achebe
related:
  - sessions/07-many-hands
---

The tempting way to add a second input device is a branch: `if (isTouch) {
...touch logic... } else { ...mouse logic... }`. It works, briefly, and then
every feature added afterwards --- the constraint from week 4, the decay from
week 5 --- has to be built twice and kept in sync twice. The alternative is one
internal event, produced identically by every input source, that the rest of
the instrument never has to know the origin of. Once that unification exists,
a keyboard user and a touchscreen user aren't a special case you remembered to
handle; they're just two more ways of producing the one thing the instrument
actually listens for.

This is also the week accessibility stops being a separate checklist. An
instrument built around one shared internal event, rather than one device's
raw API, tends to already work for a keyboard-only user, because the keyboard
was never a bolted-on afterthought to begin with.

It also cashes the promise week 3 made and left open: once every device
funnels into the same event, some expressive qualities don't need an event at
all. A live voice count, how long a shared map has sat non-empty, what's
actually in it --- state every input path already writes to, readable
directly, with no per-device reasoning left to do.

## Outline

- the branch-per-device trap, and why it compounds with every later feature
- designing one internal event that every input source produces
- why this makes keyboard support a consequence, not a separate task
- reading expressive signals off shared state instead of any single event
