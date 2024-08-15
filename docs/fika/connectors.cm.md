Based on the provided documents, here's the consolidated documentation:

# Storage Height Manipulator Documentation

## Overview

This document describes the functionality of a height manipulator for storage units in the FIKA Office product line. The manipulator is designed to work with two types of storage units: base storage and panel-hung storage.

## Position Logic

The manipulator's position is determined based on the type of storage unit it's associated with:

1. For Base Storage:
   - The manipulator is positioned at the center of the storage unit's width and depth.
   - The height of the manipulator is set to the full height of the storage unit.

2. For Panel-Hung Storage:
   - The manipulator is positioned at the center of the storage unit's width and depth.
   - The height of the manipulator is set to the sum of the storage unit's height and its elevation from the ground.

If the manipulator is not associated with either of these storage types, it will be positioned at the origin point (0, 0, 0).

## Orientation

The manipulator is always oriented in a specific way:
- It has no rotation around the vertical axis.
- It is rotated 90 degrees around the horizontal axis (front-to-back).
- It has no rotation around the depth axis.

This orientation ensures that the manipulator is always facing the correct direction for easy interaction.

## Appearance

The manipulator may appear as an arrow, depending on whether the associated storage unit can be stretched or resized. This visual cue helps users understand when they can adjust the height of the storage unit.

## Interaction

While not explicitly stated in the provided information, it's likely that this manipulator allows users to adjust the height of storage units by clicking and dragging. The exact interaction method and any constraints on height adjustment would need to be verified with additional information.

## Remarks and Disclaimers

- This documentation is based on the provided class information and may not cover all aspects of the manipulator's functionality.
- The exact visual representation of the manipulator in the user interface is not specified in the given information.
- Additional rules or constraints regarding minimum and maximum heights for storage units may exist but are not detailed in the provided code.
- The functionality for actually changing the height of the storage unit when the manipulator is used is not included in this class and would likely be handled elsewhere in the system.