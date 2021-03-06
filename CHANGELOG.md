## [Unreleased](https://github.com/hlpullen/quickviewer/compare/v0.2.0...HEAD)

### Added
- DICOM support for images, dose fields, and structures
- Extra user settings: `cmap`, `dose_cmap`
- Ability to load a dose field via the `dose` argument without loading an image file
- Ability to change type of comparison image with a dropdown menu
- Computation and plotting of distance-to-agreement and gamma index comparison images
- Ability to print mean squared error on comparison plot
- Options `structs_to_keep` and `structs_to_ignore` to give user more control over which structures to load

### Changed:
- Zoom level stays the same when switching between different orientations.

## [0.1.0](https://github.com/hlpullen/quickviewer/releases/tag/v0.1.0) - 2021-04-13

### Added
- Version of QuickViewer presented in Radiotherapy Research Group meeting.
- Features include:
    - Interactive NIfTI file viewing
    - Saving publication-quality plots
    - Overlaying dose fields, structures, and masks
    - Viewing of chequerboard, overlay and differences between two images
    - Viewing of deformation field and Jacobian determinant
    - Creation of structure information and structure comparison tables
    - Ability to compare many structures at once via majority vote
    - Time slider for a series of multiple images at different time points
