# 01 — Editor Layout and Layer Model

## Goal
Create the initial editor state model and wire the UI shell to that model.

## Requirements
- Define a basic serializable project structure.
- Define an initial layer model that includes:
  - heightmap layer
  - surface paint layer
  - labels layer
- Define editor UI state for:
  - active tool
  - active layer
  - brush size placeholder
  - selected label placeholder
- Build UI panels that reflect this state.
- The center area should render a map canvas placeholder with visible dimensions and grid/guide support if helpful.

## Deliverables
- Types/interfaces for project and layer state
- Simple editor state wiring
- Layer panel showing available layers
- Tool panel showing placeholder tools
- Inspector reflecting active selections

## Notes
- Keep state simple and local if appropriate.
- Zustand is acceptable if used cleanly, but not required.