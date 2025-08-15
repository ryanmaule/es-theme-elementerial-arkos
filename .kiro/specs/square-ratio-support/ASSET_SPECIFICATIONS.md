# Asset Specifications for 1:1 Ratio (720x720)

## Current Status
All assets are currently copied from ratio32 (480x320) as temporary placeholders.
These need to be recreated at 720x720 resolution for optimal square display.

## Required Assets

### 1. borders.png
- **Target Size**: 720x720
- **Current**: 480x320 (placeholder from ratio32)
- **Purpose**: Screen border overlay
- **File Size Analysis**: 
  - ratio32: 1,695 bytes (480x320)
  - ratio43: 3,002 bytes (640x480) 
  - ratio53: 12,822 bytes (1920x1152)
- **Requirements**: 
  - Transparent background with subtle borders
  - Maintains theme aesthetic consistency
  - Should scale proportionally for 720x720 resolution
  - Estimated target file size: ~2,500-4,000 bytes
- **Creation Notes**: 
  - Examine existing borders for visual elements and transparency
  - Scale border thickness proportionally for square format
  - Maintain corner radius and visual consistency

### 2. carousel-background.png
- **Target Size**: 720x720
- **Current**: 480x320 (placeholder from ratio32)
- **Purpose**: Background for system carousel view
- **File Size Analysis**: 
  - ratio32: 22,772 bytes (480x320)
  - ratio43: 38,180 bytes (640x480) 
  - ratio53: 163,517 bytes (1920x1152)
- **Requirements**: 
  - Proper visual hierarchy for system logos and text
  - Square-optimized layout with centered focus
  - Gradient or visual elements that work with square format
  - Estimated target file size: ~35,000-50,000 bytes
- **Creation Notes**: 
  - Adapt gradient/visual elements for square aspect ratio
  - Ensure system logo positioning area is optimized
  - Maintain text readability areas

### 3. gamelist-basic.png
- **Target Size**: 720x720
- **Current**: 480x320 (placeholder from ratio32)
- **Purpose**: Background for basic game list view
- **File Size Analysis**: 
  - ratio32: ~15,000-25,000 bytes (estimated)
  - ratio43: ~25,000-40,000 bytes (estimated)
  - ratio53: ~80,000-120,000 bytes (estimated)
- **Requirements**: 
  - Optimal contrast for text readability
  - Square layout considerations for game list positioning
  - Estimated target file size: ~30,000-45,000 bytes

### 4. gamelist-video.png
- **Target Size**: 720x720
- **Current**: 480x320 (placeholder from ratio32)
- **Purpose**: Background for video game list view
- **File Size Analysis**: Similar to gamelist-basic.png
- **Requirements**: 
  - Proper video area definition for square format
  - Text contrast optimization for square layout
  - Video positioning area clearly defined
  - Estimated target file size: ~30,000-45,000 bytes

### 5. menu.png
- **Target Size**: 72x72 (SAME AS ALL OTHER RATIOS)
- **Current**: 72x72 (correct size, no changes needed)
- **Purpose**: Menu system overlay element (not full background)
- **File Size Analysis**: 
  - ratio32: 72x72 (small overlay file)
  - ratio43: 72x72 (small overlay file)
  - ratio53: 72x72 (small overlay file)
  - ratio11: 72x72 (already correct)
- **Requirements**: 
  - NO CHANGES NEEDED - this file is resolution-independent
  - White with transparent rounded corner masks (as you described)
  - File can be left as-is from the copied ratio32 version

### 6. osd-bg.png
- **Target Size**: 720x720
- **Current**: 480x320 (placeholder from ratio32)
- **Purpose**: On-screen display background
- **File Size Analysis**: Similar to other background assets
- **Requirements**: 
  - Proper transparency for help prompts and status indicators
  - Square format optimization for OSD elements
  - Estimated target file size: ~20,000-35,000 bytes

## Asset Creation Notes
- All assets use 8-bit/color RGBA format with transparency support
- Maintain visual consistency with existing theme aesthetic
- Consider Material Design principles that the theme is based on
- Ensure proper contrast ratios for text readability
- Test with various color schemes (14 available)

## Comparison with Other Ratios
- **ratio32**: 480x320 (3:2) - closest to square, good reference
- **ratio43**: 640x480 (4:3) - standard format
- **ratio53**: 1920x1152 (5:3) - widescreen format
- **ratio11**: 720x720 (1:1) - target square format