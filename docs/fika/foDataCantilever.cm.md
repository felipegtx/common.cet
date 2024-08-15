Here's the consolidated document that combines the information from both sources while removing redundancies and maintaining clarity:

# FIKA Office Cantilever Support Documentation

## Product Overview

This document describes the logic and rules for the FIKA Office Cantilever Support, a component used in office furniture configurations. The cantilever support is designed to provide structural support for worksurfaces and can be configured in different ways depending on its placement and usage.

## Dimensions

The cantilever support has the following dimensions:

- Width: 1.5 inches (3 inches when shared)
- Depth: 16 inches
- Height: 16 inches

## Handedness Options

The cantilever support can be configured with three different handedness options:

1. Left-handed
2. Right-handed
3. Shared (double-sided)

The handedness is determined automatically based on its placement on the worksurface.

## Part Number Logic

The part number for the cantilever support follows this structure:

```
FIKA-CANTILEVER-[HANDEDNESS]
```

Where [HANDEDNESS] can be:
- "LH" for left-handed
- "RH" for right-handed
- "DBL" for shared (double-sided)

Here's a table explaining the part number structure:

| Prefix | Product Type | Handedness |
|--------|--------------|------------|
| FIKA-  | CANTILEVER-  | LH/RH/DBL  |

Valid part numbers for the FIKA Office Cantilever Support:

1. FIKA-CANTILEVER-LH
2. FIKA-CANTILEVER-RH
3. FIKA-CANTILEVER-DBL

## Placement and Configuration Rules

1. The cantilever support's handedness is automatically determined based on its placement on the worksurface:
   - If it can be shared, it will be set as a shared support
   - If it's placed on the left side, it will be set as left-handed
   - If it's placed on the right side, it will be set as right-handed

2. The width of the support changes based on its handedness:
   - For left-handed or right-handed: 1.5 inches
   - For shared (double-sided): 3 inches (2 * 1.5 inches)

3. The position of the support relative to the worksurface changes based on its handedness:
   - Left-handed: Aligned to the left edge of its bounding box
   - Right-handed: Moved to align with the right edge of its bounding box
   - Shared: Centered (moved half its width to the left)

## Labeling and Identification

1. The cantilever support is labeled with a tag for easy identification:
   - The tag always starts with "C-" followed by a letter indicating its handedness:
     - "C-L" for left-handed
     - "C-R" for right-handed
     - "C-S" for shared

2. The position of the identification tag depends on the handedness:
   - For left-handed supports, the tag is placed further to the right
   - For right-handed supports, the tag is placed further to the left
   - For all supports, the tag is positioned at the front edge of the support

## Interaction with Other Components

1. The cantilever support is designed to work with worksurfaces in the FIKA office system.
2. It can be automatically generated as part of a worksurface configuration.
3. The support has a priority system, which may affect its placement or interaction with other components in complex configurations.

## Validation Rules

1. The cantilever support must always have a valid handedness option (left-handed, right-handed, or shared). The "none" option is explicitly excluded.
2. If the support has any undecided options or incomplete data, it will be marked as invalid in the configuration.

## Remarks and Disclaimers

- This documentation is based on the provided class information and may not cover all possible scenarios or configurations.
- The exact behavior of the cantilever support in complex office layouts may depend on additional rules and constraints not visible in the provided code.
- For precise measurements and detailed installation instructions, please refer to the official FIKA Office product documentation.