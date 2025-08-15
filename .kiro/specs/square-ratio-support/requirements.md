# Requirements Document

## Introduction

This feature adds 1:1 (square) screen ratio support to the Elementerial EmulationStation theme for ArkOS. The R36Max device has a 720x720 square display, and currently using the 3:2 ratio leaves a portion of the screen cut off on the right side. Adding native 1:1 support will provide optimal display utilization and visual experience for square screen devices.

## Requirements

### Requirement 1

**User Story:** As a user with a square screen device (720x720), I want to select a 1:1 screen ratio option in the theme settings, so that the theme displays properly without any screen cutoff.

#### Acceptance Criteria

1. WHEN the user accesses theme settings THEN the system SHALL display a "1:1" option in the "Screen ratio" subset
2. WHEN the user selects the "1:1" ratio option THEN the system SHALL apply square-optimized layouts and assets
3. WHEN the 1:1 ratio is active THEN the system SHALL utilize the full 720x720 screen area without cutoff

### Requirement 2

**User Story:** As a user with a square screen, I want all theme views (system carousel, game lists, menus, etc.) to be properly laid out for 1:1 aspect ratio, so that all UI elements are visible and aesthetically pleasing.

#### Acceptance Criteria

1. WHEN viewing the system carousel THEN the system SHALL display system logos and information positioned optimally for square screens
2. WHEN viewing game lists THEN the system SHALL display game information, metadata, and navigation elements properly sized for square layout
3. WHEN viewing the grid view THEN the system SHALL arrange game thumbnails in a grid layout optimized for square dimensions
4. WHEN viewing menus THEN the system SHALL display menu items and backgrounds properly fitted to square screens
5. WHEN viewing any theme view THEN the system SHALL ensure no UI elements are cut off or improperly positioned

### Requirement 3

**User Story:** As a user, I want the 1:1 ratio to have the same visual quality and asset support as other ratios, so that I get a consistent theme experience regardless of my screen ratio.

#### Acceptance Criteria

1. WHEN using 1:1 ratio THEN the system SHALL provide ratio-specific background images for all views
2. WHEN using 1:1 ratio THEN the system SHALL provide properly sized border overlays and UI elements
3. WHEN using 1:1 ratio THEN the system SHALL support all color schemes available in other ratios
4. WHEN using 1:1 ratio THEN the system SHALL support all view types (basic, detailed, grid, boxes, video, elementflix)
5. WHEN using 1:1 ratio THEN the system SHALL provide appropriate battery and status bar icons sized for the resolution

### Requirement 4

**User Story:** As a developer maintaining the theme, I want the 1:1 ratio implementation to follow the existing theme architecture patterns, so that it integrates seamlessly and is maintainable.

#### Acceptance Criteria

1. WHEN implementing 1:1 support THEN the system SHALL follow the same file structure pattern as existing ratios
2. WHEN implementing 1:1 support THEN the system SHALL use the same variable naming conventions and XML structure
3. WHEN implementing 1:1 support THEN the system SHALL maintain compatibility with all existing theme features
4. WHEN implementing 1:1 support THEN the system SHALL not break or affect existing ratio configurations