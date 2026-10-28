# Step-into-A-World

> Turn a static site into a live, observable world.

Step-into-A-World is a new tool framework that turns a static website — pages and
pre-generated images — into a virtual world you can observe in real time. Instead of
pre-rendering every view, the framework generates a new video on every observation,
right on edge hardware — creatures appropriate to the domain appear at random, weather
and time keep changing — so no two visits ever see the same video.

A new project built for **ASUS UGen AI League 2026** — Creator AI theme ×
Lightning battlefield × Online track. Proposed in Stage I, prototyped in Stage II on
the organizer-provided UGen300 (Hailo-10H) edge device.

## First site brought to life: K's Hunting Log

Today, NeoBabylon ZERO's hunting log is a static site of pre-generated images. It is
the framework's first demonstration ground — and its journey page is the Stage I
initial simulation. With the framework, the same Cloud-Ladder mining corridor (FK-W013)
stops being one fixed video everyone replays: every visit generates a new video —
domain-appropriate creatures appear at random, weather and time change — and the
mist-crest jaguar's forbidden stone steps mean something again — stop at the boundary
line and turn back, because the world says so, not because the picture says so.

The K site itself is not the submitted work. The framework is.

Initial simulation (Stage I): https://k-hunting-log.icareu.tw/journey/ — the current
static journey page. Stage II will spin its live observation off into a standalone URL.

## How it works

1. **Static site in** — pages, pre-generated images, and canon data: domain geography,
   species bestiary, journey routes, field logs, world state.
2. **World model** — parsed into terrain, habitats, species, routes, and state, every
   entry referenced to its source.
3. **Per-observation generation on edge hardware** — each visit generates a fresh video
   on UGen300 (Hailo-10H, 40 TOPS INT4, 8GB): domain-appropriate creatures appear at
   random, weather and time vary — not a replay of a pre-generated file.
4. **Live observation** — open the world in a browser and watch it happen. Open a
   location's field note. Boundary lines have real meaning.
5. **Persistent state** — yesterday's expedition changes today's world. Tracks remain,
   routes open or close, and the next observation starts from the updated state.
6. **Verification gates** — canon, asset, routing, and language checks before anything
   goes live. Expansions are labeled EXPANSION and must fit habitat, ecology chains,
   and existing canon. The framework never rewrites the author's main story.

One framework, any static site: apply it to another site and that site comes alive too.

## Stage plan

- **Stage I** — proposal + concept architecture + initial simulation (the K journey
  page, running on an ordinary laptop, as the rules allow).
- **Stage II** — prototype on the organizer-provided UGen300: hardware integration and
  performance verification of live world observation on edge hardware.

## Repository layout

- `docs/PRD.md` — product requirements (Chinese).
- `engine/` — framework code (planned).
- `examples/` — demo sites (planned; first site: K's Hunting Log).
