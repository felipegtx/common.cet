# FIKA Product Line Documentation

## Overview

This document provides comprehensive information about the FIKA product line, including part number structure, product categories, and configuration logic. It is designed to assist Interior Designers in effectively configuring and ordering products without requiring programming knowledge.

## Part Number Structure

FIKA part numbers follow a consistent structure that provides information about the product type, dimensions, and specific features. The general format is:

```
FIKA-[Product Type]-[Specifications]-[Dimensions]
```

Components:
1. **FIKA**: Prefix consistent across all products in the FIKA line.
2. **Product Type**: Indicates the category of the product.
3. **Specifications**: Additional details about the product's features or configuration.
4. **Dimensions**: The size of the product, typically in inches.

## Product Categories

### Cabinets (CAB)

```
FIKA-CAB-[Type]-[Width][Depth]
```

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| Type | Cabinet configuration | BBF (Box/Box/File), FF (File/File), SBOOO (Single Box, Open/Open/Open) |
| Width | Cabinet width in inches | 15, 18 |
| Depth | Cabinet depth in inches | 18, 24, 30 |

Example: `FIKA-CAB-BBF-1524` (Box/Box/File cabinet, 15" wide, 24" deep)

### Workstations (WS)

```
FIKA-WS-[Shape]-[Width][Depth]
```

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| Shape | Workstation shape | RECT (Rectangle), ARC (Arc) |
| Width | Workstation width in inches | 18, 24, 30, 36, etc. |
| Depth | Workstation depth in inches | 18, 24, 30, 36, etc. |

Example: `FIKA-WS-RECT-3060` (Rectangular workstation, 30" wide, 60" deep)

### Bookcases (BOOK)

```
FIKA-BOOK[Height]-[Width][Depth]
```

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| Height | Number of shelves | 2, 3, 4, 5 |
| Width | Bookcase width in inches | 24, 30, 36, 42 |
| Depth | Bookcase depth in inches | 24, 30 |

Example: `FIKA-BOOK3-3024` (Bookcase with 3 shelves, 30" wide, 24" deep)

### Lateral Files (LAT)

```
FIKA-LAT[Drawers]-[Width][Height]
```

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| Drawers | Number of drawers | 1, 15, 2, 3, 4, 5, 6 |
| Width | Lateral file width in inches | 30, 36, 42 |
| Height | Lateral file height in inches | 18, 24 |

Example: `FIKA-LAT3-3624` (3-drawer lateral file, 36" wide, 24" high)

### Additional Product Categories

The FIKA product line includes several other categories, each with its own part number logic:

- Overhead storage (OVERHEAD)
- Tables (TBL)
- Pedestals (PF)
- Tiles (TILE)
- Shelves (SHELF)
- Towers (TOWER)

Each category follows a similar logic to the examples provided above, with specific components indicating the product's unique features and dimensions.

## Configuration Logic

### FOItemTag

The FOItemTag class is responsible for creating and managing dynamic item tags in an office setting.

Key Features:
- Tag Creation: Creates new item tags based on provided information, position, and rotation.
- Flexibility: Tags can be placed at any specified position in the 3D space of the office layout.
- Customizable Rotation: Tags can be rotated to any angle for flexible placement and readability.
- Unique Identification: Each tag can be assigned a unique key for easy reference and management.

### FOItemTagInfo

The FOItemTagInfo class contains detailed information for an office item tag.

Key Features:
- Text Style: Provides a custom text style for the tag's visual appearance.
- Tag Content: Stores the text content of the tag, typically describing or identifying the associated office item.
- Layer Information: Incorporates layer information for organizing and displaying tags in complex office layouts.

### Tag Behavior and Rules

1. Text Height: Default text height is 4 inches, but can be customized.
2. Layer Management: Tags are associated with specific layers, controlling visibility in the office layout.
3. Export Functionality: Tags can be exported with attributes including position, rotation, font height, and color.
4. Visibility Rules: Tag visibility is controlled by view mode, layer settings, and content filters.
5. Attribute Assignment: Exported tags are assigned various attributes such as prompt, text content, name, position, rotation, font height, and color.
6. Color Management: Tag text color is determined by either a custom text style or a predefined color associated with the tag's layer.

## Conclusion

Understanding the FIKA part number system and configuration logic allows Interior Designers to efficiently identify, specify, and manage products across the entire FIKA line. When ordering or configuring FIKA products, always use the complete and correct part number to avoid confusion or errors in the procurement process.

The FOItemTag and FOItemTagInfo classes provide a flexible system for creating and managing item tags within office layouts, enhancing the ability to organize and identify FIKA products in complex design scenarios.