# World Seed Mapper — STATUS

## Product summary
World Seed Mapper is a web app for building a flat 2D world map and previewing that map as a wrapped 3D globe.

The initial product focuses on a clean MVP:
- 2D equirectangular world editor
- heightmap editing
- terrain/water/feature painting
- labels
- local save/load
- globe preview

## Current build intent
Build a strong MVP foundation first.
Do not expand into simulation-heavy or account-heavy features yet.

## Architecture direction
- Next.js
- TypeScript
- Tailwind CSS
- 2D canvas editor for map interaction
- separate 3D globe preview module
- serializable project model

## Project model (target direction)
A project should eventually contain:
- project metadata
- canvas dimensions
- heightmap layer data
- surface paint layer data
- label data
- view/editor settings

This model can begin simple and evolve.

## Editor model (target direction)
The editor should be structured around layers/tools, not one-off hacks.

Expected initial concepts:
- active tool
- active layer
- brush settings
- viewport state
- project state

## Map assumptions
- projection: equirectangular
- left/right edges wrap
- top/bottom are poles
- all future tool decisions should respect globe wrapping

## Constraints
- Keep the MVP small and working.
- Prefer simple implementations over ambitious incomplete systems.
- Avoid premature optimization.
- Avoid introducing backend complexity unless needed.
- Local save/load is enough for the MVP.

## Known non-goals for MVP
- accounts/auth
- cloud sync
- advanced erosion
- tectonic simulation
- multiplayer
- marketplace/export economy features

## Queue
- [ ] 00_foundation_scaffold.md
- [ ] 01_editor_layout_and_layer_model.md
- [ ] 02_heightmap_brush_tools.md
- [ ] 03_surface_paint_tools.md
- [ ] 04_label_tools.md
- [ ] 05_local_project_save_load.md
- [ ] 06_globe_preview.md
- [ ] 07_basic_undo_redo.md
- [ ] 08_seed_noise_generation.md
- [ ] 09_polish_and_usability_pass.md

## Implementation notes
- Nothing implemented yet.

## Known issues
- None yet.

## Follow-up backlog
- Export image pipeline
- Better label styling
- River/lake specialized tools
- Biome tools
- Seam-aware brush refinement
- Globe-specific overlays