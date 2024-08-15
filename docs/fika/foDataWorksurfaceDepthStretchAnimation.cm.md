# FIKA Product Line Documentation

## Overview

This document provides comprehensive information about the FIKA product line, including the part numbering system and configuration logic for various products. It is designed to assist Interior Designers in effectively configuring and ordering products without requiring programming knowledge.

## Part Number Structure

FIKA part numbers follow a consistent structure that encodes important information about each product. The general format is:

```
FIKA-[Product Type]-[Specifications]
```

Each part of the number has a specific meaning:

1. **FIKA**: The brand identifier, always present at the beginning of every part number.
2. **Product Type**: Indicates the category of the product (e.g., CAB for cabinet, WS for workstation).
3. **Specifications**: Varies based on the product type, often including dimensions and features.

## Product Categories and Their Part Numbers

### Cabinets (CAB)

Format: `FIKA-CAB-[Type]-[Width][Depth]`

| Component | Possible Values | Description |
|-----------|-----------------|-------------|
| Type | BBF, FF, SBOOO | Cabinet type (e.g., BBF for Box/Box/File) |
| Width | 15, 18 | Width in inches |
| Depth | 18, 24, 30 | Depth in inches |

Example: `FIKA-CAB-BBF-1524` represents a Box/Box/File cabinet that is 15" wide and 24" deep.

### Workstations (WS)

Format: `FIKA-WS-[Shape]-[Width][Depth]`

| Component | Possible Values | Description |
|-----------|-----------------|-------------|
| Shape | RECT, ARC | Workstation shape |
| Width | 18 to 96 | Width in inches |
| Depth | 18 to 96 | Depth in inches |

Example: `FIKA-WS-RECT-3060` represents a rectangular workstation that is 30" wide and 60" deep.

### Bookshelves (BOOK)

Format: `FIKA-BOOK[Height]-[Width][Depth]`

| Component | Possible Values | Description |
|-----------|-----------------|-------------|
| Height | 2, 3, 4, 5 | Number of shelves |
| Width | 24, 30, 36, 42 | Width in inches |
| Depth | 24, 30 | Depth in inches |

Example: `FIKA-BOOK3-3024` represents a bookshelf with 3 shelves, 30" wide and 24" deep.

### Lateral Files (LAT)

Format: `FIKA-LAT[Height]-[Width][Depth]`

| Component | Possible Values | Description |
|-----------|-----------------|-------------|
| Height | 1, 15, 2, 3, 4, 5, 6 | Number of drawers (1.5 for one and a half) |
| Width | 30, 36, 42 | Width in inches |
| Depth | 18, 24 | Depth in inches |

Example: `FIKA-LAT3-3618` represents a lateral file with 3 drawers, 36" wide and 18" deep.

### Tables (TBL)

Format: `FIKA-TBL-[Shape]-[Width][Depth]`

| Component | Possible Values | Description |
|-----------|-----------------|-------------|
| Shape | FSRECT, FSROUND | Table shape (Free Standing Rectangle or Round) |
| Width | 36 to 84 | Width in inches (for rectangular tables) |
| Depth | 36, 42 | Depth in inches (for rectangular tables) |
| Diameter | 30, 36, 42, 48, 54 | Diameter in inches (for round tables) |

Example: `FIKA-TBL-FSRECT-7242` represents a free-standing rectangular table that is 72" wide and 42" deep.

### Additional Product Categories

The FIKA product line also includes other categories such as:

- Overheads (OVERHEAD)
- Panels (PF)
- Shelves (SHELF)
- Tiles (TILE)
- Towers (TOWER)

Each of these categories follows a similar logical structure in their part numbers, encoding relevant dimensions and features.

## Worksurface Configuration Logic

### Group Depth Stretch Functionality

The FIKA product line includes a feature for managing the depth stretching of worksurfaces in a group. This allows multiple connected worksurfaces to be stretched together, maintaining a consistent depth across the group.

#### Enabling Group Depth Stretch

The group depth stretch feature can be toggled on or off. When enabled, it allows multiple connected worksurfaces to be stretched together in depth.

#### Affected Worksurfaces

When the group depth stretch is initiated, the system identifies all connected rectangular worksurfaces that are in line with the main worksurface being stretched. These worksurfaces will be affected by the group stretch operation.

#### Stretching Process

1. When the depth of the main worksurface is changed, all connected worksurfaces in the group will automatically adjust to match the new depth.
2. The system ensures that all connectors and support elements are properly realigned after the stretch operation.

#### Reverting Group Stretch

If the group depth stretch is disabled, all affected worksurfaces will revert to their original depths.

### Super Stretch Functionality

The super stretch feature, which allows for extended stretching capabilities, is not available when group depth stretch is enabled. This ensures consistent behavior across all worksurfaces in the group.

### User Interface Considerations

- When group depth stretch is enabled, certain properties related to individual worksurface stretching (such as "gapLength" and "superEnable") are hidden from the user interface to prevent conflicts with the group behavior.
- These properties become visible again when group depth stretch is disabled.

### Interaction with Other Worksurface Features

- The group depth stretch functionality works in conjunction with the worksurface's support system, ensuring that all supports are properly positioned after a stretch operation.
- The system maintains the original positions of panel-hung supports and adjusts other supports based on their zones and positions relative to the worksurface.

### Limitations and Considerations

- Group depth stretch only affects rectangular worksurfaces that are in line with the main worksurface being stretched.
- The feature is designed to work with straight-back worksurfaces and may not be compatible with other worksurface types.

## Remarks

- Always use the full part number when ordering or specifying products.
- Dimensions are typically in inches and listed in a width-depth format.
- Some product categories may have additional features encoded in their part numbers, such as left/right orientation for towers (e.g., FIKA-TOWER-4BBF-1524-L).
- If you encounter a part number that doesn't seem to fit these patterns, consult with a FIKA representative for clarification.
- The exact behavior of the group depth stretch feature may depend on the specific configuration and types of worksurfaces involved.

This documentation provides a comprehensive overview of the FIKA product line, including the part numbering system and configuration logic for worksurfaces. It enables Interior Designers to confidently interpret and use these codes, as well as understand the functionality of the group depth stretch feature, without needing programming knowledge.