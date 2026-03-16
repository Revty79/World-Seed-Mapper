# 06 — Globe Preview

## Goal
Wrap the flat map onto a 3D globe preview.

## Requirements
- Add a globe preview panel using Three.js / React Three Fiber or equivalent.
- Use the flat map representation as a texture source for the sphere.
- Support at minimum:
  - rotate globe
  - zoom camera
- The globe should update from current map data, either live or via refresh action.
- Maintain clear separation between editor logic and globe rendering logic.

## Deliverables
- Working globe preview
- Texture pipeline from flat map to sphere
- Clean preview panel/component structure

## Notes
- It is acceptable for labels to be baked visually into the preview or omitted initially.
- Accuracy and clean wrapping matter more than visual complexity.