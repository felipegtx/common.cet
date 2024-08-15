Here's the consolidated document combining the information from both sources:

# Chair Insertion Animation Documentation

This document describes the logic and behavior of the chair insertion animation for interior designers. The animation is designed to facilitate the placement of chairs in a space, particularly in relation to tables or other furniture.

## Multi-Chair Insertion

The animation allows for the insertion of multiple chairs at once. This feature can be toggled on or off.

- By default, multiple chair insertion is enabled.
- Users can choose to insert a single chair or multiple chairs based on their needs.

## Chair Positioning

When inserting chairs, there are two main adjustable parameters:

1. **Rotation Offset**: 
   - This determines the angle at which the chair is rotated relative to its default position.
   - The rotation can be set between 0 and 359 degrees.
   - By default, there is no rotation (0 degrees).

2. **Position Offset**: 
   - This adjusts the chair's position relative to its default placement point.
   - The offset can range from -6 inches to 24 inches.
   - By default, there is no position offset (0 inches).

These settings allow for fine-tuning of chair placement to ensure proper alignment with tables or other furniture.

## Chair-Table Interaction

When placing chairs near tables:

- The animation attempts to snap the chair to an appropriate position relative to the table.
- If the chair being placed is a specific type (FODataChair), it will use a predefined snap point to align with the table.
- For other chair types, a default snapping behavior is used.

## Insertion Process

1. If multiple chair insertion is enabled:
   - The animation will attempt to place multiple chairs around a table or in a designated area.
   - It takes into account the rotation and position offsets for each chair.
   - Chairs are placed to avoid overlapping with each other or other furniture.

2. If single chair insertion is selected:
   - Only one chair will be placed at a time.
   - The chair will be positioned according to the specified rotation and position offsets.

3. After placement, the animation checks for any conflicts or overlaps with existing furniture.

4. The process completes once all selected chairs are successfully placed or if the user ends the animation manually.

## User Interaction

- Users can adjust the multi-insert, rotation, and position settings during the animation process.
- These settings are remembered for future use, allowing for consistent chair placement across multiple insertion actions.

## Limitations and Considerations

- The animation may behave differently depending on the specific type of chair being inserted.
- Complex room layouts or tightly packed spaces may limit the ability to insert multiple chairs simultaneously.
- Users should be aware of the room's scale and furniture arrangement to ensure optimal chair placement.

## Part Numbers

The FIKA product line includes various chair options. Here's a breakdown of the chair part numbers:

| Part Number | Description |
|-------------|-------------|
| FIKA-CHR-01 | Standard Chair |
| FIKA-CHR-AR | Chair with Armrests |
| FIKA-CHR-HR | Chair with Headrest |

The part number structure for chairs follows this pattern:

| Prefix | Product Type | Feature |
|--------|--------------|---------|
| FIKA   | CHR          | 01/AR/HR |

- FIKA: Represents the product line
- CHR: Indicates it's a chair
- Feature: 
  - 01: Standard model
  - AR: With armrests
  - HR: With headrest

When selecting chairs for insertion, users should refer to these part numbers to ensure they are using the correct chair type for their design.

This animation tool aims to streamline the process of placing chairs in a design, offering flexibility and precision in furniture arrangement. By understanding the part number system, designers can easily identify and select the appropriate chair models for their projects.