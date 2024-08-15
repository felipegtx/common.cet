Based on the provided documents, here's the consolidated documentation:

# FOSchemePushBehavior and FOMDataSchemePushBehavior Documentation

This document describes the behavior of two classes: FOSchemePushBehavior and FOMDataSchemePushBehavior. These classes are responsible for managing the process of applying changes to product configurations in the FIKA Office system.

## FOSchemePushBehavior

This class handles the process of applying changes to a product's configuration.

### Key Features:

1. **Owner Association**: The class maintains a reference to a Snapper object, which likely represents the main product or component being configured.

2. **Pre-Push Preparation**: Before applying any changes, the class ensures that the necessary settings are in place for the object receiving the changes.

3. **Post-Push Actions**: After applying changes, the class performs several important actions:
   - It triggers a custom action related to the scheme being applied.
   - If the object receiving changes is a visual component, it marks it for visual update.

### Behavior:

1. When a change is about to be applied:
   - If the object receiving the change is a CoreObject but not a Snapper, its settings are ensured to be ready.

2. After a change has been applied:
   - A custom action is triggered, passing along details about the change (such as what was changed, the source of the change, and the new value).
   - If the object that received the change is a visual component (AOComponent), it is marked for visual update, ensuring that any visual changes are reflected in the user interface.

## FOMDataSchemePushBehavior

This class handles the process of applying changes specifically to data within the FIKA Office system.

### Key Features:

1. **Owner Association**: Similar to FOSchemePushBehavior, this class maintains a reference to an owner object, which likely represents the main product or component associated with the data being changed.

2. **Data-Specific Behavior**: This class is designed to work with a specific type of data structure (DsMultiPData), suggesting it handles complex or multi-layered data.

### Behavior:

1. After a change has been applied to the data:
   - A custom action is triggered on the owner object, passing along details about the change (such as what was changed, the source of the change, and the new value).
   - This custom action is specifically related to changes applied to data, as indicated by the "ToData" part of the action name.

## General Notes:

- Both classes are designed to work within a larger system that manages product configurations and their associated data.
- They provide hooks for custom actions to be performed when changes are applied, allowing for flexible and extensible behavior.
- The classes seem to be part of a system that separates the concerns of visual components and their underlying data, with each having its own specific behavior when changes are applied.

## Remarks and Disclaimers:

- This documentation is based solely on the provided class definitions and does not include information about the broader system these classes operate within.
- The exact nature of the "schemes" being applied and the specific types of changes these classes handle would require more context about the FIKA Office system.
- The behavior described here is focused on the logic of applying changes and does not include details about how these changes affect specific product configurations or dimensions.