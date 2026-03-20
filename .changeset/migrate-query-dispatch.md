---
"@_linked/react": patch
---

Replace removed `Shape.queryParser` with `getQueryDispatch()` from `@_linked/core/queries/queryDispatch`, compatible with `@_linked/core` v1.3.0+. Query factories now call `.build()` before dispatch to produce the expected `IRSelectQuery` input.
