# FIKA Office Tile Documentation

This document describes the logic and functionality of the FIKA Office Tile component, which is a part of a panel system used in office furniture configurations.

## Tile Types and Materials

The FIKA Office Tile can be made of various materials, each with its own characteristics:

1. Fabric
2. Laminate
3. Veneer
4. Markerboard
5. Glass

The tile's material type determines its properties and appearance in the office panel system.

## Tile Dimensions

The tile's dimensions are defined by:

- Width (W): Determined by the panel it's attached to
- Height (H): Can be customized, represented in inches

## Part Number Structure

The part number for a FIKA Office Tile follows this structure:

```
FIKA-TILE-[Width in inches][Height in inches]
```

For example, a tile that is 24 inches wide and 18 inches high would have a part number like:

```
FIKA-TILE-2418
```

Here's a table explaining the structure of the part number:

| Component | Description | Example |
|-----------|-------------|---------|
| FIKA      | Product line identifier | FIKA |
| TILE      | Component type | TILE |
| Width     | Width in inches (24, 30, 36, 42, 48, 54, 60) | 24 |
| Height    | Height in inches (06, 12, 18, 24, 30, 36, 42, 48, 54, 60) | 18 |

Valid part numbers for FIKA Office Tiles include:

FIKA-TILE-2406, FIKA-TILE-2412, FIKA-TILE-2418, FIKA-TILE-2424, FIKA-TILE-2430, FIKA-TILE-2436, FIKA-TILE-2442, FIKA-TILE-2448, FIKA-TILE-2454, FIKA-TILE-2460, FIKA-TILE-3006, FIKA-TILE-3012, FIKA-TILE-3018, FIKA-TILE-3024, FIKA-TILE-3030, FIKA-TILE-3036, FIKA-TILE-3042, FIKA-TILE-3048, FIKA-TILE-3054, FIKA-TILE-3060, FIKA-TILE-3606, FIKA-TILE-3612, FIKA-TILE-3618, FIKA-TILE-3624, FIKA-TILE-3630, FIKA-TILE-3636, FIKA-TILE-3642, FIKA-TILE-3648, FIKA-TILE-3654, FIKA-TILE-3660, FIKA-TILE-4206, FIKA-TILE-4212, FIKA-TILE-4218, FIKA-TILE-4224, FIKA-TILE-4230, FIKA-TILE-4236, FIKA-TILE-4242, FIKA-TILE-4248, FIKA-TILE-4254, FIKA-TILE-4260, FIKA-TILE-4806, FIKA-TILE-4812, FIKA-TILE-4818, FIKA-TILE-4824, FIKA-TILE-4830, FIKA-TILE-4836, FIKA-TILE-4842, FIKA-TILE-4848, FIKA-TILE-4854, FIKA-TILE-4860, FIKA-TILE-5406, FIKA-TILE-5412, FIKA-TILE-5418, FIKA-TILE-5424, FIKA-TILE-5430, FIKA-TILE-5436, FIKA-TILE-5442, FIKA-TILE-5448, FIKA-TILE-5454, FIKA-TILE-5460, FIKA-TILE-6006, FIKA-TILE-6012, FIKA-TILE-6018, FIKA-TILE-6024, FIKA-TILE-6030, FIKA-TILE-6036, FIKA-TILE-6042, FIKA-TILE-6048, FIKA-TILE-6054, FIKA-TILE-6060

## Material Selection Logic

The tile's material is determined through a hierarchical selection process:

1. The main material type is checked first (Fabric, Laminate, Veneer, Markerboard, or Glass).
2. For Fabric and Laminate, there are subtypes:
   - Fabric: PG1 or PG2 (likely representing different price or quality groups)
   - Laminate: LPL (Low Pressure Laminate) or HPL (High Pressure Laminate)
3. Based on these selections, a specific material code is assigned to the tile.

## Visibility and Selection

- The tile has a visible height, which can be different from its actual height.
- When selected in the configuration tool, the tile is highlighted with a green outline for easy identification.

## Elevation View

In elevation views (2D representations of the panel):

- The tile displays a text label representing its material.
- The tile's height is shown in the format "H:[height in inches]".

## Parts and Assembly

- The tile is considered a part of a larger panel assembly.
- When generating parts lists, the tile is included with its specific part number and quantity.

## Material Legends

The system supports custom material legends, which can assign specific identifiers or codes to materials for easier reference in documentation or ordering processes.

## Interaction with Panels

- The tile is designed to fit within a panel frame.
- Its width is determined by the panel it's attached to.
- Changes to the tile (such as material selection) can trigger updates to the parent panel, ensuring the overall configuration remains consistent.

## 3D Representation

In 3D views:

- The tile is represented with its correct dimensions and material appearance.
- It includes a slight bevel or frame effect around the edges for a more realistic look.
- The material applied in the 3D view corresponds to the selected material type and finish.

This documentation provides an overview of the FIKA Office Tile's functionality and configuration options. It's designed to help interior designers understand how the tile component works within the larger panel system, without delving into technical programming details.