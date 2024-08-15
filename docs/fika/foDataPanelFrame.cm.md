# Panel Frame Documentation

This document describes the logic and behavior of a Panel Frame product in the FIKA Office system. The Panel Frame is a versatile component used in office layouts, consisting of an upper and lower skin, and various customizable features.

## Product Overview

The Panel Frame is a vertical element used in office spaces. It has the following key characteristics:

1. Consists of an upper skin (upSkin) and a lower skin (downSkin)
2. Customizable width and height
3. Various material options for top trim and base cover
4. Can interact with other office components like worksurfaces

## Dimensions and Constraints

### Width
- Minimum width: 24 inches
- Maximum width: 60 inches
- Width adjusts in 6-inch increments

### Height
- Minimum height: 30 inches (based on available part numbers)
- Maximum height: 66 inches (based on available part numbers)
- Height adjusts in 6-inch increments

### Depth
- Fixed depth: Defined by the frame depth constant (not specified in part numbers)

## Part Number Logic

The part number for a Panel Frame is constructed as follows:

```
FIKA-PF-[Width in inches][Height in inches]
```

Here's a breakdown of the part number components:

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| FIKA      | Product line identifier | Fixed as "FIKA" |
| PF        | Product type (Panel Frame) | Fixed as "PF" |
| Width     | Width in inches | 24, 30, 36, 42, 48, 54, 60 |
| Height    | Height in inches | 30, 36, 42, 48, 54, 60, 66 |

Example: For a panel frame that is 42 inches wide and 66 inches high, the part number would be:
```
FIKA-PF-4266
```

## Valid Part Numbers

Based on the provided list of known part numbers, here are all the valid Panel Frame part numbers:

FIKA-PF-2430, FIKA-PF-2436, FIKA-PF-2442, FIKA-PF-2448, FIKA-PF-2454, FIKA-PF-2460, FIKA-PF-2466,
FIKA-PF-3030, FIKA-PF-3036, FIKA-PF-3042, FIKA-PF-3048, FIKA-PF-3054, FIKA-PF-3060, FIKA-PF-3066,
FIKA-PF-3630, FIKA-PF-3636, FIKA-PF-3642, FIKA-PF-3648, FIKA-PF-3654, FIKA-PF-3660, FIKA-PF-3666,
FIKA-PF-4230, FIKA-PF-4236, FIKA-PF-4242, FIKA-PF-4248, FIKA-PF-4254, FIKA-PF-4260, FIKA-PF-4266,
FIKA-PF-4830, FIKA-PF-4836, FIKA-PF-4842, FIKA-PF-4848, FIKA-PF-4854, FIKA-PF-4860, FIKA-PF-4866,
FIKA-PF-5430, FIKA-PF-5436, FIKA-PF-5442, FIKA-PF-5448, FIKA-PF-5454, FIKA-PF-5460, FIKA-PF-5466,
FIKA-PF-6030, FIKA-PF-6036, FIKA-PF-6042, FIKA-PF-6048, FIKA-PF-6054, FIKA-PF-6060, FIKA-PF-6066

## Customization Options

### Top Trim
The top trim can be customized with various materials:
- Veneer
- Laminate (LPL or HPL)
- Metal (Painted or Brushed)

### Base Cover
The base cover also offers material options:
- Veneer
- Laminate (LPL or HPL)
- Metal (Painted or Brushed)

## Interaction with Other Components

1. The Panel Frame can connect to worksurfaces on both its upper and lower sides.
2. It adjusts its minimum height based on connected components like hung panels or worksurfaces.
3. The frame has a floor gap of 0.5 inches and a base cover height of 4 inches.

## Configuration Rules

1. The selected height must be within the valid height domain, which considers connected components.
2. When stretching the panel height, it may affect connected components and neighboring panels.
3. The width can be adjusted, and this change will update connected components like worksurfaces.
4. The panel has a top cap with a thickness of 0.5 inches.

## Visual Representation

- In 2D views, the panel is represented by a rectangle with darker areas for the skins.
- In 3D views, the panel shows detailed representations of the skins and their materials.
- The panel can display a text label showing its name and dimensions.

## Additional Features

1. The panel can be tagged with additional information.
2. It supports mirroring.
3. Users can select individual tiles on the panel for more detailed configuration.
4. The panel participates in various animations during insertion and modification in the layout.

## Invalidation and Error Checking

The system checks for undecided options in the panel's configuration. If any options are not fully specified, it will be flagged for the user's attention.

## Remarks and Disclaimers

This documentation is based on the provided class information and the list of known part numbers. The exact behavior of some features might depend on the implementation of referenced classes or methods not provided in this snippet. Always refer to the most up-to-date product specifications and guidelines when configuring Panel Frames.