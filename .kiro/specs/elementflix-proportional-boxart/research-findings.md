# EmulationStation Grid System Research Findings

## Current ElementFlix Implementation

### Grid Configuration:
- **autoLayout**: `3.5 1` (3.5 columns × 1 row)
- **scrollDirection**: `horizontal`
- **imageSource**: `thumb` (uses thumbnail images)
- **imageSizeMode**: Conditional based on BoxArtStyle subset:
  - `cover` → `minSize` (scales to fit smallest dimension)
  - `fit` → `maxSize` (scales to fit largest dimension)  
  - `stretch` → `size` (stretches to fill tile completely)

### Current Problem:
- `autoLayout` creates equal-width tiles regardless of image aspect ratios
- All images forced into same tile dimensions
- Landscape box art appears squished or poorly fitted

## Available EmulationStation Grid Properties

### Core Grid Properties:
1. **autoLayout**: `X Y` - Creates X columns × Y rows with equal tile sizes
2. **scrollDirection**: `horizontal` or `vertical`
3. **imageSource**: `image`, `thumbnail`, `thumb`, `marquee`
4. **margin**: Spacing around the entire grid
5. **padding**: Spacing around individual tiles
6. **animateSelection**: Enable/disable selection animations
7. **autoLayoutSelectedZoom**: Scale factor for selected items

### Image Sizing Options:
1. **minSize**: Scale image to fit within tile (maintains aspect ratio, may leave empty space)
2. **maxSize**: Scale image to fill tile (maintains aspect ratio, may crop image)
3. **size**: Stretch image to exact tile dimensions (distorts aspect ratio)

### Tile Configuration:
1. **selectionMode**: `full`, `image` - What gets highlighted on selection
2. **imageSizeMode**: How images fit within tiles
3. **backgroundColor**: Tile background color
4. **imageColor**: Image tint/color
5. **padding**: Internal tile padding

## Key Limitation Discovered:
**EmulationStation's `autoLayout` system inherently creates equal-sized tiles.** There is no built-in "proportional" or "variable-width" tile mode in the grid system.

## Potential Solutions:

### Option 1: Modified autoLayout + maxSize (Recommended)
- **Approach**: Use higher column count (e.g., `6 1` instead of `3.5 1`)
- **imageSizeMode**: `maxSize` to maintain aspect ratios
- **Result**: More tiles visible, images maintain proportions within tiles
- **Pros**: Minimal code changes, works within existing system
- **Cons**: Still has equal tile widths, but more tiles = better utilization

### Option 2: Dynamic autoLayout Based on System
- **Approach**: Different autoLayout values for different game systems
- **Implementation**: Conditional autoLayout based on system type
- **Result**: Portrait systems get more columns, landscape systems get fewer
- **Pros**: System-specific optimization
- **Cons**: Requires system detection and multiple configurations

### Option 3: Alternative Layout Approach
- **Approach**: Remove autoLayout, use manual positioning
- **Implementation**: Custom tile positioning and sizing
- **Result**: True proportional widths
- **Pros**: Complete control over proportions
- **Cons**: Major code changes, complex implementation

## Recommended Technical Approach:

**Use Option 1 - Modified autoLayout + maxSize** because:

1. **Minimal Changes**: Works within existing EmulationStation capabilities
2. **Better Utilization**: More tiles visible = better use of landscape images
3. **Maintains Compatibility**: No breaking changes to existing functionality
4. **Easy Implementation**: Simple conditional configuration

### Implementation Strategy:
```xml
<!-- Current -->
<autoLayout>3.5 1</autoLayout>
<imageSizeMode ifSubset="BoxArtStyle:cover">minSize</imageSizeMode>

<!-- Proportional -->
<autoLayout ifSubset="BoxArtStyle:proportional">6 1</autoLayout>
<imageSizeMode ifSubset="BoxArtStyle:proportional">maxSize</imageSizeMode>
```

This approach will:
- Show more games simultaneously (6 instead of 3.5)
- Use `maxSize` to maintain aspect ratios within tiles
- Allow landscape images to better utilize their tile space
- Keep portrait images properly proportioned

## Conclusion:
While true variable-width tiles aren't possible with EmulationStation's grid system, we can achieve significantly better results for landscape box art by using more columns and `maxSize` image scaling. This provides the proportional appearance you're looking for with minimal code changes.