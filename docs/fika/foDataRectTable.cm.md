Based on the two documents provided, I've consolidated the information into a single, clear, and concise document that focuses on the FIKA Rectangular Table's part number structure and configuration logic. Here's the consolidated documentation in markdown format:

# FIKA Rectangular Table Documentation

This document describes the configuration logic and part number structure for the FIKA Rectangular Table, a freestanding table product.

## Part Number Structure

The part number for the FIKA Rectangular Table follows this structure:

```
FIKA-TBL-FSRECT-WWDD
```

Where:
- `FIKA`: Brand identifier
- `TBL`: Product type (Table)
- `FSRECT`: Table style (Freestanding Rectangular)
- `WW`: Width in inches
- `DD`: Depth in inches

### Valid Part Numbers

Here's a table of all valid part numbers for the FIKA Rectangular Table:

| Part Number | Width (inches) | Depth (inches) |
|-------------|----------------|----------------|
| FIKA-TBL-FSRECT-3636 | 36 | 36 |
| FIKA-TBL-FSRECT-3642 | 36 | 42 |
| FIKA-TBL-FSRECT-4236 | 42 | 36 |
| FIKA-TBL-FSRECT-4242 | 42 | 42 |
| FIKA-TBL-FSRECT-4836 | 48 | 36 |
| FIKA-TBL-FSRECT-4842 | 48 | 42 |
| FIKA-TBL-FSRECT-5436 | 54 | 36 |
| FIKA-TBL-FSRECT-5442 | 54 | 42 |
| FIKA-TBL-FSRECT-6036 | 60 | 36 |
| FIKA-TBL-FSRECT-6042 | 60 | 42 |
| FIKA-TBL-FSRECT-6636 | 66 | 36 |
| FIKA-TBL-FSRECT-6642 | 66 | 42 |
| FIKA-TBL-FSRECT-7236 | 72 | 36 |
| FIKA-TBL-FSRECT-7242 | 72 | 42 |
| FIKA-TBL-FSRECT-7836 | 78 | 36 |
| FIKA-TBL-FSRECT-7842 | 78 | 42 |
| FIKA-TBL-FSRECT-8436 | 84 | 36 |
| FIKA-TBL-FSRECT-8442 | 84 | 42 |

## Dimensions and Size Constraints

1. **Width**: 
   - Range: 36 inches to 84 inches
   - Increments: 6 inches
   - Available sizes: 36", 42", 48", 54", 60", 66", 72", 78", 84"

2. **Depth**: 
   - Available sizes: 36 inches or 42 inches

## Table Shape and Features

- Rectangular shape with rounded corners (2-inch radius)
- Four sides: front, back, left, and right

## Base Types and Support

The table can have two types of bases, determined by the table width:

1. **Post Legs**: 
   - For tables with width up to 54 inches
   - Four legs positioned near the corners

2. **X-Base**: 
   - For tables with width greater than 54 inches
   - One central X-base (for tables up to 54 inches wide)
   - Two X-bases (for tables wider than 54 inches)

### Post Leg Positions

When using post legs, they are positioned slightly inset from the corners:
- Lower Left
- Lower Right
- Upper Right
- Upper Left

### X-Base Positions

For X-base support:
- Tables up to 54 inches wide: One central X-base
- Tables wider than 54 inches: Two X-bases, positioned at 1/4 and 3/4 of the table width

## Configuration Rules and Constraints

1. Width must be selected before depth
2. Changing base type recalculates support locations
3. Multiple chair placements are allowed
4. Edge stretching affects adjacent edges:
   - Stretching left/right affects back edge
   - Stretching front affects left and right sides

## Material and Finish Options

The table has three main components for material selection:
1. Surface material (tabletop)
2. Edge material
3. Base material (including painted metal options)

Specific material and finish options should be documented separately as part of the product's configuration logic.

## Remarks

- The table height is not specified in the part number and should be documented separately
- Material and finish selections are not reflected in the part number
- The base type (Post Legs or X-Base) is determined by the table width and is not explicitly coded in the part number

This consolidated documentation provides a clear and concise explanation of the FIKA Rectangular Table's part number structure, valid configurations, and key features. It should be easily understood by Interior Designers, focusing on the product configuration logic and part number structure.