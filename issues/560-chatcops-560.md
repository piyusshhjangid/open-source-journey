# codercops/chatcops Issue #560 — Make the lint script expand package globs on Windows

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#560 — Make the lint script expand package globs on Windows](https://github.com/codercops/chatcops/issues/560)
- **Status:** Closed (checked 1 November 2026)
- **Linked pull request:** [#565](https://github.com/codercops/chatcops/pull/565) (merged)

## Problem and expected behavior

Windows PowerShell passed package globs literally to Biome, causing an I/O error and preventing workspace linting. The issue requested cross-platform path expansion that also includes future packages.

## Discussion and result

The issue closed with merged PR #565.

## Contribution notes

This record summarizes the issue and its linked contribution. The issue and PR pages remain the source of truth for discussion, full implementation details, and validation.
