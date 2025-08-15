# Design Document

## Overview

This design document outlines the implementation of 1:1 (square) screen ratio support for the Elementerial EmulationStation theme. The implementation follows the existing modular architecture pattern used for 3:2, 4:3, and 5:3 ratios, ensuring consistency and maintainability.

The 720x720 square resolution presents unique layout challenges compared to rectangular ratios, requiring optimized positioning and sizing for UI elements to maximize screen utilization while maintaining visual hierarchy and usability.

## Architecture

### Modular Ratio System
The theme uses a subset-based architecture where users can select their screen ratio through the theme settings. Each ratio has:

1. **Configuration File**: A dedicated XML file (`view-system-11.xml`) containing ratio-specific overrides
2. **Asset Directory**: A folder (`assets/ratio11/`) containing ratio-optimized background images
3. **Variable System**: A `ratioPath` variable that dynamically references the correct asset folder

### File Structure
```
├── settings/display/
│   └── view-system-11.xml          # 1:1 ratio configuration
├── assets/
│   └── ratio11/                    # 1:1 ratio assets
│       ├── borders.png
│       ├── carousel-background.png
│       ├── gamelist-basic.png
│       ├── gamelist-video.png
│       ├── menu.png
│       └── osd-bg.png
└── theme.xml                       # Updated to include 1:1 option
```

## Components and Interfaces

### 1. Theme Configuration (theme.xml)
- Add "1:1" option to the "Ratio" subset
- Include reference to `view-system-11.xml`

### 2. Ratio Configuration (view-system-11.xml)
- Define `ratioPath` variable as "ratio11"
- Override positioning and sizing for all views that require square-specific layouts
- Maintain compatibility with all existing theme features

### 3. Asset Creation (assets/ratio11/)
- Create square-optimized background images (720x720)
- Ensure visual consistency with existing ratio assets
- Optimize for square aspect ratio display

### 4. Layout Optimizations
Based on analysis of existing ratio files, the following elements require square-specific adjustments:

#### System Carousel View
- **Carousel positioning**: Optimize logo positioning for square layout
- **System name/info**: Adjust text positioning to work with square backgrounds
- **Logo scaling**: Ensure system logos display properly in square format

#### Game List Views (Basic, Detailed, Video)
- **Text spacing**: Adjust line spacing for optimal readability
- **Image positioning**: Reposition game images and metadata for square layout
- **Rating positioning**: Adjust star rating placement

#### Grid Views
- **Grid layout**: Optimize grid dimensions (likely 3x3 or 4x4 for square)
- **Tile padding**: Adjust spacing between grid items
- **Image corners**: Set appropriate corner radius for square display
- **Text sizing**: Optimize text size and padding for grid tiles

#### Menu and UI Elements
- **Status bar**: Position clock and battery indicators for square screens
- **Battery icons**: Use appropriately sized icons (likely 24x24 for 720x720)
- **Help prompts**: Ensure help text fits properly

## Data Models

### Configuration Variables
```xml
<variables>
  <ratioPath>ratio11</ratioPath>
</variables>
```

### Key Layout Parameters (Estimated for 720x720)
- **Grid layouts**: 3x3 or 4x4 depending on view type
- **Margins**: Consistent with existing ratios but optimized for square
- **Font sizes**: Inherit from existing font size system
- **Icon sizes**: 24x24px for status bar elements
- **Corner radius**: Consistent with theme's rounded corner aesthetic

## Error Handling

### Asset Fallbacks
- If ratio11 assets are missing, gracefully fall back to default assets
- Maintain theme functionality even with incomplete asset sets

### Layout Validation
- Ensure all UI elements remain within screen boundaries
- Validate that text doesn't overflow or get cut off
- Test with various game list lengths and metadata combinations

## Asset Creation Strategy

### Required Assets for ratio11 folder
The following PNG assets need to be created at 720x720 resolution:

1. **borders.png** - Screen border overlay (likely transparent with subtle borders)
2. **carousel-background.png** - Background for system carousel view
3. **gamelist-basic.png** - Background for basic game list view
4. **gamelist-video.png** - Background for video game list view  
5. **menu.png** - Background for menu system
6. **osd-bg.png** - Background for on-screen display elements

### Asset Creation Methods
Since I cannot generate PNG files directly, the asset creation will require one of these approaches:

