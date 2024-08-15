# Fika Office Selection Filter Documentation

This document describes the functionality of the Fika Office Selection Filter, which is used to filter and manage the selection of various office components in a space.

## Overview

The Fika Office Selection Filter allows users to select and filter different types of office components, primarily focusing on panels, worksurfaces, storage units, and accessories. It provides a user interface for selecting these components and manages the filtering process based on the user's choices.

## Main Components

1. **Panels**: Various types of panels that can be selected and filtered.
2. **Worksurfaces**: Different types of worksurfaces, including free-standing tables, straight-back worksurfaces, and corner worksurfaces.
3. **Storage Units**: Cabinets, towers, and other storage solutions.
4. **Accessories**: Additional components such as overhead units, shelves, and supports.

## Part Number Structure

Fika office components use a standardized part numbering system. Here's a breakdown of the structure:

| Component | Format | Example | Description |
|-----------|--------|---------|-------------|
| Prefix | FIKA- | FIKA- | Identifies the product line |
| Product Type | XXX- | WS- | Indicates the type of product (e.g., WS for Worksurface) |
| Configuration | XXX- | RECT- | Specifies the configuration or shape |
| Dimensions | XXXX | 2430 | Dimensions in inches (width x depth) |

### Example Part Numbers

1. **Worksurfaces**: 
   - `FIKA-WS-RECT-2430`: Rectangular worksurface, 24" x 30"
   - `FIKA-WS-ARC-3060`: Arc-shaped worksurface, 30" x 60"

2. **Storage Units**:
   - `FIKA-CAB-BBF-1524`: Cabinet with Box/Box/File configuration, 15" x 24"
   - `FIKA-TOWER-4FF-1524-L`: Tower with 4 file drawers, 15" x 24", left-handed

3. **Panels**:
   - `FIKA-TILE-3060`: Panel tile, 30" x 60"

4. **Accessories**:
   - `FIKA-OVERHEAD-3614`: Overhead storage unit, 36" x 14"
   - `FIKA-SHELF-3009`: Shelf, 30" x 9"

## Selection Process

The filter works by creating a tree structure of selectable items. The main categories are:

1. Panel Types
2. Worksurface Types
3. Storage Units
4. Accessories

Each category is further divided into subcategories based on configurations and dimensions.

### Panel Types

Panel types are determined by their frame names. Each unique frame name becomes a selectable item in the filter.

### Worksurface Types

There are three types of worksurfaces:

1. Free-standing
2. Straight-back
3. Corner

## User Interface

The filter provides a popup dialog for users to interact with. This dialog includes:

1. A search input at the top, allowing users to search for specific items.
2. A tree view displaying all selectable items organized by category.

Users can check or uncheck items in the tree view to include or exclude them from the selection.

## Filtering Logic

When a user makes a selection:

1. The system checks all items in the current selection.
2. For each item, it determines if it matches the user's filter criteria.
3. If an item doesn't match the criteria, it is removed from the selection.

The filter considers several factors when determining if an item should be included:

1. The item must be active.
2. For composite items (block snappers), at least one of its sub-components must match the criteria.
3. The item must be allowed to be selected and visible in the space.

## Search Functionality

The search feature allows users to quickly find specific items:

1. As the user types in the search box, the tree view updates in real-time.
2. Items matching the search term (case-insensitive) are displayed.
3. If a parent item doesn't match but has children that do, it will still be shown to maintain the hierarchy.

## Conclusion

The Fika Office Selection Filter provides a powerful and user-friendly way to select and filter office components. It allows for precise control over which items are included in a selection, making it easier for users to work with specific subsets of office components. The standardized part numbering system ensures clear identification and organization of all available products.