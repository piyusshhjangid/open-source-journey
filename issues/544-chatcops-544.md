# codercops/chatcops Issue #544 — Widget: report invalid inline container selectors clearly

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#544 — Widget: report invalid inline container selectors clearly](https://github.com/codercops/chatcops/issues/544)
- **Status:** Closed (checked 1 November 2026)
- **Linked pull request:** [#549](https://github.com/codercops/chatcops/pull/549) (merged)

## Problem and expected behavior

Malformed CSS selectors passed to document.querySelector() produced a browser DOMException, unlike valid selectors with no match. The issue requested a clear ChatCops error while preserving the no-match behavior.

## Discussion and result

The issue closed with merged PR #549.

## Contribution notes

This record summarizes the issue and its linked contribution. The issue and PR pages remain the source of truth for discussion, full implementation details, and validation.
