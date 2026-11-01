# OSS Contribution #57 — ChatCops PR #553: fix(core): cancel retryable response bodies

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#551](https://github.com/codercops/chatcops/issues/551) (closed)
- **Pull request:** [#553 — fix(core): cancel retryable response bodies](https://github.com/codercops/chatcops/pull/553)
- **Status:** Merged
- **Date merged:** 2026-10-31

## Problem and implementation

Cancel each intermediate retryable HTTP response body before waiting to retry. Successful response bodies remain available and the final failed response body is preserved for error details.

## Validation

Focused response-body tests (3), regression checks, core typecheck, Biome, and diff check were reported passing.

## What I learned

This contribution strengthened my practice in defining edge-case behavior, adding focused regression coverage, and documenting changes in the package’s established workflow.

## Result

The change was merged into ChatCops. See the linked PR for the full diff, review discussion, and checks.
