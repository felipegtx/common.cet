# FODataPicklist Documentation

This document describes the functionality and behavior of the FODataPicklist, a specialized picklist for the FIKA Office product line.

## Overview

The FODataPicklist is a customized version of a standard picklist, designed specifically for use with FIKA Office products. It provides a user interface for selecting and managing product data within the configuration system.

## Key Features

1. **User Interface**: The picklist uses a gray border color, which helps it stand out from other elements in the interface.

2. **Catalog Browser Integration**: When interacting with the picklist, it can open a specialized catalog browser or a custom dialog, depending on the context.

3. **Data Management**: The picklist is capable of handling and displaying product data, allowing users to select and manage items within the FIKA Office product line.

## Part Number Structure

FIKA Office products use a standardized part numbering system. Understanding this system is crucial for effective use of the FODataPicklist. Here's a breakdown of the part number structure:

| Component | Description | Format | Example |
|-----------|-------------|--------|---------|
| Prefix    | Product line identifier | FIKA- | FIKA- |
| Product Type | Indicates the type of product | 2-5 letter code | CAB-, WS-, TBL- |
| Subtype   | Further specifies the product | 0-4 letter code | BBF-, RECT-, ARC- |
| Dimensions | Product dimensions | 2-8 digit code | 1518, 3636, 24424224 |
| Orientation | (Optional) Left/Right orientation | -L or -R | -L, -R |

### Example Part Numbers

1. `FIKA-CAB-BBF-1518`: A FIKA cabinet with box/box/file configuration, 15" wide and 18" deep.
2. `FIKA-WS-RECT-2430`: A FIKA rectangular workstation, 24" wide and 30" deep.
3. `FIKA-TOWER-4BBF-1524-L`: A FIKA tower with 4 box/box/file drawers, 15" wide, 24" deep, left-oriented.

## Valid Part Number Ranges

The FODataPicklist supports various product types within the FIKA Office line. Here are some key product categories and their part number patterns:

1. **Cabinets (CAB)**: 
   - Format: FIKA-CAB-[BBF/FF/SBOOO]-[width][depth]
   - Width: 15, 18
   - Depth: 18, 24, 30

2. **Workstations (WS)**:
   - Format: FIKA-WS-[RECT/ARC]-[width][depth]
   - Width: 18 to 36 (in 6" increments)
   - Depth: 18 to 96 (in 6" increments)

3. **Tables (TBL)**:
   - Format: FIKA-TBL-FSRECT-[width][depth] or FIKA-TBL-FSROUND-[diameter]
   - Rectangular: Width 36 to 84, Depth 36 or 42
   - Round: Diameter 30, 36, 42, 48, 54

4. **Towers**:
   - Format: FIKA-TOWER-[configuration]-[width][depth]-[L/R]
   - Configuration: 4BBF, 4FF, 5BBF, 5FF, 6BBF, 6FF
   - Width: 15
   - Depth: 18, 24, 30
   - Orientation: L (Left), R (Right)

## Behavior and Functionality

### Visibility Rules

The picklist has specific rules for when certain properties are visible:

1. If the picklist contains product data:
   - The "name" property will not be visible.
   - All other properties will be visible.

2. If the picklist does not contain product data:
   - The "name" property will be visible.
   - All other properties will not be visible.

These rules ensure that users only see relevant information based on the current state of the picklist.

### Catalog Browser Interaction

When a user interacts with the picklist to view more details:

1. If the picklist is using the default key:
   - A specialized FODataPicklist dialog will be shown.
   - The picklist editor will be ensured to be visible.

2. For all other cases:
   - A standard extendable catalog browser will be opened.

This behavior allows for a more tailored experience when working with default FIKA Office data, while still providing flexibility for custom or extended data sets.

## User Interaction

Users can interact with the FODataPicklist to:

1. View available FIKA Office products.
2. Select products for configuration.
3. Access detailed product information through the catalog browser or custom dialog.

When selecting a product, users should pay attention to the part number structure to ensure they are choosing the correct item for their needs.

---

This documentation provides an overview of the FODataPicklist's functionality and behavior, focusing on its role in managing FIKA Office product data and user interactions. The inclusion of part number structure and valid ranges will help users better understand the product selection process and the logic behind the FIKA Office product line, while the behavior and functionality details ensure proper usage of the picklist within the configuration system.