# FIKA Product Configuration Documentation

This document provides a comprehensive overview of the configuration options, part number logic, and rules for the FIKA product line in office furniture. The information is intended for Interior Designers who need to understand the logic behind product configuration without delving into programming details.

## Part Number Structure

FIKA product part numbers follow a consistent structure that encodes various attributes of the product. The general format is:

```
FIKA-[Product Type]-[Configuration]-[Dimensions]
```

Components:
1. **FIKA**: Common prefix for all products in this line.
2. **Product Type**: Indicates the category of the product.
3. **Configuration**: Specifies particular features or arrangements.
4. **Dimensions**: Represents the size of the product, usually in inches.

## Product Types and Their Part Numbers

### 1. Cabinets (CAB)

Configurations:
- BBF: Box/Box/File
- FF: File/File
- SBOOO: Open Shelf

Format: `FIKA-CAB-[Configuration]-[Width][Depth]`
Example: `FIKA-CAB-BBF-1518` (15" wide, 18" deep Box/Box/File cabinet)

| Configuration | Width Options | Depth Options |
|---------------|---------------|---------------|
| BBF, FF, SBOOO| 15, 18        | 18, 24, 30    |

### 2. Bookcases (BOOK)

Format: `FIKA-BOOK[Height]-[Width][Depth]`
Example: `FIKA-BOOK3-2430` (24" wide, 30" deep, 3-high bookcase)

| Height Options | Width Options | Depth Options |
|----------------|---------------|---------------|
| 2, 3, 4, 5     | 24, 30, 36, 42| 24, 30        |

### 3. Lateral Files (LAT)

Format: `FIKA-LAT[Height]-[Width][Depth]`
Example: `FIKA-LAT3-3618` (36" wide, 18" deep, 3-high lateral file)

| Height Options | Width Options | Depth Options |
|----------------|---------------|---------------|
| 1, 2, 3, 4, 5, 6 | 30, 36, 42  | 18, 24        |

### 4. Workstations (WS)

Format: `FIKA-WS-[Type]-[Width][Depth]`
Example: `FIKA-WS-RECT-2448` (24" deep, 48" wide rectangular workstation)

| Type Options | Width Options | Depth Options |
|--------------|---------------|---------------|
| RECT, ARC    | 18-96 (in 6" increments) | 18-36 (in 6" increments) |

### 5. Tables (TBL)

Format: `FIKA-TBL-[Shape]-[Dimensions]`
Example: `FIKA-TBL-FSRECT-3636` (36" x 36" rectangular table)

| Shape Options | Size Options |
|---------------|--------------|
| FSRECT        | Various combinations from 36x36 to 84x42 |
| FSROUND       | Diameters: 30, 36, 42, 48, 54 |

## Additional Product Types

The FIKA line includes other product types such as overhead storage (OVERHEAD), pedestals (PF), tiles (TILE), and various supports and accessories. Each follows a similar logic in its part numbering system.

## Configuration Options

### Spread Options

1. None: Not spread or grouped
2. Individual: Standalone unit
3. Sideways: Side-by-side configuration
4. Group: Part of a group configuration
5. All: Covers all available options

### Panel Tile Material Types

1. Fabric
2. Laminate
3. Veneer
4. Markerboard
5. Glass

### Support Handedness

1. None: No specific handedness
2. Left-handed
3. Right-handed
4. Shared: For both left and right-handed configurations

## Remarks and Disclaimers

1. When configuring products, ensure that the chosen options align with the available part numbers.
2. Some product types may have additional configuration options not fully reflected in the part number (e.g., material choices for tiles).
3. For precise pricing and availability, always refer to the most current product catalog or consult with a sales representative.
4. Custom configurations may be available but would require special ordering and may not follow the standard part numbering system.
5. This documentation provides a general overview of the FIKA product line's part numbering system and configuration options. For specific product details or configuration rules, please refer to the detailed product catalogs or specification guides.
6. The actual implementation of how these options affect product configuration and pricing would be found in other parts of the system not provided here.