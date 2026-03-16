# Codex Bootstrap — Build World Seed Mapper

You are Codex working in this repository.

## Your job
Build **World Seed Mapper**, a web app for creating world maps in 2D and previewing them wrapped onto a 3D globe.

The product you are building is:
- a focused worldbuilding web app
- centered on a 2D equirectangular world editor
- capable of editing terrain/height information, painted map features, and labels
- capable of previewing the same map texture on a rotatable 3D globe
- intentionally scoped to an MVP first, not a full cartography suite

## Core product principles
- Do **not** rebuild the project from scratch once implementation begins unless a prompt explicitly requires it.
- Keep the architecture clean, modular, and easy to extend.
- Favor simplicity and clear separation of concerns over over-engineering.
- Build the smallest complete version of each feature before adding polish.
- Preserve working functionality while extending the app.

## Technical direction
- Framework: Next.js
- Language: TypeScript
- Styling: Tailwind CSS
- 2D editing: canvas-based editor (preferred: Konva or Fabric.js)
- 3D globe: Three.js via React Three Fiber or equivalent clean integration
- Projection assumption: **equirectangular** map from day one

## MVP scope
The MVP should support:
- a flat 2D world map canvas
- a grayscale heightmap editing workflow
- a color paint layer for terrain/water/features
- a basic label layer
- local project save/load
- a live or refreshable 3D globe preview using the flat map as a globe texture

## Non-goals for now
Do not spend time on these unless a prompt explicitly asks for them:
- auth/accounts
- cloud save
- collaboration
- advanced erosion simulation
- tectonic simulation
- procedural civilizations
- marketplace features
- payments
- multiplayer
- full GIS-level projection tooling

## Process (repeat until done)
1) Open and read `/prompts/STATUS.md`.
2) Find the FIRST prompt in the Queue that is not checked `[ ]`.
3) Open that prompt file.
4) Implement it completely.
5) Keep changes aligned with the architecture and constraints in `STATUS.md`.
6) Update `/prompts/STATUS.md`:
   - mark completed prompt(s) as `[x]`
   - add concise implementation notes
   - add any new known issues or follow-up tasks
7) Commit only coherent, working progress.

## Implementation standards
- Use App Router if starting fresh in modern Next.js.
- Use TypeScript throughout.
- Keep components small and purpose-specific.
- Keep editor state organized and ready for later undo/redo.
- Prefer explicit types over loose `any`.
- Avoid hidden coupling between the 2D editor and 3D preview.
- Keep map/project data serializable.
- Where possible, design data structures so future layers/tools can be added without major rewrites.

## UX standards
- The app should feel visually interesting, modern, and purpose-built.
- Avoid flat generic admin-dashboard vibes.
- The editor should prioritize clarity:
  - visible active tool
  - visible active layer
  - obvious map/globe preview area
  - obvious save/load actions
- MVP polish matters, but feature completeness matters first.

## Important map rules
- The map is an equirectangular world texture.
- Horizontal wrap should be treated as a world seam where left/right edges connect.
- Top and bottom of the map represent poles.
- Design decisions should preserve the ability to wrap the map onto a sphere cleanly.

## Output expectations
When a prompt is complete:
- the app should still run
- new code should be integrated, not isolated junk files
- any temporary shortcuts should be documented in `STATUS.md`
- any follow-up needs should be noted clearly
```

---
