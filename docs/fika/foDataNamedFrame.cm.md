# FODataNamedFrame Documentation

This document describes the functionality and behavior of the FODataNamedFrame class, a specialized panel frame used in office furniture configurations.

## Overview

The FODataNamedFrame is an extension of the AODataSkinFrame class, designed to represent a named panel frame in an office furniture system. It includes features for managing frame types, updating panel names, and handling various aspects of the panel's behavior within a space.

## Key Features

1. Frame Type Management
2. Panel Naming
3. Height and Width Handling
4. Property Management
5. Space Interaction

## Detailed Functionality

### Frame Type Management

- Each frame has a unique `frameTypeId` that identifies its type.
- The `frameName` is derived from the `frameTypeId` and corresponds to a predefined list of frame names.

### Panel Naming

- The panel name is automatically updated when certain conditions change, such as height or frame type.
- The `updatePanelName` function ensures that the panel name remains consistent with its properties and the space it occupies.

### Height and Width Handling

- When the height of the panel changes, the `heightChanged` function is called, triggering an update to the panel name.
- The panel's dimensions are used in the `mainTagText` function to create a descriptive tag for the panel (e.g., "Frame Name - Width/Height").

### Property Management

- The class handles various properties and responds to property changes.
- When animation properties change, it updates internal values and may adjust the height to the closest valid value.

### Space Interaction

- The panel interacts with its containing space and other panels in the space.
- It can determine if it's the last panel of its type in the space using the `lastInSpace` function.
- The panel can update its type and appearance based on the space it's in and the other panels present.

## Part Number Logic

The part number logic is not explicitly defined in this class. However, the `frameKey` function suggests that the part number might be constructed using the following components:

1. A prefix "FO"
2. The panel height
3. Information from the upper skin (if present)
4. Information from the lower skin (if present)

For example, a part number might look like: "FO72UPSK01DWSK02" (where 72 is the height in inches, UPSK01 is an upper skin code, and DWSK02 is a lower skin code).

## Dimensions

The class uses the following dimension-related functions:

- `w` for width
- `h` for height
- `d` for depth (inherited from parent classes)

The dimensions are likely defined in the parent classes or determined by the specific product configuration.

## Interaction Rules

1. The panel can be part of a group of panels in a space.
2. It interacts with a panel manager dialog when in development mode.
3. The panel can be connected to other panels using junction snappers.
4. It responds to animation events and property changes.

## Invalidation Rules

The panel's appearance and properties are invalidated (marked for update) when:

1. The panel name is updated
2. The frame type changes
3. The height changes
4. Certain properties that start with "cAOMultiDataPK" are modified

## Additional Notes

- The class uses a baptism system for managing panel types within a world or space.
- It has special behaviors when suspended or unsuspended, particularly in development mode.
- The class creates custom junction connections and snappers specific to this type of panel.

This documentation provides an overview of the FODataNamedFrame class's functionality. For more specific details about valid part numbers, dimensions, or product-specific rules, additional information from related classes or product specifications would be needed.