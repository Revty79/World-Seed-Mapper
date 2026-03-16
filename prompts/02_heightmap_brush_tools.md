# 02 — Heightmap Brush Tools

## Goal
Implement the first real editing workflow: grayscale heightmap painting.

## Requirements
- Add a working editable heightmap canvas/layer.
- Support at minimum these tools/actions:
  - raise terrain
  - lower terrain
  - smooth terrain (simple approximation is acceptable)
- Add brush controls for:
  - size
  - strength
- Height data should be visible to the user, ideally as grayscale.
- The data model must remain serializable for later save/load.

## Deliverables
- Functional heightmap editing interaction
- Brush UI controls
- Live visible change to terrain values
- Cleanly separated heightmap logic from general app shell

## Notes
- MVP implementation can use a 2D array, ImageData, or another pragmatic structure.
- Do not overbuild simulation logic.
- Keep future globe preview compatibility in mind.