Based on the provided documents, I will consolidate the information into a single, clear, and concise document. Since there is no information in the Part Numbers document, the consolidated document will be based entirely on the Configuration Logic document.

# FODataWorksurfaceDepthStretchAnimationG2 Documentation

This document describes the functionality and behavior of the FODataWorksurfaceDepthStretchAnimationG2, which manages the depth stretching of worksurfaces in a group.

## Overview

The FODataWorksurfaceDepthStretchAnimationG2 handles the stretching of worksurface depths, particularly for straight back worksurfaces. It allows for group stretching, where multiple worksurfaces can be adjusted simultaneously.

## Group Depth Stretch Functionality

### Enabling Group Depth Stretch

The system provides an option to enable or disable group depth stretching. When enabled, it allows multiple worksurfaces to be stretched together.

### Behavior When Group Depth Stretch is Enabled

1. When the main worksurface's depth changes, all worksurfaces in the group adjust to match the new depth.
2. The system tracks the original depths of all worksurfaces in the group.
3. "Super Stretch" feature and gap length adjustment are disabled during group depth stretch.

### Behavior When Group Depth Stretch is Disabled

1. Each worksurface can be adjusted independently.
2. All worksurfaces in the group revert to their original depths.
3. "Super Stretch" feature and gap length adjustment become available again.

## Worksurface Selection for Group Stretching

The system automatically identifies worksurfaces for group stretching:

1. It identifies the main worksurface (must be a straight back worksurface).
2. It finds other inline rectangular surfaces connected to the main worksurface.
3. These connected surfaces are added to the group for stretching.

## Depth Adjustment Process

When the main worksurface's depth changes and group stretching is enabled:

1. The new depth applies to all worksurfaces in the group.
2. The system updates each worksurface's dimensions.
3. Connectors on the worksurfaces are realigned to maintain proper connections.

## Reverting Group Stretch

When group stretching is disabled:

1. The system retrieves the original depth for each worksurface in the group.
2. It sets each worksurface back to its original depth.
3. The dimensions of each worksurface are updated.
4. Connectors on the worksurfaces are realigned.

## Additional Notes

- The system tracks original depths of worksurfaces for accurate reverting.
- Group depth stretch is designed for straight back worksurfaces and may not apply to other surface types.
- "Super Stretch" is disabled during group depth stretch to avoid conflicts.

## Remarks and Disclaimers

- This documentation is based on provided class information and may not cover all scenarios or edge cases.
- Exact dimensions and constraints for worksurfaces are not specified and may depend on other system parts.
- Part number logic for worksurfaces is not present in the provided information and is likely handled in a different part of the system.