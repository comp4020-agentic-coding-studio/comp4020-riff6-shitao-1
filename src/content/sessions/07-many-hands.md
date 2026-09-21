---
title: Many hands
description:
  Folding mouse, touch and keyboard into one path through the code, instead of
  a separate branch for each
week: 7
date: 2027-04-05
teachers:
  - rowan-achebe
spec:
  - at least two distinct input devices (of mouse, touch, keyboard, pen) drive the same instrument through one shared code path
  - you can point at the branch in the code where the two devices would diverge, and show that it doesn't exist
related:
  - lectures/week-07
---

## Before the studio

Bring your instrument built against whichever input device you happened to
prototype on. For most people that's a mouse, sometimes touch. Today it has to
answer to a second one.

## In the studio

Add a keyboard path, or a touch path if you built for mouse, and route it
through the exact function that already drives your existing input --- not a
parallel `if (isTouch)` branch that quietly reimplements the same behaviour
twice. The test that matters isn't "does touch also draw a line," it's "does
the constraint from week 4 and the decay from week 5 still hold when the input
comes from somewhere else." If they don't, the bug is almost always that
those features were built against one device's assumptions rather than
against the shared signal underneath it.

## Afterwards

Get someone in the room to drive your instrument with the device you didn't
build it for first. Watch, don't help.
