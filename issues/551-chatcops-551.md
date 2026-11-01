# codercops/chatcops Issue #551 — Core: release retryable response bodies before retrying

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#551 — Core: release retryable response bodies before retrying](https://github.com/codercops/chatcops/issues/551)
- **Status:** Closed (checked 1 November 2026)
- **Linked pull request:** [#553](https://github.com/codercops/chatcops/pull/553) (merged)

## Problem and expected behavior

Retryable 429 and 5xx responses could leave intermediate response bodies unreleased while waiting to retry. The issue requested cancellation of intermediate bodies while preserving successful and final error responses.

## Discussion and result

The issue closed with merged PR #553.

## Contribution notes

This record summarizes the issue and its linked contribution. The issue and PR pages remain the source of truth for discussion, full implementation details, and validation.
