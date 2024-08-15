Based on the provided documents, I will consolidate the information into a single, clear, and concise document. Since there is no information in the Part Numbers document, the consolidated document will be based entirely on the Configuration Logic document.

# FOItemTag and FOItemTagInfo Documentation

## Overview

This document describes the functionality and behavior of the FOItemTag and FOItemTagInfo classes, which are used for creating and managing item tags in an office environment. These classes handle the display and export of text labels associated with office items.

## FOItemTag

The FOItemTag class creates dynamic item tags in an office setting, extending the functionality of basic dynamic item tags.

### Key Features:

1. **Positioning**: Placement at specific positions in the 3D office layout.
2. **Rotation**: Alignment with office items or viewing angles.
3. **Identification**: Association with a unique key for easy management.

## FOItemTagInfo

The FOItemTagInfo class contains information for creating and displaying item tags in an office environment, building upon basic item tag information.

### Key Features:

1. **Text Style**: Custom text style for consistency with office design standards.
2. **Layer Information**: Office-specific drawing layer information for proper display and export.

## Tag Behavior and Rules

1. **Text Display**:
   - Displays text associated with an office item.
   - Default text height is 4 inches, but customizable.

2. **Visibility**:
   - Depends on current view mode and layer settings.
   - Can be hidden based on specific export or view settings.

3. **Export Behavior**:
   - Includes tag attributes (text, position, rotation, color).
   - Considers visibility settings and current view mode.

4. **Layer Management**:
   - Associated with specific layers affecting visibility and export behavior.
   - Determines display in different views or exports.

5. **Text Styling**:
   - Uses custom text style (font, color, size) for consistency with office design standards.

6. **Positioning and Rotation**:
   - Can be positioned anywhere in the 3D office layout.
   - Rotatable to align with furniture or face specific viewing angles.

7. **Identification**:
   - Associated with a unique key for easy management and reference.

## Interaction with Other Office Items

- Typically associated with specific office items or areas.
- May require updates or repositioning when office layouts change.
- Visibility and appearance may be affected by global office view settings.

## Remarks

- This documentation is based on provided class information and may not cover all possible use cases or exceptions.
- Exact tag behavior may depend on specific implementations of related classes and global settings not visible in the provided code.
- For more detailed information, consult the full system documentation or contact the development team.