Based on the provided documents, I'll consolidate the information into a single, clear, and concise document that focuses on both the part numbering system and the configuration logic for Fika Office products. Here's the consolidated documentation:

# Fika Office Product Configuration Documentation

## Overview

This document provides comprehensive information on the Fika Office product line, including the part numbering system and configuration logic. It is designed to assist Interior Designers in understanding and using Fika Office products effectively.

## Part Numbers

Fika Office uses a standardized part numbering system that provides essential information about each component. The general format is:

```
FIKA-[ProductType]-[Specifications]
```

### Product Types and Their Part Numbers

#### 1. Cabinets (CAB)

| Product Type | Description | Format | Example |
|--------------|-------------|--------|---------|
| BBF | Box/Box/File | FIKA-CAB-BBF-[Width][Depth] | FIKA-CAB-BBF-1518 |
| FF | File/File | FIKA-CAB-FF-[Width][Depth] | FIKA-CAB-FF-1524 |
| SBOOO | Single Box, Open Open Open | FIKA-CAB-SBOOO-[Width][Depth] | FIKA-CAB-SBOOO-1530 |

Available sizes: 15"x18", 15"x24", 15"x30", 18"x18", 18"x24", 18"x30"

#### 2. Bookcases (BOOK)

Format: FIKA-BOOK[Height]-[Width][Depth]
Example: FIKA-BOOK2-2424

Heights: 2, 3, 4, 5 (shelves)
Widths: 24", 30", 36", 42"
Depths: 24", 30"

#### 3. Lateral Files (LAT)

Format: FIKA-LAT[Height]-[Width][Depth]
Example: FIKA-LAT1-3018

Heights: 1, 1.5, 2, 3, 4, 5, 6 (drawers)
Widths: 30", 36", 42"
Depths: 18", 24"

#### 4. Overhead Cabinets (OVERHEAD)

Format: FIKA-OVERHEAD-[Width]14 or FIKA-OVERHEAD-[Width]14-OPEN
Example: FIKA-OVERHEAD-3014 or FIKA-OVERHEAD-3014-OPEN

Widths: 30", 36", 42", 48", 54", 60"

#### 5. Worksurfaces (WS)

| Product Type | Format | Example |
|--------------|--------|---------|
| Rectangular | FIKA-WS-RECT-[Width][Depth] | FIKA-WS-RECT-1818 |
| Arc | FIKA-WS-ARC-[Width][Depth] | FIKA-WS-ARC-2418 |
| 120° | FIKA-WS-120-[Depth][Width][Depth][Width][Depth] | FIKA-WS-120-18363618 |
| 90° | FIKA-WS-90-[Depth][Width][Depth][Width] | FIKA-WS-90-18363618 |

Widths: 18" to 96" (in 6" increments)
Depths: 18" to 36" (in 6" increments)

#### 6. Support Components

| Product Type | Format | Example |
|--------------|--------|---------|
| Cantilever | FIKA-CANTILEVER-[Type] | FIKA-CANTILEVER-DBL |
| End Panels | FIKA-PF-[Width][Depth] | FIKA-PF-2430 |

Cantilever Types: DBL (Double), LH (Left Hand), RH (Right Hand)
End Panel Widths: 24" to 60" (in 6" increments)
End Panel Depths: 30" to 66" (in 6" increments)

#### 7. Storage Towers

Format: FIKA-TOWER-[Config]-[Width][Depth]-[Hand]
Example: FIKA-TOWER-4BBF-1518-L

Configurations: 4BBF, 4FF, 5BBF, 5FF, 6BBF, 6FF
Widths: 15"
Depths: 18", 24", 30"
Handedness: L (Left), R (Right)

#### 8. Accessories

| Product Type | Format | Example |
|--------------|--------|---------|
| Shelves | FIKA-SHELF-[Width]09 | FIKA-SHELF-2409 |
| Tiles | FIKA-TILE-[Width][Height] | FIKA-TILE-2406 |

Shelf Widths: 24", 30", 36", 42", 48", 54", 60"
Tile Widths: 24" to 60" (in 6" increments)
Tile Heights: 6" to 60" (in 6" increments)

## Configuration Logic

### Product Categorization

1. Old Fika Office products (versions 0.0.0 to 12.0.6):
   - Now categorized under "Legacy"
   - Related reports moved to legacy reports category
   - "FOArticlePartColumn" renamed to "FikaArticlePartColumn" and moved to a different category

2. Data Fika Office products (version 12.0.6 or earlier):
   - Now categorized under main "Fika Office" category
   - Junction products renamed:
     - "FOEJunction" to "FODataEJunction"
     - "FOIJunction" to "FODataIJunction"
     - "FOLJunction" to "FODataLJunction"
     - "FOVJunction" to "FODataVJunction"
     - "FOTJunction" to "FODataTJunction"
     - "FOYJunction" to "FODataYJunction"
     - "FOXJunction" to "FODataXJunction"
   - "foHandedness" feature renamed to "foSupportHandedness"
   - Related reports moved to main reports category

### Configuration Rules

1. The system tracks which products have been updated to the new naming and categorization system.
2. Products already updated will not be changed again.
3. Renaming and recategorization process is automatic when products are accessed in the system.

## Important Notes for Interior Designers

1. All measurements in part numbers are in inches.
2. Always use the full part number when ordering to ensure accuracy.
3. Some product types may have additional options not covered in this guide. Consult the full product catalog for comprehensive information.
4. Custom sizes or configurations may be available upon request but will have different part number formats.
5. When searching for older Fika Office products, look in the "Legacy" categories.
6. Junction products now have "Data" in their names, which may affect how they are searched for or referenced.
7. For product handedness, look for "Support Handedness" instead of just "Handedness".
8. Reports for both old and new products are now consolidated in the main reports category.

## Disclaimers

- This document focuses on part numbering and product categorization. It does not provide detailed information about specific product dimensions or configuration rules beyond naming and categorization.
- The exact behavior of products after renaming and recategorization is not specified. Verify product functionality after these changes.
- Exercise caution when working with older configurations that might reference previous product names or categories.