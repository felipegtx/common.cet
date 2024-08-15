Based on the provided documents, I will consolidate the information into a single, clear, and concise document. Since there is no information in the Part Numbers document, the consolidated document will be based entirely on the Configuration Logic document.

# FODataChairInsertAnimationG2 Documentation

This document describes the functionality and behavior of the FODataChairInsertAnimationG2 class, which is responsible for handling the insertion of chairs in a Fika office environment.

## Overview

The FODataChairInsertAnimationG2 class extends the ChairInsertAnimationG2 class and provides specific functionality for inserting chairs in a Fika office environment. It manages multiple chair insertions, chair rotation, and positioning relative to tables.

## Key Features

1. Multiple Chair Insertion
2. Chair Rotation Offset
3. Chair Position Offset
4. Table Snap Functionality

## Detailed Functionality

### Multiple Chair Insertion

- Allows insertion of multiple chairs at once
- Default: Enabled (true)
- User-configurable setting
- System remembers the last used value

### Chair Rotation Offset

- Allows setting a rotation offset for inserted chairs
- Default: 0 degrees
- System remembers the last used value

### Chair Position Offset

- Allows setting a position offset for inserted chairs
- Default: 0 inches
- System remembers the last used value

### Table Snap Functionality

- Automatically snaps chairs to nearby tables
- Specifically designed for FODataChair objects

## User Interaction

1. **Changing Settings**: The system updates and stores values for multiple insert, rotation offset, and position offset when changed by the user.

2. **Inserting Chairs**: 
   - Multiple chairs inserted if enabled, single chair if disabled
   - Based on available space and configuration

3. **Chair Placement**: 
   - Applies rotation offset to each chair
   - Applies position offset to each chair
   - Attempts to snap FODataChairs to nearby tables

## Important Notes

- Exact rules for multiple chair placement (spacing, maximum number) are not specified in this class
- Specific dimensions and constraints for chair insertion are not defined in this class

## Remarks

- This documentation is based solely on the provided class code
- Some functionalities may be inherited from parent classes or defined in other system components
- The method for building part numbers for the chairs is not defined in this class