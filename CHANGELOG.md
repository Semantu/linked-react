# Changelog

## 1.0.0

### Major Changes

- [#1](https://github.com/Semantu/linked-react/pull/1) [`4ef2ccf`](https://github.com/Semantu/linked-react/commit/4ef2ccf954629e43b6ddc995766d8e26244130ca) Thanks [@flyon](https://github.com/flyon)! - update to major

### 1.0.0 (from LINCD.js)

Initial extraction from the LINCD monolith. Moves React-specific linked component wrappers into a standalone package.

- `linkedComponent(...)` and `linkedSetComponent(...)` extracted from `lincd`.
- `LinkedComponentClass` base class for class-based linked components.
- `useStyles(...)` hook for component styling.
- Pagination API (`nextPage`, `previousPage`, `setPage`, `setLimit`) on linked set components.
- `_refresh(updatedProps?)` for optimistic UI updates on linked components.
