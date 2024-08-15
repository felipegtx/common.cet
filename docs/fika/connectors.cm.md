# Storage Height Manipulator Documentation

## Overview

This document describes the functionality of a Storage Height Manipulator, a tool used to adjust the height of storage units in an office environment. The manipulator is designed to work with various types of storage units, including base storage, panel-hung storage, and other components of the FIKA product line.

## Part Number Structure

The FIKA product line uses a standardized part numbering system to identify different components and configurations. Understanding this system is crucial for proper product configuration. Here's a breakdown of the part number structure:

| Prefix | Product Type | Configuration | Dimensions |
|--------|--------------|---------------|------------|
| FIKA-  | CAB, BOOK, LAT, etc. | BBF, FF, etc. | Width x Depth x Height |

### Example Part Number Breakdown:

Let's take the part number `FIKA-CAB-BBF-1518` as an example:

- `FIKA-`: Standard prefix for all FIKA products
- `CAB`: Indicates a cabinet
- `BBF`: Stands for "Box/Box/File" configuration
- `1518`: Dimensions (15" width, 18" depth)

## Valid Part Numbers

Here's a list of valid part numbers for different FIKA product categories:

### Cabinets (CAB)

- Box/Box/File (BBF): FIKA-CAB-BBF-1518, FIKA-CAB-BBF-1524, FIKA-CAB-BBF-1530, FIKA-CAB-BBF-1818, FIKA-CAB-BBF-1824, FIKA-CAB-BBF-1830
- File/File (FF): FIKA-CAB-FF-1518, FIKA-CAB-FF-1524, FIKA-CAB-FF-1530, FIKA-CAB-FF-1818, FIKA-CAB-FF-1824, FIKA-CAB-FF-1830
- Open Storage (SBOOO): FIKA-CAB-SBOOO-1518, FIKA-CAB-SBOOO-1524, FIKA-CAB-SBOOO-1530, FIKA-CAB-SBOOO-1818, FIKA-CAB-SBOOO-1824, FIKA-CAB-SBOOO-1830

### Bookcases (BOOK)

Available in 2, 3, 4, and 5 shelf configurations:

- FIKA-BOOK2-2424, FIKA-BOOK2-2430, FIKA-BOOK2-3024, FIKA-BOOK2-3030, FIKA-BOOK2-3624, FIKA-BOOK2-3630, FIKA-BOOK2-4224, FIKA-BOOK2-4230
- FIKA-BOOK3-2424, FIKA-BOOK3-2430, FIKA-BOOK3-3024, FIKA-BOOK3-3030, FIKA-BOOK3-3624, FIKA-BOOK3-3630, FIKA-BOOK3-4224, FIKA-BOOK3-4230
- FIKA-BOOK4-2424, FIKA-BOOK4-2430, FIKA-BOOK4-3024, FIKA-BOOK4-3030, FIKA-BOOK4-3624, FIKA-BOOK4-3630, FIKA-BOOK4-4224, FIKA-BOOK4-4230
- FIKA-BOOK5-2424, FIKA-BOOK5-2430, FIKA-BOOK5-3024, FIKA-BOOK5-3030, FIKA-BOOK5-3624, FIKA-BOOK5-3630, FIKA-BOOK5-4224, FIKA-BOOK5-4230

### Lateral Files (LAT)

Available in 1, 1.5, 2, 3, 4, 5, and 6 drawer configurations:

- FIKA-LAT1-3018, FIKA-LAT1-3024, FIKA-LAT1-3618, FIKA-LAT1-3624, FIKA-LAT1-4218, FIKA-LAT1-4224
- FIKA-LAT15-3018, FIKA-LAT15-3024, FIKA-LAT15-3618, FIKA-LAT15-3624, FIKA-LAT15-4218, FIKA-LAT15-4224
- FIKA-LAT2-3018, FIKA-LAT2-3024, FIKA-LAT2-3618, FIKA-LAT2-3624, FIKA-LAT2-4218, FIKA-LAT2-4224
- FIKA-LAT3-3018, FIKA-LAT3-3024, FIKA-LAT3-3618, FIKA-LAT3-3624, FIKA-LAT3-4218, FIKA-LAT3-4224
- FIKA-LAT4-3018, FIKA-LAT4-3024, FIKA-LAT4-3618, FIKA-LAT4-3624, FIKA-LAT4-4218, FIKA-LAT4-4224
- FIKA-LAT5-3018, FIKA-LAT5-3024, FIKA-LAT5-3618, FIKA-LAT5-3624, FIKA-LAT5-4218, FIKA-LAT5-4224
- FIKA-LAT6-3018, FIKA-LAT6-3024, FIKA-LAT6-3618, FIKA-LAT6-3624, FIKA-LAT6-4218, FIKA-LAT6-4224

## Position Calculation

The manipulator's position is calculated differently depending on the type of storage unit it's attached to:

1. For Base Storage (e.g., FIKA-CAB-*, FIKA-LAT-*):
   - The manipulator is positioned at the center of the storage unit's width and depth.
   - The height of the manipulator is set to the full height of the storage unit.

2. For Panel-Hung Storage (e.g., FIKA-OVERHEAD-*):
   - The manipulator is positioned at the center of the storage unit's width and depth.
   - The height of the manipulator is set to the sum of the storage unit's height and its elevation from the ground.

If the manipulator is not attached to either type of storage, it will be positioned at the origin point (0, 0, 0).

## Orientation

The manipulator is always oriented in a specific way:
- It has no rotation around the vertical axis.
- It is rotated 90 degrees around the horizontal axis that runs from front to back.
- It has no rotation around the horizontal axis that runs from side to side.

This orientation ensures that the manipulator is always facing the correct direction for easy interaction.

## Appearance

The manipulator can appear in two styles:

1. Standard Style: Used when the storage unit cannot be resized (e.g., FIKA-CAB-BBF-*, FIKA-LAT-*).
2. Arrow Style: Used when the storage unit can be resized (stretchable) (e.g., FIKA-BOOK-*, FIKA-OVERHEAD-*).

The arrow style provides a visual cue to users that they can adjust the height of the storage unit.

## Interaction

Users can interact with the manipulator to adjust the height of the storage unit. The exact interaction method and constraints may vary depending on the specific type of storage unit and any additional rules set by the system.

## Remarks and Disclaimers

- The exact dimensions and size constraints for each storage unit are defined by their respective part numbers.
- Height adjustment capabilities may vary between different product types and configurations.
- Always refer to the specific product documentation for detailed information on size ranges and adjustment limitations.
- The actual resizing behavior when interacting with the manipulator may be subject to system-wide rules and constraints not covered in this document.
- There are no explicit invalidation rules or constraints mentioned in the provided information. These might be implemented in other parts of the system or in a separate validation system.