Here's the consolidated document combining the information from both sources:

# FIKA Office Wall Start Insert Animation

## Overview

This document describes the logic and behavior of the Wall Start Insert Animation for FIKA Office products. This animation is used when placing a product against a wall in an office environment.

## Part Number Logic

FIKA Office products use a standardized part numbering system. The part numbers are structured to provide information about the product type, dimensions, and other characteristics. Here's a breakdown of the part number structure:

| Component | Description | Example Values |
|-----------|-------------|----------------|
| Prefix    | Always "FIKA-" | FIKA- |
| Product Type | Indicates the type of product | WS (Workstation), CAB (Cabinet), BOOK (Bookcase), LAT (Lateral File), etc. |
| Variant | Specific variant or configuration | RECT (Rectangle), ARC (Arc), BBF (Box/Box/File), FF (File/File), etc. |
| Dimensions | Width and depth in inches | 3036 (30" wide, 36" deep) |
| Additional Info | Optional, varies by product type | L (Left), R (Right), OPEN, etc. |

### Example Part Numbers

1. Workstation: `FIKA-WS-RECT-3036`
2. Cabinet: `FIKA-CAB-BBF-1524`
3. Lateral File: `FIKA-LAT3-3624`

## Valid Product Types for Wall Start Insert Animation

The following product types are compatible with the Wall Start Insert Animation:

1. Workstations (WS)
2. Cabinets (CAB)
3. Bookcases (BOOK)
4. Lateral Files (LAT)
5. Overhead Storage (OVERHEAD)
6. Towers (TOWER)

For a complete list of valid part numbers, please refer to the product catalog or database.

## Alignment Behavior

When inserting a product near a wall, the system attempts to align it with the wall surface. This alignment process considers the current position of the mouse cursor and the selected product.

- The system continuously checks if the product can be aligned with a nearby wall surface.
- If alignment is possible, the product will snap to the wall.
- If alignment is not possible, the product will follow the standard insertion behavior.

## Interaction with Walls

The product being inserted interacts with walls in the following ways:

1. It attempts to detect nearby wall surfaces.
2. When a suitable wall is detected, the product tries to align itself with that wall.
3. The alignment considers the orientation and position of the wall.

## Mouse Interaction

The position of the mouse cursor plays a crucial role in the insertion process:

- The system constantly monitors the mouse position.
- The current mouse position is used to determine if wall alignment is possible.
- If the mouse is moved away from a wall, the product may detach from the wall alignment.

## Standard Insertion Behavior

If the product cannot be aligned with a wall, it will revert to the standard insertion behavior:

- The product will follow the mouse cursor freely.
- It can be placed anywhere in the office space without snapping to any surface.

## Remarks and Disclaimers

- The exact dimensions for each product are encoded in their respective part numbers.
- Specific rules for interaction with other products may vary depending on the product type and should be referenced in the individual product documentation.
- While this document provides an overview of the part numbering system, always refer to the most up-to-date product catalog for the complete list of valid part numbers and their specifications.

For more detailed information about specific product dimensions, part numbers, and interaction rules, please refer to the documentation of individual product classes or consult the FIKA Office product catalog.