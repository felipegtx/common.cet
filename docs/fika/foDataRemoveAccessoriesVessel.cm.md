# FIKA Product Line Documentation

## Overview

The FIKA product line offers a comprehensive range of office furniture components, including cabinets, bookcases, lateral files, overhead storage, worksurfaces, tables, and various accessories. This document provides detailed information on the part numbering system and configuration logic for the FIKA product line.

## Part Numbers

FIKA part numbers follow a standardized structure to uniquely identify each component:

```
FIKA-[ProductType]-[Specifications]
```

Where:
- `FIKA` is the product line identifier
- `[ProductType]` indicates the type of component
- `[Specifications]` provide details about size, configuration, or other attributes

### Product Types and Their Part Numbers

#### 1. Cabinets (CAB)

| Part Number Format | Description | Example |
|--------------------|-------------|---------|
| FIKA-CAB-BBF-WWDD | Box/Box/File cabinet | FIKA-CAB-BBF-1518 |
| FIKA-CAB-FF-WWDD | File/File cabinet | FIKA-CAB-FF-1824 |
| FIKA-CAB-SBOOO-WWDD | Open cabinet with shelf | FIKA-CAB-SBOOO-1530 |

Where:
- WW: Width in inches (15, 18)
- DD: Depth in inches (18, 24, 30)

#### 2. Bookcases (BOOK)

| Part Number Format | Description | Example |
|--------------------|-------------|---------|
| FIKA-BOOKH-WWDD | Bookcase | FIKA-BOOK3-3024 |

Where:
- H: Height level (2, 3, 4, 5)
- WW: Width in inches (24, 30, 36, 42)
- DD: Depth in inches (24, 30)

#### 3. Lateral Files (LAT)

| Part Number Format | Description | Example |
|--------------------|-------------|---------|
| FIKA-LATH-WWDD | Lateral file | FIKA-LAT3-3618 |

Where:
- H: Height level (1, 15, 2, 3, 4, 5, 6)
- WW: Width in inches (30, 36, 42)
- DD: Depth in inches (18, 24)

#### 4. Overhead Storage (OVERHEAD)

| Part Number Format | Description | Example |
|--------------------|-------------|---------|
| FIKA-OVERHEAD-WW14 | Closed overhead storage | FIKA-OVERHEAD-3614 |
| FIKA-OVERHEAD-WW14-OPEN | Open overhead storage | FIKA-OVERHEAD-4214-OPEN |

Where:
- WW: Width in inches (30, 36, 42, 48, 54, 60)

#### 5. Worksurfaces (WS)

| Part Number Format | Description | Example |
|--------------------|-------------|---------|
| FIKA-WS-RECT-WWDD | Rectangular worksurface | FIKA-WS-RECT-3060 |
| FIKA-WS-ARC-WWDD | Arc-shaped worksurface | FIKA-WS-ARC-3672 |
| FIKA-WS-120-WWDDHHDD | 120-degree worksurface | FIKA-WS-120-30484830 |

Where:
- WW: Width in inches
- DD: Depth in inches
- HH: Height in inches (for 120-degree surfaces)

#### 6. Tables (TBL)

| Part Number Format | Description | Example |
|--------------------|-------------|---------|
| FIKA-TBL-FSRECT-WWDD | Rectangular table | FIKA-TBL-FSRECT-4242 |
| FIKA-TBL-FSROUND-DD | Round table | FIKA-TBL-FSROUND-48 |

Where:
- WW: Width in inches
- DD: Depth or Diameter in inches

#### 7. Accessories

| Part Number Format | Description | Example |
|--------------------|-------------|---------|
| FIKA-CANTILEVER-[Type] | Cantilever support | FIKA-CANTILEVER-LH |
| FIKA-CHR-[Type] | Chair | FIKA-CHR-AR |
| FIKA-COH-[Length] | Cohesion | FIKA-COH-24 |
| FIKA-J-[Length]-[Type] | J-channel | FIKA-J-60-E |
| FIKA-PF-WWDD | Privacy filter | FIKA-PF-3048 |
| FIKA-SHELF-WWDD | Shelf | FIKA-SHELF-3609 |
| FIKA-TILE-WWDD | Tile | FIKA-TILE-4860 |

Where:
- WW: Width in inches
- DD: Depth in inches
- [Type]: Specific type or configuration
- [Length]: Length in inches

## Configuration Logic

### Accessory Removal

The FIKA product line includes functionality for removing accessories from worksurfaces, implemented through the FODataRemoveAccessoriesVessel.

#### Spread Options

The accessory removal feature supports different spread options:

1. **No Spread**: Only affects the selected worksurface.
2. **Sideways**: Affects the selected worksurface and its connected neighbors.
3. **Group**: Affects all worksurfaces in the same connected group as the selected worksurface.
4. **All**: Affects all worksurfaces in the main space.

#### Visual Representation

The accessory removal process provides visual feedback in both 2D and 3D representations:

##### 2D Representation
- For spread options other than "No Spread":
  - Affected worksurfaces are filled with a dark red color (RGB: 192, 64, 64).
  - If no worksurfaces are affected, a gray circle is displayed at the current position.

##### 3D Representation
- For spread options other than "No Spread":
  - Affected worksurfaces are highlighted with a red frame.
  - A red arrow is placed at the center of each affected worksurface, pointing upwards.
  - If no worksurfaces are affected, a gray arrow is displayed at the current position.

#### Interaction and Invalidation

- The accessory removal process interacts with worksurfaces and their accessories, potentially affecting multiple worksurfaces based on their connections and groupings.
- When accessories are removed, the affected worksurfaces are marked for rebuilding their 2D representation to reflect the changes.

## Remarks

- All part numbers start with "FIKA-" to identify the product line.
- Dimensions are typically expressed in inches and follow a width-depth-height order when applicable.
- Some product types have additional identifiers (e.g., "FS" for freestanding tables, "OPEN" for open storage units).
- Always refer to the most up-to-date product catalog for the complete list of available part numbers and their specifications.
- The exact appearance of the 2D and 3D representations for accessory removal may vary depending on the implementation of referenced methods and materials.
- This documentation combines information from both the part numbering system and the configuration logic. For the most accurate and up-to-date information on specific features or functionalities, please consult the relevant technical documentation or contact the FIKA support team.