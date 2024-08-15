# Fika Office Library Documentation

This document describes the functionality and structure of the Fika Office Library, which is a collection of office furniture and accessories that can be configured and placed in a virtual space.

## Library Structure

The Fika Office Library is organized into several main categories:

1. Global Settings
2. Panels
3. Worksurfaces
4. Supports
5. Tables
6. Low Storage
7. Upper Storage
8. Chairs

Each category contains various products that can be added to the virtual space.

## Product Categories and Part Numbers

### Panels

The Panels category includes:
- Panel Frames
- Wall Starts
- Panel Tile Segments
- Panel Type Elevations

Users can customize panels with different materials:
- Fabric
- Veneer
- Laminate
- Markerboard
- Glass

A Panel Manager is available for more advanced configuration options.

Panel part numbers follow this structure:

| Part | Description | Possible Values |
|------|-------------|-----------------|
| FIKA | Brand identifier | Always "FIKA" |
| TILE | Product type | Always "TILE" |
| XX | Width in inches | 24, 30, 36, 42, 48, 54, 60 |
| YY | Height in inches | 06, 12, 18, 24, 30, 36, 42, 48, 54, 60 |

Example: FIKA-TILE-3024 (30" wide, 24" high panel tile)

### Worksurfaces

The Worksurfaces category includes:
- Rectangular Worksurfaces
- Arc Front Worksurfaces
- 90-Degree Corner Worksurfaces
- 120-Degree Corner Worksurfaces

Worksurface part numbers follow this structure:

| Part | Description | Possible Values |
|------|-------------|-----------------|
| FIKA | Brand identifier | Always "FIKA" |
| WS | Product type (Worksurface) | "WS" |
| TYPE | Shape type | RECT (Rectangular), ARC (Arc Front), 90 (90-Degree), 120 (120-Degree) |
| XX | Width in inches | Various sizes (18-96) |
| YY | Depth in inches | Various sizes (18-48) |

Examples:
- FIKA-WS-RECT-3060 (30" x 60" rectangular worksurface)
- FIKA-WS-ARC-3660 (36" x 60" arc front worksurface)
- FIKA-WS-90-24363624 (24" x 36" x 36" x 24" 90-degree corner worksurface)
- FIKA-WS-120-30424230 (30" x 42" x 42" x 30" 120-degree corner worksurface)

### Supports

The Supports category allows users to:
- Enable or disable automatic supports
- Add cantilever supports
- Remove supports
- Reset supports to default configuration

Support part numbers:

- FIKA-CANTILEVER-LH (Left-hand cantilever support)
- FIKA-CANTILEVER-RH (Right-hand cantilever support)
- FIKA-CANTILEVER-DBL (Double cantilever support)

### Tables

The Tables category includes:
- Rectangular Tables
- Round Tables

Table part numbers follow this structure:

| Part | Description | Possible Values |
|------|-------------|-----------------|
| FIKA | Brand identifier | Always "FIKA" |
| TBL | Product type (Table) | "TBL" |
| SHAPE | Table shape | FSRECT (Freestanding Rectangular), FSROUND (Freestanding Round) |
| XX | Width/Diameter in inches | Various sizes (30-84) |
| YY | Depth in inches (for rectangular tables) | 36, 42 |

Examples:
- FIKA-TBL-FSRECT-6036 (60" x 36" rectangular table)
- FIKA-TBL-FSROUND-48 (48" diameter round table)

### Low Storage

The Low Storage category includes:
- Lateral File Cabinets
- Bookcases
- Pedestals
- Bookcase Towers

Low storage part numbers follow these structures:

Lateral File Cabinets:
| Part | Description | Possible Values |
|------|-------------|-----------------|
| FIKA | Brand identifier | Always "FIKA" |
| LAT | Product type (Lateral File) | "LAT" |
| X | Number of drawers | 1-6 |
| XX | Width in inches | 30, 36, 42 |
| YY | Height in inches | 18, 24 |

Example: FIKA-LAT3-3624 (3-drawer lateral file, 36" wide, 24" high)

Bookcases:
| Part | Description | Possible Values |
|------|-------------|-----------------|
| FIKA | Brand identifier | Always "FIKA" |
| BOOK | Product type (Bookcase) | "BOOK" |
| X | Number of shelves | 2-5 |
| XXYY | Width and Height in inches | Various sizes |

Example: FIKA-BOOK3-3630 (3-shelf bookcase, 36" wide, 30" high)

### Upper Storage

The Upper Storage category includes:
- Overhead Cabinets
- Shelves

Upper storage part numbers follow these structures:

Overhead Cabinets:
| Part | Description | Possible Values |
|------|-------------|-----------------|
| FIKA | Brand identifier | Always "FIKA" |
| OVERHEAD | Product type | "OVERHEAD" |
| XX | Width in inches | 30, 36, 42, 48, 54, 60 |
| YY | Height in inches | Always 14 |
| OPEN | Optional open shelf indicator | "OPEN" or omitted |

Examples:
- FIKA-OVERHEAD-3614 (36" wide, 14" high overhead cabinet)
- FIKA-OVERHEAD-4214-OPEN (42" wide, 14" high open overhead cabinet)

Shelves:
| Part | Description | Possible Values |
|------|-------------|-----------------|
| FIKA | Brand identifier | Always "FIKA" |
| SHELF | Product type | "SHELF" |
| XX | Width in inches | 24, 30, 36, 42, 48, 54, 60 |
| YY | Depth in inches | Always 09 |

Example: FIKA-SHELF-3609 (36" wide, 9" deep shelf)

### Chairs

The Chairs category allows users to add office chairs to the space.

Chair part numbers:
- FIKA-CHR-01 (Standard chair)
- FIKA-CHR-AR (Chair with arms)
- FIKA-CHR-HR (Chair with headrest)

## Configuration Options

### Auto Supports

Users can toggle automatic support generation for worksurfaces. When enabled, the system will automatically add necessary supports. When disabled, users can manually add or remove supports as needed.

### Material Selection

For panels and possibly other products, users can select from various materials including fabric, veneer, laminate, markerboard, and glass. This allows for customization of the appearance of the office furniture.

### Panel Manager

A dedicated Panel Manager is available for more detailed configuration of panel systems. This tool likely allows for advanced customization of panel layouts and properties.

### Scheme Selection

Users can access a scheme selector, which may allow for saving and loading different configuration presets or color schemes for the office layout.

## Interaction Methods

The library uses various interaction methods for product placement and configuration:

- Snapper: Used for placing individual items like worksurfaces, tables, and storage units.
- Animation: Used for more complex actions like configuring panel tile segments or applying materials.
- Callback: Used for actions like toggling auto supports or managing supports.

## Notes

- The library checks for the presence of a specific catalog ("FIKA") before loading. If the catalog is missing, a simplified version of the library is presented.
- There are developer tools available in non-release mode, which are not accessible to end-users.
- The library uses a consistent icon size for most products (30x44 pixels) to maintain a uniform appearance in the interface.

This documentation provides an overview of the Fika Office Library's structure, functionality, and part