1. **Manual Creation**: Use image editing software (GIMP, Photoshop, etc.) to create square versions
2. **Intelligent Cropping**: Analyze existing ratio assets and crop/adapt to square format while preserving key visual elements
3. **Template-Based**: Create reusable templates that maintain the theme's visual language
4. **Placeholder Strategy**: Initially use solid color or simple gradient placeholders, then replace with proper assets

### Recommended Approach
For this implementation, I recommend:
1. **Phase 1**: Create simple placeholder assets (solid colors matching theme) to test functionality
2. **Phase 2**: Analyze existing assets to understand their structure and visual elements
3. **Phase 3**: Create proper square assets using image editing tools, guided by the analysis

### Asset Analysis Strategy
I can analyze the existing ratio32, ratio43, and ratio53 assets by:
- Examining their dimensions and aspect ratios
- Understanding their visual structure and key elements
- Providing specific guidance on how to adapt them for 1:1 ratio
- Creating detailed specifications for manual asset creation

### Asset Design Principles
- Maintain visual consistency with existing theme aesthetic
- Ensure backgrounds don't interfere with text readability
- Use appropriate transparency and gradients
- Consider the Material Design principles the theme is based on

## Complete View Coverage Analysis

Based on analysis of all view files in settings/display/, the 1:1 ratio needs to handle:

### Core Views (Covered in design)
- **view-system.xml** - System carousel and navigation
- **view-general.xml** - Common game list layouts
- **view-grid.xml** - Grid-based game browsing
- **view-boxes.xml** - Box art focused grid view
- **view-elementflix.xml** - Netflix-style horizontal scrolling

### Additional Views (Need consideration)
- **view-menu.xml** - Menu backgrounds (uses ratioPath for menu.png)
- **view-system-video.xml** - Video playback in system view (no ratio-specific changes needed)
- **customBg.xml** - Custom background support (no ratio-specific changes needed)
- **randomBg.xml** - Random background support (no ratio-specific changes needed)

## Testing Strategy

### Manual Testing Requirements
1. **View Coverage**: Test all view types (system, basic, detailed, grid, boxes, video, elementflix, menu)
2. **Color Schemes**: Verify compatibility with all 14 color schemes
3. **Font Sizes**: Test with small, medium, and large font size options
4. **Feature Compatibility**: Verify custom backgrounds, video playback, and status bar options work correctly
5. **Background Styles**: Test default, random, and custom background options
6. **Edge Cases**: Test with long game names, missing metadata, and various image aspect ratios

### Visual Validation
1. **No Cutoff**: Ensure no UI elements are cut off or positioned outside screen bounds
2. **Proper Spacing**: Verify adequate spacing between elements
3. **Readability**: Confirm text remains readable at all font sizes
4. **Visual Hierarchy**: Maintain proper visual hierarchy and focus indicators

### Device-Specific Testing
- Test on actual 720x720 R36Max device
- Compare with 3:2 ratio to ensure improvement
- Validate performance with video playback and animations

## Implementation Phases

### Phase 1: Core Structure
1. Create `view-system-11.xml` with basic ratio configuration
2. Update `theme.xml` to include 1:1 ratio option
3. Create placeholder assets in `assets/ratio11/`

### Phase 2: Layout Optimization
1. Analyze and implement system carousel optimizations
2. Optimize game list views for square layout
3. Adjust grid layouts and spacing

### Phase 3: Asset Creation
1. Create optimized background images for all views
2. Ensure visual consistency with existing theme
3. Test asset quality and loading performance

### Phase 4: Fine-tuning
1. Adjust spacing, padding, and positioning based on testing
2. Optimize for edge cases and various content types
3. Final validation across all theme features

## Design Decisions and Rationales

### Grid Layout Choice
- **Decision**: Use 3x3 grid for main grid view, 4x4 for boxes view
- **Rationale**: Maximizes screen utilization while maintaining readability and touch targets

### Asset Strategy
- **Decision**: Create new square-optimized assets rather than stretching existing ones
- **Rationale**: Ensures optimal visual quality and prevents distortion

### Positioning Strategy
- **Decision**: Center-align major elements with appropriate margins
- **Rationale**: Square format benefits from centered layouts, and this maintains visual balance

### Icon Size Selection
- **Decision**: Use 24x24px icons for status bar elements
- **Rationale**: Provides good visibility on 720x720 display while maintaining proportion with other UI elements

This design ensures that the 1:1 ratio implementation integrates seamlessly with the existing theme architecture while providing an optimal user experience for square screen devices.