## [0.0.3] - 2025-11-14
### Added
- Added `T: Text` variable and automatic `JsonObject.WriteTo(T);` in generated procedures.
- Updated extension icon to a new minimalist 128x128 design.
- Improved README.md with English documentation and feature examples.

### Changed
- Minor cleanup of generated procedure indentation.
- Updated categories in `package.json` for better Marketplace visibility.

---

## [0.0.2] - 2025-11-14
### Added
- Added JSON preview WebView for quick payload inspection.
- Added support for choosing output mode (full procedure vs. Add-lines only).
- Added automatic enum detection using `Format()` when generating JsonObject mapping.

### Fixed
- Case-insensitive trigger for `BuildJson`.
- Improved code action detection logic.

---

## [0.0.1] - 2025-11-14
### Added
- Initial release.
- Generate JsonObject.Add mapping from Item, Customer, Vendor.
- Full procedure generation.
- Configurable mappings via `mappings.json`.
