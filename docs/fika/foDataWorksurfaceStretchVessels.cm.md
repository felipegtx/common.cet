Here's the consolidated document combining the information from both sources:

# 120-Degree Worksurface Stretch Vessel Documentation

This document describes the functionality and behavior of the 120-Degree Worksurface Stretch Vessel, which is a component used in office furniture configuration.

## Overview

The 120-Degree Worksurface Stretch Vessel is a specialized type of worksurface that extends the capabilities of a standard worksurface stretch vessel. It is designed to work with 120-degree corner surfaces, providing specific positioning for stretch-related visual elements.

## Part Numbers

The 120-Degree Worksurface Stretch Vessel is part of the FIKA product line. The relevant part numbers for this product are:

| Part Number | Description |
|-------------|-------------|
| FIKA-WS-120-18363618 | 120-Degree Worksurface, 36"x36"x18" |
| FIKA-WS-120-18424218 | 120-Degree Worksurface, 42"x42"x18" |
| FIKA-WS-120-18484818 | 120-Degree Worksurface, 48"x48"x18" |
| FIKA-WS-120-24363624 | 120-Degree Worksurface, 36"x36"x24" |
| FIKA-WS-120-24484824 | 120-Degree Worksurface, 48"x48"x24" |
| FIKA-WS-120-30363630 | 120-Degree Worksurface, 36"x36"x30" |
| FIKA-WS-120-30424230 | 120-Degree Worksurface, 42"x42"x30" |
| FIKA-WS-120-30484830 | 120-Degree Worksurface, 48"x48"x30" |

The part number structure can be broken down as follows:

| Prefix | Product Type | Angle | Depth | Width 1 | Width 2 | Height |
|--------|--------------|-------|-------|---------|---------|--------|
| FIKA   | WS (Worksurface) | 120 | 18/24/30 | 36/42/48 | 36/42/48 | 18/24/30 |

For example, FIKA-WS-120-30484830 represents a 120-degree worksurface with a depth of 30", widths of 48" on both sides, and a height of 30".

## Functionality

### Stretch Text Position

The stretch text position is determined based on the following logic:

- If a 120-degree corner surface is present:
  - The text is positioned 6 inches to the left of the left edge of the surface
  - It is placed 12 inches below the surface
  - The text appears 1 inch above the top of the worksurface

- If no surface is detected, the text will not be displayed

### Stretch Arrow Position

The stretch arrow position is calculated using these rules:

1. The system checks for both a 120-degree corner surface and a connection point (snap)
2. If both are present:
   - For connection points on the right side or front edge:
     - If the connection is a line, the arrow is placed at the end of the line
     - Otherwise, it's placed at the connection point itself
   - The arrow always appears 1 inch above the top of the worksurface
3. If either the surface or connection point is missing, no arrow will be displayed

## Interaction with Other Components

This component is designed to work specifically with 120-degree corner surfaces. It relies on the presence of these surfaces to properly position its visual elements (text and arrows).

The component also interacts with connection points, particularly those on the right side and front edge of the surface. These connection points influence the positioning of the stretch arrow.

## Dimensions and Measurements

The component uses the following measurements:

- 6 inches: Used to offset the text position from the left edge of the surface
- 12 inches: Used to position the text below the surface
- 1 inch: The height above the worksurface where both text and arrows are displayed

Available dimensions for the worksurface itself can be found in the part number table above.

## Rules and Constraints

1. The stretch text and arrow will only be displayed if a valid 120-degree corner surface is detected
2. The arrow position is dependent on the presence and type of connection points
3. All visual elements (text and arrows) are positioned 1 inch above the worksurface top

## Remarks and Disclaimers

- This documentation covers the basic functionality of the 120-Degree Worksurface Stretch Vessel
- The exact appearance and behavior of the stretch text and arrows may depend on other components or settings not described in this document
- For more detailed information or specific configurations, please consult the product manual or contact customer support