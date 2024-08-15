Since there is no information provided in the Part Numbers document, I will consolidate the information from the Configuration Logic document into a clear and concise final document. Here's the consolidated documentation:

# FODataDimensionVessel Documentation

This document describes the functionality and behavior of the FODataDimensionVessel, which displays dimension information for office furniture objects.

## Overview

The FODataDimensionVessel is a specialized vessel that shows dimension information for office furniture objects in both 2D and 3D views. It provides visual feedback about the size of furniture items.

## Key Features

1. Dimension Display: Shows furniture object dimensions in 2D and 3D views.
2. Automatic Updates: Updates display when changes occur in the animation.
3. Flexible Positioning: Adapts position based on the attached object and current view.

## Behavior and Functionality

### Initialization

The vessel requires:
- A unique key
- A dimension property key (dimPropKey) specifying which object dimension to display

### Update Mechanism

Automatically updates when:
- Part of a CoreAnimation
- The animation is invalidated

### 3D Representation

- Displays text representation of the dimension
- Text positioned relative to the object's center
- Text orientation adjusts based on camera angle

### 2D Representation

- Shows text label with dimension value
- Label positioned to the left of the object's center
- Text size adapts based on current view scale

### Dimension Calculation

Retrieves dimension value from the attached object using the specified dimPropKey and converts it to a readable string format.

## Interaction with Other Objects

- Typically attached to a furniture object (its owner)
- Can adapt to work with the main selected object in animation contexts

## Visibility and Display Rules

- Only visible when there's a valid dimension value to display
- 3D view: Text always faces the camera
- 2D view: Text size adjusts based on view scale

## Limitations and Considerations

- Relies on the owner object having the specified dimension property
- 3D representation may be affected by complex camera angles or object positions

This documentation provides an overview of the FODataDimensionVessel's functionality, focusing on its behavior and interaction with furniture objects to display dimension information in 2D and 3D environments.