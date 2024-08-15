Based on the provided documents, there is only one document with relevant information about the FODataWsStretcher. Since there is no information about Part Numbers, I will consolidate the information from the Configuration Logic document into a clear and concise format. Here's the consolidated documentation:

# FODataWsStretcher Documentation

## Overview

The FODataWsStretcher is a component used in office furniture design for configuring worksurfaces. It functions as a manipulator that allows for adjustments to the worksurface, specifically related to stretching or modifying edges.

## Key Features and Functionality

1. **Edge Association**: 
   - Each FODataWsStretcher is linked to a specific edge of a worksurface.
   - The edge is identified by a unique ID, stored upon creation.

2. **Position and Orientation**:
   - Has a settable and retrievable position in 3D space.
   - Has a settable and retrievable orientation.
   - These properties likely determine the location and method of worksurface manipulation.

3. **Visibility**:
   - Can be visible or hidden.
   - Visibility typically depends on the associated worksurface.
   - Default is visible if no worksurface is associated.

4. **Interaction Style**:
   - Uses an arrow style for interaction.
   - Likely represented by an arrow in the user interface to indicate stretching direction or area.

5. **Rotation Behavior**:
   - Not independently rotatable.
   - Orientation is tied to the associated worksurface.

6. **Worksurface Relationship**:
   - Each FODataWsStretcher is associated with a specific FODataWorksurface.
   - This association enables interaction with and modification of the attached worksurface.

## Usage in Design

Interior designers can utilize the FODataWsStretcher to:

1. Adjust worksurface size or shape by manipulating edges.
2. Fine-tune worksurface dimensions to meet specific space requirements.
3. Customize office space layouts by modifying individual worksurfaces.

## Remarks and Disclaimers

- This documentation is based on provided class information and may not cover all aspects of the FODataWsStretcher's functionality in the broader system.
- The exact visual representation and user interaction methods are not specified and may depend on the user interface implementation.
- Specific rules for how stretching affects worksurface dimensions and any limitations are not defined in this class and may be implemented elsewhere in the system.
- Information about part numbers or specific dimensions was not found in the provided code and may be handled by the FODataWorksurface class or another related class.