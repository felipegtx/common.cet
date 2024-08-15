Here's the consolidated document combining the information from both sources:

# FODataMaterialLimb Documentation

This document describes the functionality and behavior of the FODataMaterialLimb class, which is part of the custom.fika.office package. This class extends the DsMaterialLimb class and provides specific functionality for handling material selection in the FIKA Office product line.

## Overview

The FODataMaterialLimb class is responsible for managing material selection and display within the FIKA Office product configuration interface. It provides customized behavior for building the material selection window, setting minimum label widths, and showing material dialogs.

## Part Number Structure

FIKA Office products use a standardized part numbering system to uniquely identify each product and its variations. Understanding this system is crucial for effective product configuration and management.

### Part Number Format

The general format for FIKA Office part numbers is as follows:

```
FIKA-[ProductType]-[Specifications]
```

Where:
- FIKA: The brand identifier, always present at the beginning of the part number.
- ProductType: Indicates the category or type of product.
- Specifications: Additional details about the product, which may include dimensions, features, or variations.

### Product Types and Their Specifications

Here's a breakdown of the main product types and their part number structures:

1. Cabinets (CAB)

```
FIKA-CAB-[Type]-[Width][Depth]
```

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| Type | Cabinet type | BBF (Box/Box/File), FF (File/File), SBOOO (Side-to-Side Box/Open/Open/Open) |
| Width | Width in inches | 15, 18 |
| Depth | Depth in inches | 18, 24, 30 |

Example: FIKA-CAB-BBF-1524 (A Box/Box/File cabinet, 15" wide and 24" deep)

2. Bookshelves (BOOK)

```
FIKA-BOOK[Height]-[Width][Depth]
```

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| Height | Number of shelves | 2, 3, 4, 5 |
| Width | Width in inches | 24, 30, 36, 42 |
| Depth | Depth in inches | 24, 30 |

Example: FIKA-BOOK3-3024 (A bookshelf with 3 shelves, 30" wide and 24" deep)

3. Lateral Files (LAT)

```
FIKA-LAT[Height]-[Width][Depth]
```

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| Height | Number of drawers | 1, 15, 2, 3, 4, 5, 6 |
| Width | Width in inches | 30, 36, 42 |
| Depth | Depth in inches | 18, 24 |

Example: FIKA-LAT3-3618 (A lateral file with 3 drawers, 36" wide and 18" deep)

4. Overhead Cabinets (OVERHEAD)

```
FIKA-OVERHEAD-[Width]14[-OPEN]
```

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| Width | Width in inches | 30, 36, 42, 48, 54, 60 |
| -OPEN | Optional, indicates open shelving | Present or absent |

Example: FIKA-OVERHEAD-3614-OPEN (An open overhead cabinet, 36" wide and 14" high)

5. Worksurfaces (WS)

```
FIKA-WS-[Shape]-[Width][Depth]
```

| Component | Description | Possible Values |
|-----------|-------------|-----------------|
| Shape | Surface shape | RECT (Rectangle), ARC (Arc) |
| Width | Width in inches | Various (18 to 96) |
| Depth | Depth in inches | Various (18 to 96) |

Example: FIKA-WS-RECT-3060 (A rectangular worksurface, 30" wide and 60" deep)

## Functionality

### Window Building

The class overrides the `build` method from its parent class. This method creates and returns the window that displays the material selection interface. It calls the parent class's `build` method, maintaining the basic structure of the window while potentially applying FIKA Office-specific modifications elsewhere.

### Minimum Label Width

The `labelMinWidth` method returns a predefined minimum width for labels in the interface. This width is set to a value stored in the `foLibraryMinInputW` variable, ensuring consistency in the appearance of labels across the FIKA Office material selection interface.

### Material Dialog Display

The `showMaterialDialog` method displays a dialog box for material selection. It takes two parameters:
- `m`: The material to be displayed or selected
- `label`: An optional label for the dialog (if not provided, it uses the default label)

Before calling the parent class's implementation, it sets the label to the result of calling the `label()` method, suggesting that FIKA Office may have a custom way of generating labels for material dialogs.

## Animation Callback

The `foDataTileMatAnimCB` function handles animations related to material selection:

1. Stops all currently running animations
2. Checks if the provided limb is an instance of DsMaterialLimb
3. If so, it creates a new FODataTileMatApplyAnimation with the given limb and material
4. Starts the new animation

This animation provides visual feedback when a user selects a material, enhancing the user experience in the FIKA Office product configurator.

## Conclusion

The FODataMaterialLimb class provides FIKA Office-specific customizations for material selection and display. It maintains most of the functionality from its parent class (DsMaterialLimb) while adding custom behaviors in label generation and animation handling. This class ensures that the material selection interface in FIKA Office products is consistent with the overall design and user experience of the FIKA Office product line, while also integrating seamlessly with the standardized part numbering system used across the product range.