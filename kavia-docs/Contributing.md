# Contribution Guidelines

## Development Workflow
1. Install Flutter SDK and Android SDK
2. From frontend_app/, run:
   - flutter pub get
   - flutter analyze
   - flutter test
   - flutter run

## Code Style
- Follow Effective Dart conventions
- Use const constructors where possible
- Respect analyzer rules from analysis_options.yaml
- Use full package imports (e.g., package:shared_preferences/shared_preferences.dart)

## Async and Context Safety
- Do not use BuildContext or any widget/controller after an await
- Update only primitive state variables from async functions
- Drive UI updates from build() based on state flags

## Testing
- Prefer widget tests for UI
- Keep tests deterministic

## Commits and PRs
- Small, focused commits with descriptive messages
- Reference the component or screen being changed
- Include screenshots/GIFs for UI changes when possible

## Environment
- No external services required
- .env is included but remains empty for this app

## Running Preview
- Local: flutter run
- In integrated environments a preview may be available at port 3000 automatically
