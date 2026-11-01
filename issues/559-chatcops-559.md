# codercops/chatcops Issue #559 — Server: block trailing-dot local webhook hostnames

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#559 — Server: block trailing-dot local webhook hostnames](https://github.com/codercops/chatcops/issues/559)
- **Status:** Closed (checked 1 November 2026)
- **Linked pull request:** [#562](https://github.com/codercops/chatcops/pull/562) (merged)

## Problem and expected behavior

Webhook URL safety checks did not normalize a trailing DNS root dot, so localhost. could bypass local-host checks. The issue requested equivalent blocking for trailing-dot local and private hostnames while preserving public URLs.

## Discussion and result

The issue closed with merged PR #562.

## Contribution notes

This record summarizes the issue and its linked contribution. The issue and PR pages remain the source of truth for discussion, full implementation details, and validation.
