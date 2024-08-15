Since there is no information provided in the "Part Numbers" document, I will consolidate the information from the "Configuration Logic" document while maintaining its structure and content. Here's the consolidated documentation:

# FODataSkin Documentation

This document describes the functionality and behavior of the FODataSkin class, which is responsible for managing the skin of a panel in an office furniture configuration system.

## Overview

The FODataSkin class represents a skin of a panel, which can be either the upper or lower part of the panel. It manages the tiles that make up the skin, their properties, and various operations that can be performed on them.

## Key Features

1. **Tile Management**: The skin is composed of multiple tiles (FODataTile objects) that can be added, removed, or modified.

2. **Color Scheme Handling**: The class provides methods to manage color schemes for the tiles, including the ability to set and retrieve color information.

3. **Material Management**: It allows setting and retrieving materials for specific ranges within the skin.

4. **Dimension Handling**: The class manages the width and height of the skin, which are typically derived from the panel it belongs to.

5. **Invalidation Checking**: It can check for and report any undecided options in the skin configuration.

6. **Elevation Graphs**: The class can generate elevation graphs for visual representation of the skin.

## Tile Operations

### Initialization
When the skin is initialized, it creates a single tile that spans the entire height of the skin.

### Merging Tiles
Tiles can be merged together. When merging, the following rules apply:
- If a tile is selected, it will be preserved while other tiles in the merge range are removed.
- If no tile is selected, the first tile in the merge range is preserved.
- The height of the preserved tile is adjusted to cover the entire merged area.

### Updating Tiles
After any changes to the tiles, the skin updates various properties:
- Assigns unique keys to each tile based on their position and whether it's the upper or lower skin.
- Synchronizes data with the panel.
- Invalidates the panel's edit connectors for both upper and lower skins.
- Updates the panel name if applicable.

## Color Scheme Management

The skin provides methods to manage color schemes for its tiles:

1. **Get Color Scheme**: Retrieves the current color scheme for the entire skin or a specific range.
2. **Get Colorless Scheme**: Creates a color scheme where all tiles are set to an "undecided" state.
3. **Set Color Scheme**: Applies a given color scheme to the skin's tiles.

## Material Management

The skin allows setting materials for specific ranges within it. When setting a material:
- It checks if the given range intersects with each tile.
- If there's an intersection, it attempts to set the material for that tile.
- The operation returns true if at least one tile's material was successfully set.

## Dimension Handling

The skin's width and height are typically derived from the panel it belongs to. If no panel is associated, default values are used:
- Default width: 42 inches
- Default height: 60 inches

## Invalidation Checking

The skin can check for any undecided options in its configuration. If any tile has undecided options, it reports an invalidation.

## Elevation Graphs

The skin can generate elevation graphs, which include:
- Material labels for each tile (if enabled)
- Tile height labels (if enabled)

These graphs are positioned relative to the skin's dimensions and the panel's configuration.

## Remarks and Disclaimers

1. This documentation is based on the provided class definition and may not cover all possible use cases or edge cases.
2. The exact behavior of some methods may depend on the implementation of related classes (e.g., FODataTile, FODataPanelFrame) which are not fully defined in the given code.
3. The part number logic is not explicitly defined in this class. It may be handled by the panel or individual tiles.
4. Specific dimension constraints and product rules are not explicitly defined in this class and may be handled at a higher level in the product hierarchy.