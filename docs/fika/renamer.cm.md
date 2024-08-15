Based on the provided documents, I will consolidate the information into a single, clear, and concise document. Since there is no information in the Part Numbers document, the consolidated document will be based entirely on the Configuration Logic document.

# Fika Office Package Renaming Documentation

This document outlines the renaming logic for packages and classes in the Fika Office system, aimed at maintaining compatibility with older versions while reorganizing the system structure.

## Renaming Rules

### Old Fika Office (Versions 0.0.0 to 12.0.6)

1. "custom.fika.office" → "custom.fika.office.legacy"
2. "custom.fika.office.reports" → "custom.fika.office.legacy.reports"
3. "FOArticlePartColumn" → moved to "custom.fika" package and renamed to "FikaArticlePartColumn"

Note: These changes do not apply to classes listed in the dataFikaClassNames group.

### Data Fika Office (Up to Version 12.0.6)

1. "custom.fika.office.dataFika" → "custom.fika.office"
2. "custom.fika.office.dataFika.reports" → "custom.fika.office.reports"

Class renaming within "custom.fika.office.dataFika":
- "FOEJunction" → "FODataEJunction"
- "FOIJunction" → "FODataIJunction"
- "FOLJunction" → "FODataLJunction"
- "FOVJunction" → "FODataVJunction"
- "FOTJunction" → "FODataTJunction"
- "FOYJunction" → "FODataYJunction"
- "FOXJunction" → "FODataXJunction"
- "foHandedness" → "foSupportHandedness"

These renamed classes are added to the dataFikaClassNames group.

## System-wide Changes

1. "custom.fika.office.dataFika" package is marked as deprecated.
2. Old Fika Office renaming rules apply to the main package and reports package.
3. Data Fika Office renaming rules apply to the dataFika package and its reports package.

## Purpose and Impact

These changes reorganize the Fika Office system structure while maintaining backward compatibility. They affect how system components are organized and named, potentially impacting how users and other parts of the system locate and interact with these components.

Example: "FOEJunction" in "custom.fika.office.dataFika" is now "FODataEJunction" in "custom.fika.office".

These changes do not affect the functionality of the classes, only their names and locations within the system structure.

## Remarks

- This document focuses on renaming logic and does not cover specific functionality of renamed classes or packages.
- The renaming process is version-dependent.
- The complete list of classes in the dataFikaClassNames group is not provided in this documentation.
- This renaming process may be part of a larger system update or reorganization.