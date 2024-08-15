# Straight Back Worksurface Documentation

This document describes the logic and behavior of a straight back worksurface product. This product is a type of support worksurface with specific characteristics and rules for configuration.

## Part Numbers

The part numbers for the straight back worksurface follow a specific format: `FIKA-WS-RECT-WWDD`, where:

- `FIKA`: The product line identifier
- `WS`: Indicates it's a worksurface
- `RECT`: Specifies that it's a rectangular shape
- `WW`: Width in inches (18 to 96, in 6-inch increments)
- `DD`: Depth in inches (18 to 96, in 6-inch increments)

Here's a table explaining the part number structure:

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| FIKA      | Product line | Fixed as "FIKA" |
| WS        | Worksurface indicator | Fixed as "WS" |
| RECT      | Shape indicator | Fixed as "RECT" for rectangular |
| WW        | Width in inches | 18, 24, 30, 36, 42, 48, 54, 60, 66, 72, 78, 84, 90, 96 |
| DD        | Depth in inches | 18, 24, 30, 36, 42, 48, 54, 60, 66, 72, 78, 84, 90, 96 |

Valid part numbers for this product include:

- FIKA-WS-RECT-1818
- FIKA-WS-RECT-2424
- FIKA-WS-RECT-3030
- FIKA-WS-RECT-3636
- FIKA-WS-RECT-4242
- FIKA-WS-RECT-4848
- FIKA-WS-RECT-5454
- FIKA-WS-RECT-6060
- FIKA-WS-RECT-6666
- FIKA-WS-RECT-7272
- FIKA-WS-RECT-7878
- FIKA-WS-RECT-8484
- FIKA-WS-RECT-9090
- FIKA-WS-RECT-9696

Note that not all combinations of width and depth are available. The actual available sizes may be limited based on manufacturing or design constraints.

## Dimensions and Properties

The straight back worksurface has two main dimensions:

1. Width: Represented by the property `cFOWidthPK`
2. Depth: Represented by the property `cFODepthPK`

### Valid Dimensions

- Width: The width can range from 18 inches to 96 inches, with increments of 6 inches.
- Depth: The depth can range from 18 inches to 96 inches, with increments of 6 inches.

## Shape and Edges

The worksurface has a rectangular shape with four distinct edges:

1. Back edge: Labeled as "b"
2. Front edge: Labeled as "f"
3. Left side: Labeled as "ls"
4. Right side: Labeled as "rs"

The front edge is distinguished from the other edges by having a thicker line type in visual representations.

## Connectivity and Interaction Rules

1. The worksurface can connect to other worksurfaces and base storage units.
2. When connecting to another worksurface or base storage unit along its front edge, special alignment rules apply to ensure proper positioning.
3. The worksurface can be adjusted to snap to the left or right side of another worksurface during placement, depending on the mouse position relative to the target worksurface's center.

## Stretching and Modification

- The width can be modified by stretching the left or right sides.
- The depth can be modified by stretching the front edge.
- When stretching the width, the back edge remains fixed.
- When stretching the depth, both left and right sides remain fixed.

## Grouping and Adjacent Surfaces

The worksurface can identify and group with other straight back worksurfaces that are adjacent to it. This grouping considers:

1. Surfaces to the left
2. Surfaces to the right
3. Surfaces in both directions

Adjacent surfaces are only grouped if they have the same rotation (yaw) as the current surface.

## Input Settings

The width and depth properties have specific input settings:

- Both are stretchable, insertable, and draggable.
- Both can be locked.
- Both have buttons for quick adjustments.
- Changes to these dimensions affect all connected components.

## Additional Notes

- The worksurface uses a standard edge type (FOStdEdge) for most edges, with a special edge type (FOBigEdge) for the front edge.
- The product supports automatic generation of supports, though the specific logic for this is not detailed in this class.
- The product can be part of a larger configuration system, interacting with other office furniture components.

## Remarks and Disclaimers

- The behavior of height adjustments, while supported, is not fully detailed in this documentation.
- Actual available sizes may be subject to manufacturing or design constraints not specified in this document.