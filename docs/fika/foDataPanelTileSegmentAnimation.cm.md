Based on the provided documents, I will consolidate the information into a single, clear, and concise document. Since there is no information in the Part Numbers document, all the content will be derived from the Configuration Logic document.

# Data Panel Tile Segment Animation

This document describes the functionality of the Data Panel Tile Segment Animation, which manages the segmentation of data panel tiles in an office environment.

## Overview

The Data Panel Tile Segment Animation allows users to customize how data panels are divided into tiles using two main methods:

1. By height
2. By number of tiles

## Key Features

### Tile Splitting Methods

1. **Split by Height**: Users specify a fixed height for each tile. The panel is divided into as many tiles as necessary to fill the total height.

2. **Split by Number**: Users specify the number of tiles they want. The panel's height is divided equally among these tiles.

### Default Settings

- Default tile height: 24 inches
- Default number of tiles: 3

### Customization Options

Users can modify:
- The splitting method (height or number)
- The default tile height (when using split by height)
- The number of tiles (when using split by number)

## Behavior and Constraints

1. The system remembers the last used settings for splitting method, tile height, and number of tiles.

2. The interface updates to show relevant options when changing the splitting method.

3. The number of tiles is limited based on the panel's total height and the minimum allowable tile height. The system automatically adjusts if an invalid number is selected.

4. Tile heights are restricted to a predefined set of valid heights (determined by the `actualTileHDomain()` method).

5. The maximum number of tiles is set to 10.

## Interaction with Frames

- The animation can be applied to both upper and lower sides of a frame.
- It can spread horizontally across multiple frames if the `horizontalSpread` option is enabled.
- The animation only applies to frames identified as Data Panel Frames.

## Updating Process

1. When the user moves the animation, the system checks if the target frame has changed.
2. If the frame changes, properties are rebuilt to reflect the new frame's dimensions and constraints.
3. Tiles are then split according to current settings and applied to the frame.

## Limitations and Edge Cases

- If the remaining height is less than the specified tile height, the last tile will be smaller to fit the available space.
- The system ensures that the number of tiles always results in valid tile heights.

## Remarks

- This documentation does not cover internal implementation details or exact methods for calculating valid tile heights and numbers.
- The actual visual representation of the tiles may depend on other components not described in this class.