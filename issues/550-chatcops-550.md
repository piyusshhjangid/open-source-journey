# codercops/chatcops Issue #550 — Core: honor HTTP-date Retry-After values in provider retries

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#550 — Core: honor HTTP-date Retry-After values in provider retries](https://github.com/codercops/chatcops/issues/550)
- **Status:** Closed (checked 1 November 2026)
- **Linked pull request:** [#552](https://github.com/codercops/chatcops/pull/552) (merged)

## Problem and expected behavior

The shared provider retry helper handled numeric Retry-After values but fell back to exponential backoff for valid HTTP-date values. The issue requested date parsing, a 30-second cap, zero delay for past dates, and preserved abortable waits.

## Discussion and result

The issue closed with merged PR #552.

## Contribution notes

This record summarizes the issue and its linked contribution. The issue and PR pages remain the source of truth for discussion, full implementation details, and validation.
