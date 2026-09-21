---
title: Pattern and seed
description:
  Giving a hand a control to choose among a family of variations, deliberate
  rather than accidental, instead of one fixed result
week: 8
date: 2027-04-12
teachers:
  - rowan-achebe
spec:
  - given the same seed, your instrument produces the same result twice in a row
  - a hand has a control (a key, a slider, a tap) that moves to a different seed and gets a visibly different, equally deliberate result
---

## Before the studio

Bring an instrument that behaves identically every time it runs. Today it
learns to vary on purpose, and gives a hand a way to choose the variation.

## In the studio

Wire a seeded random source into one part of the instrument --- where the next
mark starts, how a constraint bends, what a decayed state regenerates into ---
and give a hand a control that moves between seeds, not just a viewer who can
read the number off a corner of the screen. The discipline here is narrow:
"random" and "unpredictable to me right now" are not the same thing, and an
instrument that can't reproduce its own output on request is much harder to
debug, let alone exhibit. Two runs with the same seed should be identical down
to the pixel; that's the test, not a vibe check. But the point isn't
reproducibility for its own sake --- it's that choosing a new seed should feel
like choosing a different mark, not spinning a wheel of pure noise.

## Afterwards

Hand your instrument to someone and let them move through three seeds without
touching anything else. Ask which one they'd pick to show, and why. If they
can't tell the seeds apart, the variation isn't visible yet; if none of them
feels like a choice worth making, the seed reached everywhere it needed to but
the marks don't diverge in any way a hand would care about.
