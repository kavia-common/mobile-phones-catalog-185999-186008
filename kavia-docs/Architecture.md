# Architecture Overview

## Context
This project is a single-container Flutter application that displays a catalogue of mobile phones. It is a client-only app with no backend or authentication. The app uses Material 3 and aims for a light, modern design.

## Current Implementation Snapshot
At the time of this document:
- Entry point: lib/main.dart
- App widget: MyApp sets up MaterialApp with a light theme derived from a seed color.
- Home: MyHomePage shows a placeholder “App is being generated...” message and a progress indicator.
- Tests: test/widget_test.dart validates the placeholder UI text and app bar title.
- Config: pubspec.yaml declares dependencies and assets (including an empty .env and assets/ directory).

These reflect a scaffold ready to evolve into a fully functional phones list and detail flow.

## Targeted App Layers
Given the app’s simplicity and lack of backend, a lightweight layering is sufficient:

- Presentation
  - Screens:
    - PhonesListScreen: Displays a vertical list/grid of phone cards with image, brand, model, price.
    - PhoneDetailScreen: Shows large photo and detailed attributes of the selected phone.
  - Widgets:
    - PhoneCard: Reusable card with photo, brand, model, price.
- State/Logic
  - Provider-based ChangeNotifier(s) for simple state if needed (e.g., selected phone, filters).
- Data
  - Local static data source or in-app seeded data structures to represent phones.
  - Optionally, local persistence (e.g., SharedPreferences) for simple toggles or preferences. No remote calls.

## Dependencies in Codebase
Declared in pubspec.yaml:
- provider, shared_preferences, intl, path, sqflite, flutter_staggered_grid_view
Note: The current code uses only Flutter SDK. These dependencies enable common patterns if the app grows, but the phones catalogue as described can be implemented with core Flutter and Provider alone.

## Navigation
- Single-stack Navigator with two named routes:
  - / (PhonesListScreen)
  - /detail (PhoneDetailScreen)
- Data passed through Navigator arguments or via provider-selected item.

## Theming
- Light theme using the provided style guide:
  - Primary: #3b82f6
  - Secondary: #64748b
  - Success: #06b6d4
  - Error: #EF4444
  - Background: #f9fafb
  - Surface: #ffffff
  - Text: #111827
- Material 3 with ColorScheme adjusted to match the palette.

## Build and Run
- flutter pub get
- flutter run
- In integrated environments, a preview may be available on port 3000 automatically.

## Non-Goals
- No server communication, no authentication, no complex offline caches.
- No platform-specific integrations beyond standard Flutter build.

## Future-proofing
- Keep business logic separate from UI (even if minimal).
- Use const constructors where possible.
- Avoid using BuildContext across async gaps as per Flutter Async Context critical rules.
