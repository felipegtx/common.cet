Here's the consolidated document combining the information from both sources:

# FIKA Office Cantilever Support Documentation

## Product Overview

This document describes the logic, configuration rules, and part numbering system for the FIKA Office Cantilever Support, a component used in office furniture systems.

## Dimensions

The Cantilever Support has the following dimensions:
- Width: 1.5 inches (3 inches if shared)
- Depth: 16 inches
- Height: 16 inches

## Handedness Options

The Cantilever Support can be configured with three handedness options:
1. Left-handed
2. Right-handed
3. Shared (double-width)

## Part Number Logic

The part number for the Cantilever Support follows this structure:

FIKA-CANTILEVER-[HANDEDNESS]

Where [HANDEDNESS] can be:
- LH for Left-handed
- RH for Right-handed
- DBL for Shared (double-width)

Here's a table explaining the part number structure:

| Prefix | Product Type | Handedness |
|--------|--------------|------------|
| FIKA-  | CANTILEVER-  | LH / RH / DBL |

Valid part numbers and their descriptions:

| Part Number | Description |
|-------------|-------------|
| FIKA-CANTILEVER-LH | Left-handed Cantilever Support |
| FIKA-CANTILEVER-RH | Right-handed Cantilever Support |
| FIKA-CANTILEVER-DBL | Shared (double-width) Cantilever Support |

These part numbers represent the complete range of Cantilever Support configurations available in the FIKA office furniture system.

## Configuration Rules and Logic

1. Handedness Selection:
   - The handedness is automatically determined based on the support's location on the worksurface.
   - The system analyzes the support's location relative to the worksurface edges.
   - If the support is within a certain distance from the left edge, it's configured as left-handed (LH).
   - If it's within a certain distance from the right edge, it's configured as right-handed (RH).
   - If it's positioned between two adjacent worksurfaces, it's configured as shared (DBL).

2. Width Adjustment:
   - For left-handed or right-handed supports, the width is 1.5 inches.
   - For shared supports, the width is doubled to 3 inches.

3. Position on Worksurface:
   - Left-handed supports are positioned at the left edge of their designated space.
   - Right-handed supports are positioned at the right edge of their designated space.
   - Shared supports are centered in their designated space.

4. Labeling:
   - Each support is labeled with a tag for easy identification.
   - The tag includes "C-" followed by a letter indicating the handedness:
     - "C-L" for left-handed
     - "C-R" for right-handed
     - "C-S" for shared

5. Tag Positioning:
   - For left-handed supports, the tag is positioned to the right of the support.
   - For right-handed supports, the tag is positioned to the left of the support.
   - For all supports, the tag is placed at the front edge of the support.

6. Automatic Part Number Assignment:
   - Based on the position determination, the system automatically assigns the appropriate part number.
   - This ensures that the correct support type is always specified for each location.

7. Visual Representation Updates:
   - The 2D and 3D representations of the support are updated to reflect the assigned configuration.
   - This includes adjusting the width, position, and labeling of the support in all views.

## Interaction with Other Components

1. Worksurface Compatibility:
   - The Cantilever Support is designed to work with compatible worksurfaces.
   - It communicates changes in its properties to the parent worksurface.

2. Visual Representation:
   - When attached to a worksurface, the support is represented with a dotted line in 2D views.
   - The color of this line matches the surface color of the worksurface.

## Configuration Validation

The system checks for any undecided options in the support's configuration. If any options are not fully specified, it will flag this as an invalid configuration that needs to be resolved before proceeding.

## Remarks and Disclaimers

- This documentation assumes that the Cantilever Support is always used in conjunction with a compatible worksurface.
- The exact mechanism for attaching the support to the worksurface is not detailed in this document.
- The system for automatically determining the support's location and handedness may involve additional components or logic not visible in the provided information.