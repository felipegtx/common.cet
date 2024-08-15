Here's the consolidated document combining the information from both sources:

# FIKA Office Material Legend Controller Documentation

## Overview

This document describes the functionality of the FIKA Office Material Legend Controller, which is responsible for managing material legends in the FIKA Office product line. The controller handles the creation, updating, and management of material legends, which are used to display information about materials used in office designs.

## Part Number Structure

FIKA Office products use a standardized part numbering system. Understanding this system is crucial for interior designers working with the product line. The part numbers are structured as follows:

| Prefix | Product Type | Variant | Dimensions |
|--------|--------------|---------|------------|
| FIKA-  | 2-4 letters  | 1-3 characters | 2-8 digits |

### Prefix
All FIKA Office products start with the prefix "FIKA-".

### Product Type
This section identifies the type of product. Common types include:
- WS: Workstation
- CAB: Cabinet
- TBL: Table
- BOOK: Bookcase
- LAT: Lateral File
- OVERHEAD: Overhead Storage
- PF: Panel Fabric
- TILE: Tile
- J: Junction

### Variant
This section provides additional information about the product variant. It can include:
- Numbers (e.g., 2, 3, 4, 5 for BOOK types)
- Letters (e.g., BBF, FF for CAB types)
- Combinations (e.g., 4BBF, 5FF for TOWER types)

### Dimensions
This section specifies the product dimensions, typically in inches. The format can vary:
- Two sets of two-digit numbers (e.g., 2424, 3036)
- Three sets of two-digit numbers (e.g., 363618, 424230)
- Single two-digit number for some products (e.g., 30 for round tables)

## Examples of Valid Part Numbers

1. Workstations:
   - `FIKA-WS-RECT-2430`: Rectangular workstation, 24" x 30"
   - `FIKA-WS-ARC-3660`: Arc-shaped workstation, 36" x 60"

2. Cabinets:
   - `FIKA-CAB-BBF-1524`: Box/Box/File cabinet, 15" x 24"
   - `FIKA-CAB-FF-1830`: File/File cabinet, 18" x 30"

3. Tables:
   - `FIKA-TBL-FSRECT-4242`: Free-standing rectangular table, 42" x 42"
   - `FIKA-TBL-FSROUND-36`: Free-standing round table, 36" diameter

4. Bookcases:
   - `FIKA-BOOK3-3024`: 3-shelf bookcase, 30" x 24"
   - `FIKA-BOOK5-4230`: 5-shelf bookcase, 42" x 30"

5. Lateral Files:
   - `FIKA-LAT2-3624`: 2-drawer lateral file, 36" x 24"
   - `FIKA-LAT4-4218`: 4-drawer lateral file, 42" x 18"

6. Overhead Storage:
   - `FIKA-OVERHEAD-4214`: Overhead storage, 42" x 14"
   - `FIKA-OVERHEAD-6014-OPEN`: Open overhead storage, 60" x 14"

7. Panel Fabric:
   - `FIKA-PF-3042`: Panel fabric, 30" x 42"
   - `FIKA-PF-6066`: Panel fabric, 60" x 66"

8. Tiles:
   - `FIKA-TILE-2418`: Tile, 24" x 18"
   - `FIKA-TILE-4860`: Tile, 48" x 60"

9. Junctions:
   - `FIKA-J-30-L`: L-shaped junction, 30" high
   - `FIKA-J-42-T`: T-shaped junction, 42" high

## Material Legend Functionality

### Creation and Type
The controller creates a specialized type of material legend called FODataMaterialLegend, specifically designed for FIKA Office products.

### Adding Materials to the Legend
Materials used in a design can be added to the legend through the following process:
1. The system checks if adding materials is allowed.
2. If allowed, the material is temporarily stored with information for creating a legend item.
3. The legend can be immediately updated with the new material if requested.

### Updating the Material Legend
The legend can be updated:
1. Immediately after adding a new material (if specified).
2. At specific points during the design process (e.g., before fetching parts or after finalizing the design).

The update process involves:
1. Retrieving the current material legend for the design.
2. Adding all temporarily stored materials to the legend.
3. Clearing the temporary storage of materials.

### Design Process Integration
The controller integrates with the design process through two main hooks:
1. Pre-Fetch Parts Hook: Clears temporarily stored materials before fetching parts.
2. Post-Finalize Hook: Updates legends for legend parts and cleans up if no legend parts exist.

### Accessing the Material Legend
The material legend can be accessed at any time during the design process, with automatic creation if it doesn't exist.

## Important Notes

- The system works with multiple designs simultaneously, maintaining separate material legends for each.
- Safeguards prevent adding materials to the legend when inappropriate.
- The system is optimized to update the legend only when necessary.

## Remarks and Disclaimers

- This documentation provides an overview of the FIKA Office part numbering system and material legend functionality. Always refer to the most up-to-date product catalog for the complete list of available products and their specific part numbers.
- Some product lines may have additional variants or special configurations not covered in this general overview.
- When specifying products, ensure that all dimensions and variants are compatible with the overall design and other selected components.
- The exact visual representation and formatting of the material legend may be defined in other parts of the system.