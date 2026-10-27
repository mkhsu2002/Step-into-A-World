# Step-in-A-World

> Turn any story canon into a walkable 3D world.

Step-in-A-World is a new engine that turns a story world's canon data into a
first-person, walkable 3D world. Give it a canon package — domain geography, a
species bestiary, journey routes, field logs — and it generates a world you can walk
into, where agent-driven creatures live by habitat rules and yesterday's expedition
changes today's world.

A new project built for **ASUS UGen AI League 2026** — Creator AI theme ×
Thunderstorm battlefield × Online track. Proposed in Stage I, developed and showcased
through Stage II on the organizer-provided VM and SDV environment.

## Demo World 01: K's Hunting Log

The first world Step-in-A-World brings to life: NeoBabylon ZERO's hunting log —
14 domains, weekly expedition journeys, a species bestiary, and field logs. Walk the
Cloud-Ladder mining corridor (FK-W013): from the cableway frame, past copper-vein
rock lichen terraces, foldwing katydid grass belts, crystal-back alpaca slopes,
thunder-tether condor wind windows, to the mist-crest jaguar's forbidden stone steps
— where the log's own choice, stopping at the boundary line and turning back,
becomes something you do, not just something you read.

## How it works

1. **Canon package in** — domain geography, species bestiary, journey routes, field
   logs, world state. Format-neutral: any story can fill the same package.
2. **World model** — terrain, habitats, species, routes, and state, all referenced to
   canon sources.
3. **3D scene generation** — terrain, vegetation, species appearance, light and fog,
   generated from canon data.
4. **Agent-driven ecology** — creatures act on habitat conditions; outcomes write back
   to world state instead of being one-off spectacles.
5. **Verification gates** — canon, asset, routing, and language checks before anything
   goes live. Expansions are labeled EXPANSION and must fit habitat, ecology chains,
   and existing canon. The engine never rewrites the author's main story.
6. **Persistent state** — yesterday's expedition changes today's world. Tracks remain,
   routes open or close, and the next expedition starts from the updated state.

One pipeline, any canon: swap the canon package and a different world comes out.

## Repository layout

- `docs/PRD.md` — product requirements (Chinese).
- `engine/` — engine code (planned).
- `examples/` — demo canon packages (planned; Demo 01: K's Hunting Log).
