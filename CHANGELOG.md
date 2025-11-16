## [0.2.0] - 16-11-2025
### Added
- Automatic insertion of missing variables when using **Only JsonObject.Add(...) lines** mode.
- Intelligent scanning that ensures all required JSON-related elements (variables, Add-lines, WriteTo, etc.) are added when missing.
- Added `source` support in mappings, allowing API field names to differ from actual table field names.
- Updated mapping logic to fully align with `AZ AL Dev Tools` field generation.

### Changed
- Mode selection is now performed *before* table detection, enabling generation of multiple full procedures within the same file without incorrect context detection.
- Improved README with clearer documentation and usage guidance.
- Improved overall formatting and consistency of all generated AL code.

### Fixed
- Fixed procedure boundary detection to prevent code from being inserted in the wrong scope.
- Corrected `JsonObject.WriteTo(T);` placement so it always appears after all generated Add-lines and before `end;`.
- Fixed field-name resolution ensuring lowercase API names map correctly to the correct AL field names.
- Fixed issue where generating multiple procedures reused an incorrect record variable due to overly aggressive context detection.

---

## [0.1.0] - 15-11-2025
### Added
- Added changelog with version history.
- Automatic `JsonObject: JsonObject;` variable generation when missing in the procedure’s var section.
- Automatic detection of record variables such as `Item: Record Item;` or `CustomerRec: Record Customer`.

### Changed
- Improved internal code structure and generation flow.
- Improved formatting for generated AL code.

### Fixed
- Fixed an issue where certain `Record "Table Name"` declarations were not detected correctly.

---

## [0.0.3] - 14-11-2025
### Added
- Added `T: Text` variable and automatic `JsonObject.WriteTo(T);` insertion when generating procedures.
- Added preview panel for JSON payload (Ctrl + . → Preview JSON payload).
- Updated extension icon with new minimalist 128×128 design.
- Improved README.md with English documentation and feature examples.

### Changed
- Minor cleanup of procedure indentation.
- Updated categories in `package.json` for better Marketplace visibility.

---

## [0.0.2] - 14-11-2025
### Added
- Added JSON preview WebView for quick payload inspection.
- Added support for selecting output mode (full procedure vs. Add-lines only).
- Added automatic enum formatting (`Format()`) for enum fields defined in mappings.

### Fixed
- Case-insensitive detection of `BuildJson`.
- Improved code-action detection logic.

---

## [0.0.1] - 14-11-2025
### Added
- Initial release.
- Generate JsonObject.Add mappings for Item, Customer, and Vendor tables.
- Full procedure generation.
