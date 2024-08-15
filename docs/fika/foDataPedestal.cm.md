Here's the consolidated document that combines the information from both sources while removing redundancies and preserving all key points:

# FIKA Office Pedestal Cabinet Documentation

## Product Overview

This document describes the configuration logic and part number structure for the FIKA Office Pedestal Cabinet. This storage unit is designed to fit under desks or workstations, providing convenient storage space in office environments.

## Dimensions

The FIKA Office Pedestal Cabinet is available in the following dimensions:

1. Width:
   - 15 inches
   - 18 inches

2. Depth:
   - 18 inches
   - 24 inches
   - 30 inches

3. Height:
   - Fixed at a standard height (exact measurement not specified)

## Part Number Structure

The part number for the FIKA Office Pedestal Cabinet follows this structure:

```
FIKA-CAB-[Type]-[Width][Depth]
```

Where:
- FIKA: Brand identifier
- CAB: Product category (Cabinet)
- [Type]: Cabinet type (BBF for Box/Box/File, FF for File/File, or SBOOO for Side-to-Side)
- [Width]: Width in inches (15 or 18)
- [Depth]: Depth in inches (18, 24, or 30)

### Part Number Table

| Type | Width | Depth | Part Number |
|------|-------|-------|-------------|
| BBF  | 15    | 18    | FIKA-CAB-BBF-1518 |
| BBF  | 15    | 24    | FIKA-CAB-BBF-1524 |
| BBF  | 15    | 30    | FIKA-CAB-BBF-1530 |
| BBF  | 18    | 18    | FIKA-CAB-BBF-1818 |
| BBF  | 18    | 24    | FIKA-CAB-BBF-1824 |
| BBF  | 18    | 30    | FIKA-CAB-BBF-1830 |
| FF   | 15    | 18    | FIKA-CAB-FF-1518 |
| FF   | 15    | 24    | FIKA-CAB-FF-1524 |
| FF   | 15    | 30    | FIKA-CAB-FF-1530 |
| FF   | 18    | 18    | FIKA-CAB-FF-1818 |
| FF   | 18    | 24    | FIKA-CAB-FF-1824 |
| FF   | 18    | 30    | FIKA-CAB-FF-1830 |
| SBOOO| 15    | 18    | FIKA-CAB-SBOOO-1518 |
| SBOOO| 15    | 24    | FIKA-CAB-SBOOO-1524 |
| SBOOO| 15    | 30    | FIKA-CAB-SBOOO-1530 |
| SBOOO| 18    | 18    | FIKA-CAB-SBOOO-1818 |
| SBOOO| 18    | 24    | FIKA-CAB-SBOOO-1824 |
| SBOOO| 18    | 30    | FIKA-CAB-SBOOO-1830 |

## Product Categories

This pedestal cabinet belongs to the following categories:
- Lower Storage
- Lower Storage Symbol

These categories help classify the product within the office furniture system.

## Configuration Rules and Behavior

1. **Dimension Synchronization**: 
   The cabinet automatically updates its internal data to match the current width and depth settings. This ensures that all parts of the system are aware of the cabinet's current size.

2. **Height Initialization**: 
   When first placed, the cabinet always starts at the standard height for its type (BBF, FF, or SBOOO).

3. **Data Restoration**: 
   If the cabinet's configuration is changed, the system attempts to restore any sub-features that were previously set. This helps maintain consistency in the cabinet's setup even when modifications are made.

4. **Invalidation and Rebuilding**: 
   After certain changes, the cabinet's visual representation is marked for rebuilding. This ensures that what you see in the design accurately reflects the current configuration.

5. **Placement Behavior**: 
   The cabinet can be easily snapped into place within the office layout, making it simple to position correctly in relation to other furniture items.

## Interaction with Other Products

While specific interaction rules are not detailed in the provided information, the following can be inferred:

1. As a lower storage unit, this pedestal cabinet is likely designed to fit under or beside desks and workstations.
2. Its categorization as a lower storage item suggests it may have specific placement rules in relation to other office furniture pieces.

## Remarks and Disclaimers

1. The exact measurement for the standard height of each cabinet type is not specified in the provided information.
2. Detailed rules about how this pedestal cabinet interacts with other specific furniture items are not provided in the given class information.
3. No specific invalidation rules were found in the provided code snippet.