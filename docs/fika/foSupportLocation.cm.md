Here's the consolidated document combining the information from both sources:

# FOSupportLocation Documentation

## Overview

The FOSupportLocation class represents a specific location for accessories in the FIKA office product line. This class extends the functionality of the AccessoryLocation class, adding additional properties to define the characteristics of the support location.

## Key Features

1. **Left-Handed Support**: The location can be designated as left-handed, which may affect the orientation or placement of accessories.

2. **Corner Support**: The location can be specified as a corner position, which may influence how accessories are placed or connected.

3. **Shared Support**: The location can be marked as shareable, potentially allowing multiple accessories to use the same support point.

## Location Properties

When defining a support location, the following properties can be set:

1. **Owner**: The main object to which this support location belongs.
2. **Key**: A unique identifier for the support location.
3. **Position**: The exact point in 3D space where the support is located.
4. **Rotation**: The orientation of the support location.
5. **Filter**: A set of criteria that may limit which accessories can use this location.
6. **Priority**: A numerical value that may influence the order in which this location is considered for accessory placement.
7. **Left-Handed**: Indicates if the support is designed for left-handed configurations.
8. **Corner**: Specifies if the support is located in a corner.
9. **Sharable**: Determines if multiple accessories can use this support location simultaneously.

## Part Numbers

The FIKA product line includes various support-related components. Here's a breakdown of the relevant part numbers:

### Cantilever Supports

| Part Number | Description |
|-------------|-------------|
| FIKA-CANTILEVER-DBL | Double cantilever support |
| FIKA-CANTILEVER-LH | Left-hand cantilever support |
| FIKA-CANTILEVER-RH | Right-hand cantilever support |

### Rectangular Supports

| Part Number | Description |
|-------------|-------------|
| FIKA-RECT-SUPPORT | Rectangular support |

These part numbers represent different types of supports that can be used with the FOSupportLocation class.

## Usage Guidelines

When working with FOSupportLocation:

1. **Accessory Compatibility**: Ensure that accessories are compatible with the support location's properties. For example, a left-handed accessory should be paired with a left-handed support location (FIKA-CANTILEVER-LH).

2. **Corner Placements**: When a support location is marked as a corner, consider the spatial constraints and ensure that accessories designed for corner placement are used.

3. **Shared Supports**: If a support location is marked as sharable, multiple accessories may be attached to it. Verify that the combined weight and size of these accessories are within the support's capacity. The FIKA-CANTILEVER-DBL might be suitable for shared support scenarios.

4. **Prioritization**: The priority value can be used to determine which support locations should be considered first when placing accessories. Higher priority locations may be preferred over lower priority ones.

5. **Filtering**: The filter property can be used to restrict which types of accessories can be placed at this location. This ensures that only compatible accessories are used with specific support points.

## Interaction with Other Products

When integrating FOSupportLocation with other products or accessories:

1. Ensure that the accessory's dimensions and weight are suitable for the support location.
2. Check if the accessory requires a left-handed (FIKA-CANTILEVER-LH), right-handed (FIKA-CANTILEVER-RH), or double (FIKA-CANTILEVER-DBL) support, and match it accordingly.
3. For standard rectangular support needs, use the FIKA-RECT-SUPPORT.
4. Verify that the accessory meets any criteria specified in the location's filter.
5. Consider the rotation of the support location to ensure the accessory is oriented correctly when placed.

By following these guidelines and using the appropriate support part numbers, you can ensure that accessories are correctly placed and supported within the FIKA office product line, maintaining both functionality and design integrity.