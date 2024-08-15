# Straight Back Worksurface Documentation

This document describes the functionality, behavior, and part number structure of a straight back worksurface in the FIKA office furniture configuration system.

## Overview

The straight back worksurface is a rectangular support surface with a straight back edge, designed to connect with other furniture pieces. It is part of the FIKA product line.

## Part Number Structure

The part number for a straight back worksurface follows this format:

```
FIKA-WS-RECT-WWDD
```

Where:
- FIKA: Product line identifier
- WS: Worksurface indicator
- RECT: Rectangular shape indicator
- WW: Width in inches (18 to 96)
- DD: Depth in inches (18 to 96)

### Part Number Breakdown

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| FIKA      | Product line | FIKA |
| WS        | Worksurface | WS |
| RECT      | Shape       | RECT |
| WW        | Width       | 18, 24, 30, 36, 42, 48, 54, 60, 66, 72, 78, 84, 90, 96 |
| DD        | Depth       | 18, 24, 30, 36, 42, 48, 54, 60, 66, 72, 78, 84, 90, 96 |

## Valid Part Numbers

Based on the provided list, here are examples of valid part numbers for straight back worksurfaces:

```
FIKA-WS-RECT-1818, FIKA-WS-RECT-2436, FIKA-WS-RECT-3060, FIKA-WS-RECT-4872, FIKA-WS-RECT-6096
```

## Dimensions

1. Width: 18" to 96", in 6" increments
2. Depth: 18" to 96", in 6" increments

The part number directly encodes these dimensions. For example, FIKA-WS-RECT-3060 represents a worksurface that is 30" wide and 60" deep.

## Edges and Connections

The worksurface has four edges:

1. Back edge (b): Straight edge at the rear
2. Front edge (f): Opposite to the back edge, typically thicker
3. Left side edge (ls): Left edge when facing from the front
4. Right side edge (rs): Right edge when facing from the front

Each edge can connect to other furniture pieces, with the front edge having special alignment properties when connecting to other worksurfaces or storage units.

## Behavior and Interactions

1. **Stretching**: Can be stretched from sides or front. When stretched from the sides, the back edge remains fixed. When stretched from the front, both side edges remain fixed.
2. **Snapping**: Snaps into place near other furniture pieces, with sophisticated behavior when connecting to other worksurfaces.
3. **Adjacent Worksurfaces**: System identifies adjacent straight back worksurfaces to the left or right, allowing for continuous work surfaces.
4. **Height Adjustment**: Adjustable height (details not specified in this class)
5. **Support Components**: Can have support components added (e.g., legs)

## User Interaction

Users can modify the worksurface through:

1. Stretching: Drag edges to resize
2. Direct Input: Enter width and depth directly
3. Buttons: Adjust width and depth

The system ensures all changes are within allowed ranges and snapped to valid values.

## Remarks

1. The part number system allows for easy identification of worksurface dimensions.
2. The available sizes cover a wide range of office layout needs.
3. The modular nature of the part numbers facilitates inventory management and ordering.
4. Users should refer to the part number to quickly understand the worksurface size without needing to measure.
5. The specific materials and edge types (besides the thicker front edge) are not defined in this documentation and may be handled by related systems.

This documentation provides a comprehensive overview of the straight back worksurface's functionality, part number structure, and configuration logic. It should assist interior designers in understanding, specifying, and configuring the correct worksurface for their projects.