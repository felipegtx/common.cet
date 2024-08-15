# Wall Start Drag Animation Documentation

## Overview

This document describes the behavior, logic, and part numbering system of the Wall Start Drag Animation feature for the FIKA product line. This feature allows interior designers to drag and position wall elements within a space, with various alignment and snapping capabilities.

## Part Numbers

The part numbers for the FIKA product line follow a specific structure:

```
FIKA-[Product Type]-[Specifications]-[Dimensions]
```

### Product Types and Part Number Structure

| Product Type | Format | Example |
|--------------|--------|---------|
| Cabinets (CAB) | FIKA-CAB-[Type]-[WWDD] | FIKA-CAB-BBF-1518 |
| Bookcases (BOOK) | FIKA-BOOK[X]-[WWDD] | FIKA-BOOK3-2430 |
| Lateral Files (LAT) | FIKA-LAT[X]-[WWDD] | FIKA-LAT2-3624 |
| Overhead Storage | FIKA-OVERHEAD-[WWDD](-OPEN) | FIKA-OVERHEAD-3614-OPEN |
| Platforms (PF) | FIKA-PF-[WWDD] | FIKA-PF-3042 |
| Shelves (SHELF) | FIKA-SHELF-[WWDD] | FIKA-SHELF-3609 |
| Tables (TBL) | FIKA-TBL-[Type]-[Dimensions] | FIKA-TBL-FSRECT-3636 |
| Tiles (TILE) | FIKA-TILE-[WWDD] | FIKA-TILE-3030 |
| Towers (TOWER) | FIKA-TOWER-[Type]-[WWDD]-[L/R] | FIKA-TOWER-4BBF-1518-L |
| Workstations (WS) | FIKA-WS-[Type]-[Dimensions] | FIKA-WS-RECT-2448 |

Where:
- [X] represents the number of drawers or shelves
- [WW] is the width in inches
- [DD] is the depth in inches
- [L/R] indicates Left or Right orientation (for Towers)
- [Type] varies by product (e.g., BBF for Box/Box/File cabinets, RECT for rectangular workstations)

For specific product types, dimensions, and configurations, please refer to the product catalog or contact the product development team.

## Positioning and Rotation

When dragging a wall element:

1. The element's position is determined by the current mouse position.
2. The element maintains its original rotation.

## Wall Alignment and Snapping Behavior

The system attempts to align the wall element with existing wall surfaces and can snap to other objects in the space:

1. If alignment with a wall is possible, the element will align accordingly.
2. If alignment is not possible, the element will be positioned at the current mouse location.
3. Snapping to other objects follows these rules:
   - Snapping may be disabled under certain conditions.
   - If allowed, the system searches for suitable snap points.
   - If a snap is found, the element is positioned at the snap point.
   - If no snap is found, the element returns to its original position.
4. After snapping, the system:
   - Updates the position of all connected elements.
   - Aligns any other elements that were snapped during the animation.

## Movement Aid

A movement aid helper is available to assist with positioning:

- Deactivated when the element is snapped to another object.
- Activated when the element is not snapped, providing additional guidance.

## Updating the View

After each change in position or snapping:

1. The wall element's properties are updated if necessary.
2. The view is refreshed to show the new position.
3. The focus point is updated to keep the element in view.

## Interaction with Other Elements

When dragging a wall element:

1. Other elements in the space may be affected by the movement.
2. Connected elements move along with the dragged wall element.
3. The system continuously checks for potential conflicts or connections with other elements.

## Remarks and Disclaimers

- This documentation may not cover all possible scenarios or edge cases.
- For more detailed information about specific product rules, dimensions, or part numbers, please consult the product-specific documentation or contact the development team.