# UI/Style Guide Summary

## Theme
- Application theme: light
- Visual style: modern
- Color accents:
  - Primary: #3b82f6
  - Secondary: #64748b
  - Success: #06b6d4
  - Error: #EF4444
  - Background: #f9fafb
  - Surface: #ffffff
  - Text: #111827
- Suggested gradient: from #3b82f6 at 10% alpha to gray-50 for subtle header backgrounds

## Material 3 and ColorScheme
- Use Material 3 and ColorScheme for consistency
- Prefer ColorScheme.surface over deprecated background fields
- Use withAlpha() for transparency

## Layout
- Main list view displaying phone cards vertically
- Each card includes image, brand, model, and price
- Tap card to navigate to detail screen
- Detail page shows larger image, prominent model and brand, and price

## Components
- AppBar: clear title, surface background, and primary content color
- Cards: rounded corners, subtle elevation, surface background
- Typography: legible defaults with slight emphasis on price
- Spacing: consistent padding (e.g., 16dp around list and 12–16dp within cards)

## Accessibility
- Maintain sufficient color contrast with the light palette
- Minimum touch targets of 48x48dp
- Support scalable text (respect device text scale)

## Assets
- Place images in assets/
- Declare in pubspec.yaml (already configured)

## Example Theming Snippet
```dart
theme: ThemeData(
  colorScheme: ColorScheme.fromSeed(seedColor: const Color(0xFF3b82f6)),
  useMaterial3: true,
)
```
