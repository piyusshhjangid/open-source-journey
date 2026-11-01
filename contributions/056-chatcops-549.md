# OSS Contribution #56 — ChatCops PR #549: fix(widget): report invalid container selectors

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#544](https://github.com/codercops/chatcops/issues/544) (closed)
- **Pull request:** [#549 — fix(widget): report invalid container selectors](https://github.com/codercops/chatcops/pull/549)
- **Status:** Merged
- **Date merged:** 2026-10-31

## Problem and implementation

Return a clear error for malformed inline container selectors while preserving the existing no-match error for valid selectors. Add tests, documentation, and a patch changeset.

## Validation

Widget tests (67), typecheck, documentation sample check (201 TypeScript blocks, 4 skipped), size-limit, and changed-file checks were reported.

## What I learned

This contribution strengthened my practice in defining edge-case behavior, adding focused regression coverage, and documenting changes in the package’s established workflow.

## Result

The change was merged into ChatCops. See the linked PR for the full diff, review discussion, and checks.
