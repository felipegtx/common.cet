# FIKA Rectangular Table Documentation

This document describes the configuration logic and part number structure for the FIKA Rectangular Table, a freestanding table product.

## Dimensions and Size Constraints

The FIKA Rectangular Table has two main dimensions:

1. **Width**: 
   - Range: 36 inches to 84 inches
   - Increments: 6 inches
   - Available sizes: 36", 42", 48", 54", 60", 66", 72", 78", 84"

2. **Depth**: 
   - Available sizes: 36 inches or 42 inches

## Part Number Structure

The part number for the FIKA Rectangular Table follows this structure:

```
FIKA-TBL-FSRECT-[WIDTH][DEPTH]
```

Where:
- FIKA: Brand identifier
- TBL: Indicates it's a table
- FSRECT: Stands for Freestanding Rectangular
- [WIDTH]: Two-digit width in inches
- [DEPTH]: Two-digit depth in inches

Example: FIKA-TBL-FSRECT-3636 represents a 36" wide by 36" deep table.

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| FIKA      | Brand identifier | Always "FIKA" |
| TBL       | Product type | Always "TBL" for tables |
| FSRECT    | Table shape | Always "FSRECT" for freestanding rectangular |
| [WIDTH]   | Table width in inches | 36, 42, 48, 54, 60, 66, 72, 78, 84 |
| [DEPTH]   | Table depth in inches | 36, 42 |

## Valid Part Numbers

Based on the available dimensions, here's a list of all valid part numbers for the FIKA Rectangular Table:

- FIKA-TBL-FSRECT-3636
- FIKA-TBL-FSRECT-3642
- FIKA-TBL-FSRECT-4236
- FIKA-TBL-FSRECT-4242
- FIKA-TBL-FSRECT-4836
- FIKA-TBL-FSRECT-4842
- FIKA-TBL-FSRECT-5436
- FIKA-TBL-FSRECT-5442
- FIKA-TBL-FSRECT-6036
- FIKA-TBL-FSRECT-6042
- FIKA-TBL-FSRECT-6636
- FIKA-TBL-FSRECT-6642
- FIKA-TBL-FSRECT-7236
- FIKA-TBL-FSRECT-7242
- FIKA-TBL-FSRECT-7836
- FIKA-TBL-FSRECT-7842
- FIKA-TBL-FSRECT-8436
- FIKA-TBL-FSRECT-8442

## Table Shape and Features

- The table has a rectangular shape with rounded corners.
- The corner radius is 2 inches.
- The table surface has four edges: front, back, left side, and right side.

## Base Types and Support

The table can have two types of bases:

1. **X-Base**:
   - Used when the table width is 54 inches or less.
   - Single center support for smaller tables.
   - Dual support (left and right center) for tables wider than 54 inches.

2. **Post Legs**:
   - Used when the table width is greater than 54 inches.
   - Four legs positioned near the corners of the table.

The system automatically determines the appropriate base type and support configuration based on the table's width.

## Customization and Interaction Rules

1. **Width Adjustment**: 
   - The width can be changed by adjusting the left or right side of the table.
   - When stretching the width, the back edge of the table moves.

2. **Depth Adjustment**: 
   - The depth can be changed by adjusting the front edge of the table.
   - When stretching the depth, both left and right sides of the table move.

3. **Material Selection**:
   - Users can select materials for the table top and edge.
   - Base material and metal paint options are available for customization.

4. **Chair Placement**:
   - The table allows for multiple chair placements around it.

## Additional Notes

- The table is designed to work with a snapping system for precise placement and alignment.
- The table is categorized under office furniture, specifically in the tables and table support categories.
- The surface material is referenced as "A-FURN-TBFS-TPXX" in the system.

## Remarks and Disclaimers

- The exact material options and color choices are not specified in the provided information.
- Specific rules for interaction with other furniture pieces are not detailed in the provided information.

This documentation provides an overview of the FIKA Rectangular Table's configuration logic and part number structure. For more detailed information or specific queries, please consult with the development team.