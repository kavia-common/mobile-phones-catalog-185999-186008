# Future Improvements

## UI/UX
- Implement real phone cards with images and responsive layout
- Add search and brand/model filters
- Add sorting options (e.g., by price)

## Data
- Load phone data from a local JSON asset for easier updates
- Optional: enable user favorites using SharedPreferences
- Optional: local persistence or caching strategy (sqflite) if the app grows

## Architecture
- Introduce a Repository pattern if adding multiple data sources
- Expand Provider usage or consider Riverpod for scale

## Internationalization
- Add i18n strings and support for multiple locales
- Use intl more extensively for currency and locale-aware formatting

## Testing and CI
- Add more widget and golden tests for list and detail screens
- Configure CI to run flutter analyze and flutter test

## Theming
- Add dark mode variant in addition to the light theme
- Provide consistent image placeholders and error states

## Performance
- Use const constructors and memoized widgets where appropriate
- Lazy-load images and consider caching strategies for assets
