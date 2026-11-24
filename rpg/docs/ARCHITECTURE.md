# Architecture — proposal, engine-neutral

## Logical boundaries
- Application/session: lifecycle, pause, active scene and loading.
- World: regions, districts, interiors, access rights, persistent entity IDs.
- Simulation: authoritative clock, ordered events, off-screen NPC schedules, weather.
- Presentation: camera, input mapping, animation, audio and adaptive UI.
- Gameplay: tasks, dialogue, investigation, character progression, activities, relationships, economy.
- Persistence: versioned save snapshots, migrations, deterministic event restoration, future cloud adapter.
- Content: data registries, locale keys, versioned edition packages.

The rendered scene is a view of world state, not its sole source. Off-screen simulation should preserve causal continuity without rendering all residents. Engine implementation, exact schemas, memory budgets and tools require review and measurement.

## Invariants
Stable entity IDs; no duplicate NPCs or items across districts; time advances once per event; save/restore preserves state; optional content does not break shared progress; no secrets embedded in the client.

No executable project or runtime code is present.