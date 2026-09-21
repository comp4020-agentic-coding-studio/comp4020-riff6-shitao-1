---
title: Staging the work
description:
  Preparing an instrument to run unattended for a stranger, with none of the
  context you'd normally supply out loud
week: 11
date: 2027-05-03
teachers:
  - rowan-achebe
spec:
  - your instrument runs unattended for at least two minutes without crashing or needing an input you haven't documented
  - a first-time viewer can start using it with no spoken explanation from you
related:
  - lectures/week-11
---

## Before the studio

Bring the instrument you're planning to show in week 12, close to final. Today
is the last studio before it has to survive an audience without you standing
next to it.

## In the studio

Set it running and leave the room. Come back in two minutes and see what
state it's in --- most instruments that have only ever been demoed by their
author have at least one silent failure mode that only shows up unattended: a
memory leak from an event listener that never unregisters, a decay term that
eventually reaches a stuck state, a keyboard focus requirement nobody wrote
down. Fix what you find; that's the whole studio.

## Afterwards

Write the one sentence of instruction a viewer actually needs, if any, and put
it where they'll see it before they touch anything. Everything else you'd
normally say out loud has to be either obvious from using the thing, or cut.
