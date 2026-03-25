---
"@_linked/react": patch
---

Fix `preloadFor` rendering wrong entity and add Fuseki integration tests.

### preloadFor fix

`getSourceFromInputProps` now unwraps single-element arrays returned by the result mapper for `maxCount:1` properties. Previously, passing a `preloadFor` result like `[{id: 'p3'}]` to a child component would cause the query to run without a subject, rendering incorrect data.

### Integration tests

Added 7 Fuseki-backed integration tests covering `linkedComponent` and `linkedSetComponent`:
- Single property queries
- `.where()` filtered queries
- Custom props with `.where()`
- Parent/child `preloadFor` data loading
- Set components with and without source
- Default page limit behavior

Tests use a custom Jest environment (`jest-environment-jsdom-with-fetch`) that restores Node's native `fetch` in jsdom, and auto-start Fuseki via Docker when needed.
