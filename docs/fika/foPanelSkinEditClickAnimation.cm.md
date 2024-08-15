Since there is no information provided in the "Part Numbers" document, and we are instructed not to add any new information, the consolidated document will be based entirely on the "Configuration Logic" document. Here's the consolidated version:

# Panel Skin Edit Click Animation Documentation

This document describes the functionality of the Panel Skin Edit Click Animation, which is used to modify panel skins in an office environment.

## Overview

The Panel Skin Edit Click Animation allows users to interact with panel skins, enabling them to split, merge, and stretch panels. This functionality is crucial for customizing office layouts and configurations.

## Key Features

1. **Toggle Connection**: This feature allows users to split or merge panel skins.
2. **Stretch Animation**: Users can stretch panel skins to adjust their size.

## Detailed Functionality

### Toggle Connection

When a user clicks on a panel skin:

1. The system begins recording the action for undo functionality.
2. The system checks if the click is on the upper or lower half of the panel:
   - If on the lower half, it prepares for a merge action.
   - If on the upper half, it prepares for a split action.
3. The system identifies the exact item (section of the panel) that was clicked.
4. Depending on whether it's a split or merge action:
   - For a split: The system divides the selected item into two separate items.
   - For a merge: The system combines the selected item with the item above it.
5. The action is then recorded and can be undone if needed.

### Stretch Animation

When a user initiates a stretch action:

1. The system creates a new stretch animation environment.
2. It keeps track of which item (section of the panel) is being stretched.
3. As the user drags to stretch:
   - The system continuously calculates the new position.
   - It updates the size of the selected item in real-time.
   - The panel skin is redrawn to reflect the changes.
4. Once the user releases the mouse, the final position is set, and the stretch action is completed.

## User Interaction

1. To split a panel: Click on the upper half of a panel section.
2. To merge panels: Click on the lower half of a panel section.
3. To stretch a panel: Click and drag on the lower half of a panel section.

## Important Notes

- All actions (split, merge, stretch) can be undone using the system's undo functionality.
- The system ensures that only valid splits and merges are allowed based on the panel's configuration.
- The stretch functionality may be limited by the overall panel size and neighboring panels.

## Limitations

- The exact rules for allowed splits, merges, and stretches are determined by the underlying panel skin configuration and are not detailed in this class.
- The visual representation of the split and merge actions is handled by other parts of the system and is not defined here.

---

This documentation provides an overview of the Panel Skin Edit Click Animation functionality. For more detailed information about specific panel configurations or visual representations, please refer to the related documentation on panel skins and office layouts.