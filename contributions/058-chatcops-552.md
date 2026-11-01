# OSS Contribution #58 — ChatCops PR #552: fix(core): honor HTTP-date Retry-After values

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#550](https://github.com/codercops/chatcops/issues/550) (closed)
- **Pull request:** [#552 — fix(core): honor HTTP-date Retry-After values](https://github.com/codercops/chatcops/pull/552)
- **Status:** Merged
- **Date merged:** 2026-10-31

## Problem and implementation

Parse delay-seconds and HTTP-date Retry-After values in the shared provider retry helper. Clamp past dates to zero, cap waits at 30 seconds, preserve exponential backoff for missing or invalid values, and keep waits abortable.

## Validation

Core retry helper tests (7), typecheck, build, Biome, and diff check were reported passing.

## What I learned

This contribution strengthened my practice in defining edge-case behavior, adding focused regression coverage, and documenting changes in the package’s established workflow.

## Result

The change was merged into ChatCops. See the linked PR for the full diff, review discussion, and checks.
