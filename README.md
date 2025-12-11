# Mobile Phones Catalogue (Flutter)

## Overview
This repository contains a single-container Flutter mobile application that displays a list of mobile phones with basic details such as model, brand, price, and a photo. Tapping on a phone opens a detail view. The app has no backend and does not require authentication or any external services.

- Container: frontend_app
- Framework: Flutter
- Platform: Mobile
- Preview: The system starts a preview automatically on port 3000 (when available in your environment). For local development, use standard Flutter commands below.

## Project Structure
- frontend_app/: Flutter application source
  - lib/main.dart: Entry point and current app shell
  - pubspec.yaml: Dependencies and asset declarations
  - test/: Widget test scaffold
  - android/: Android-specific project files
  - assets/: Placeholder for images (empty)

## Quick Start

### Prerequisites
- Flutter SDK 3.29.0+ (Dart >= 3.7.0 per pubspec)
- Android SDK for running on Android emulator or device
- No environment variables required (.env is present but empty)

### Install dependencies
- Navigate to the Flutter app folder:
  - cd mobile-phones-catalog-185999-186008/frontend_app
- Get packages:
  - flutter pub get

### Run on device/emulator
- flutter run

### Run tests
- flutter test

## Development Notes
- This is a single container Flutter project with no backend.
- The preview system (in integrated environments) may automatically expose the app on port 3000 for quick viewing, but standard Flutter tooling remains the source of truth locally.
- The app uses Material 3 and a light theme foundation. See the UI/Style Guide Summary for theme details.

## Documentation
- See detailed docs in kavia-docs/:
  - kavia-docs/Architecture.md
  - kavia-docs/Features.md
  - kavia-docs/UI-Style-Guide.md
  - kavia-docs/Data-Model-and-Navigation.md
  - kavia-docs/Contributing.md
  - kavia-docs/Future-Improvements.md

## License
Proprietary or project-specific license. Update as appropriate.
