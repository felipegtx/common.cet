# Fika Office Selection Filter Documentation

This document describes the functionality of the Fika Office Selection Filter, which is used to filter and manage the selection of office furniture components in a space.

## Overview

The Fika Office Selection Filter allows users to select and filter different types of office furniture components, specifically panels, worksurfaces, cabinets, bookcases, lateral files, and storage towers. It provides a user interface for selecting these components and manages the filtering process based on the user's selections.

## Component Types and Part Numbers

The filter recognizes several main types of components, each with its own part numbering system:

### 1. Panels

Panels are categorized by their frame names and use the "TILE" product type in their part numbers.

Example: `FIKA-TILE-3060`

| Component | Meaning |
|-----------|---------|
| TILE | Panel or Tile |
| 30 | Width (30 inches) |
| 60 | Height (60 inches) |

### 2. Worksurfaces

Worksurfaces are divided into three categories:

1. Free-standing
2. Straight-back
3. Corner

Worksurfaces use the "WS" product type in their part numbers.

Example: `FIKA-WS-RECT-2460`

| Component | Meaning |
|-----------|---------|
| WS | Worksurface |
| RECT | Rectangular shape |
| 24 | Depth (24 inches) |
| 60 | Width (60 inches) |

Other worksurface configurations include:
- ARC: Arc-shaped worksurface
- 120: 120-degree corner worksurface
- 90: 90-degree corner worksurface

### 3. Cabinets

Cabinets are identified by the "CAB" product type.

Example: `FIKA-CAB-BBF-1518`

| Component | Meaning |
|-----------|---------|
| CAB | Cabinet |
| BBF | Box/Box/File configuration |
| 15 | Width (15 inches) |
| 18 | Depth (18 inches) |

Other cabinet configurations include:
- FF: File/File
- SBOOO: Side-to-Side Box/Open/Open/Open

### 4. Bookcases

Bookcases use the "BOOK" product type.

Example: `FIKA-BOOK3-2430`

| Component | Meaning |
|-----------|---------|
| BOOK3 | Bookcase with 3 shelves |
| 24 | Width (24 inches) |
| 30 | Height (30 inches) |

### 5. Lateral Files

Lateral files use the "LAT" product type.

Example: `FIKA-LAT3-3624`

| Component | Meaning |
|-----------|---------|
| LAT3 | Lateral file with 3 drawers |
| 36 | Width (36 inches) |
| 24 | Height (24 inches) |

### 6. Storage Towers

Storage towers use the "TOWER" product type.

Example: `FIKA-TOWER-4BBF-1524-L`

| Component | Meaning |
|-----------|---------|
| TOWER | Storage Tower |
| 4BBF | 4-high Box/Box/File configuration |
| 15 | Width (15 inches) |
| 24 | Depth (24 inches) |
| L | Left-hand configuration |

## User Interface

The filter presents a popup dialog with a tree view structure. The tree view is organized to include all component types:

- Panel Types
  - [List of available panel frame names]
- Worksurface Types
  - Free-standing
  - Straight-back
  - Corner
- Cabinets
- Bookcases
- Lateral Files
- Storage Towers

Users can check or uncheck items in the tree view to include or exclude them from the selection.

## Filtering Process

When a user makes a selection in the tree view:

1. The system collects all the selected items.
2. It then filters the current selection in the space, removing any components that don't match the selected criteria.
3. Components are evaluated based on their type and part number.

## Search Functionality

The filter includes a search feature that allows users to quickly find specific items in the tree view. As the user types in the search box, the tree view updates to show only the matching items.

## Selection Management

The filter keeps track of the current selection state. When items are checked or unchecked in the tree view:

1. The system updates the internal selection state.
2. It then applies this selection to the space, updating which components are visible or selectable.

## Component Identification

The filter uses a symbol-based system to identify different component types:

- Panels: "fikaPanelType.[frame name]"
- Worksurfaces:
  - "fikaWsType.free" for free-standing
  - "fikaWsType.straight" for straight-back
  - "fikaWsType.corner" for corner worksurfaces
- Other components are identified by their respective product types in the part numbers.

## Important Notes for Designers

1. Always use the full part number when specifying products to ensure accuracy.
2. The dimensions in part numbers are typically in inches and follow the pattern of width-depth or width-height, depending on the product type.
3. Some product types have additional options (like left/right orientation) at the end of the part number.
4. When in doubt about a part number's meaning, refer to this documentation or consult with a Fika Office representative.

## Remarks and Disclaimers

- The effectiveness of the filter depends on the correct categorization of components in the space. Ensure that all furniture components are properly classified with the correct part numbers and subtypes.
- The search functionality is case-insensitive but relies on exact matches. Users should be aware that partial matches might not yield expected results.
- The filter's performance may be affected in spaces with a very large number of components. In such cases, the filtering process might take longer to complete.

By understanding both the logic behind the part numbers and the configuration of the selection filter, Interior Designers can more efficiently specify and order the correct products for their projects without needing to understand the underlying programming of the selection filter.