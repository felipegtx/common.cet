# FIKA Office COH Trim Documentation

## Product Overview

This document describes the configuration logic for the FIKA Office COH Trim component. The COH Trim is a part of the FIKA office furniture system and is used in various configurations.

## Part Number Structure

The part number for the COH Trim follows this structure:

```
FIKA-COH-[Height]
```

Where:
- `FIKA-COH-` is the fixed prefix for all COH Trim components
- `[Height]` is the height of the trim in inches

## Valid Part Numbers

The following table lists all valid part numbers for the FIKA Office COH Trim:

| Part Number | Height (inches) |
|-------------|-----------------|
| FIKA-COH-06 | 6               |
| FIKA-COH-12 | 12              |
| FIKA-COH-18 | 18              |
| FIKA-COH-24 | 24              |
| FIKA-COH-30 | 30              |
| FIKA-COH-36 | 36              |

## Configuration Rules and Behavior

1. **Height Selection**: 
   - The COH Trim is available in six specific heights: 6, 12, 18, 24, 30, and 36 inches.
   - When a height is chosen for the trim, it will automatically adjust to the nearest available height option.
   - For example, if a height of 15 inches is requested, the system will adjust it to 18 inches.

2. **Connection Angle**: 
   - The trim has a connection angle property called "connA". This angle determines how the trim connects to other components in the FIKA office system.

3. **Positioning**: 
   - The trim is positioned relative to the frame depth of the FIKA office system. It is offset by half the frame depth towards the back.

4. **Item Tag**: 
   - Each trim piece has an associated item tag for identification purposes.
   - The tag displays "CH" followed by the height of the trim in inches.
   - For example, a 24-inch trim would have a tag displaying "CH24".
   - The tag is positioned 6 inches away from the trim's connection point, in the direction of the connection angle.

5. **Graphics**: 
   - The visual representation of the trim in 2D layouts is handled by the system, but no specific details are provided about its appearance.

## Interaction with Other Components

While specific details are not provided, the presence of a connection angle suggests that the COH Trim can be connected to other parts of the FIKA office system.

## Remarks and Disclaimers

1. The exact visual appearance of the COH Trim in 2D or 3D representations is not specified in the provided information.
2. There are no explicit invalidation rules mentioned for this component.
3. The purpose and functionality of the "build2D" method are not clear from the provided information, but it likely relates to the 2D representation of the trim.
4. The specific material or finish options for the COH Trim are not mentioned in the provided information.
5. The exact measurement unit for the connection angle (connA) is not specified, but it's likely to be in degrees.

This documentation provides a comprehensive overview of the FIKA Office COH Trim configuration logic based on the available information. For more detailed specifications or visual representations, please consult additional product documentation or contact the FIKA office system support team.