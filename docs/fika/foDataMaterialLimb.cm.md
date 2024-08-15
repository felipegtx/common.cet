Since there is no information provided in the Part Numbers document, and we are instructed to prefer that document when in doubt about Part Numbers, I will create a consolidated document based solely on the Configuration Logic document. Here's the consolidated documentation:

# FODataMaterialLimb Documentation

This document describes the functionality and behavior of the FODataMaterialLimb class, which is part of the custom.fika.office package. This class extends the DsMaterialLimb class and provides specific functionality for handling materials in the FIKA Office product line.

## Overview

The FODataMaterialLimb class manages material selection and display within the FIKA Office product configuration interface. It provides customized behavior for building the user interface, setting minimum label widths, and showing material dialogs.

## Functionality

### User Interface Building

The class overrides the `build` method to create the user interface for material selection. It uses the default implementation from its parent class (DsMaterialLimb) to construct the interface.

### Minimum Label Width

The `labelMinWidth` method returns a predefined minimum width for labels in the interface, ensuring consistency in the layout of material selection controls.

### Material Dialog Display

The `showMaterialDialog` method displays a dialog for material selection. It uses the class's label as the dialog title if no specific label is provided.

## Material Application Animation

The `foDataTileMatAnimCB` function handles the animation when applying a material:

1. It aborts any ongoing animations.
2. If the provided limb is an instance of DsMaterialLimb (which includes FODataMaterialLimb), it creates and starts a new animation (FODataTileMatApplyAnimation) to visually apply the selected material.

## Usage in Product Configuration

This class is used in the following scenarios within the FIKA Office product configuration:

1. Displaying available materials for office furniture or components.
2. Allowing users to select and preview different materials on office products.
3. Animating the application of selected materials for a more interactive and visually appealing user experience.

## Interaction with Other Components

The FODataMaterialLimb class interacts with:

1. The parent DsMaterialLimb class, inheriting and extending its functionality.
2. The Material class, which likely represents the actual material data.
3. The FODataTileMatApplyAnimation class, which handles the visual animation of applying materials.

## Constraints and Limitations

The class is designed specifically for the FIKA Office product line and may not be suitable for use in other contexts without modification.

---

For more detailed information about specific methods or behaviors, additional code or context would be necessary.