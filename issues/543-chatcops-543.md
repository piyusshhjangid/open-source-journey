# codercops/chatcops Issue #543 — Widget: validate maxMessages before saving conversation history

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#543 — Widget: validate maxMessages before saving conversation history](https://github.com/codercops/chatcops/issues/543)
- **Status:** Closed (checked 1 November 2026)
- **Linked pull request:** [#548](https://github.com/codercops/chatcops/pull/548) (merged)

## Problem and expected behavior

A zero maxMessages value caused slice(0) to save all messages; invalid values could also exceed the intended persisted history limit. The issue defined safe-integer validation, zero behavior, a default of 50, tests, and documentation.

## Discussion and result

The issue closed with merged PR #548.

## Contribution notes

This record summarizes the issue and its linked contribution. The issue and PR pages remain the source of truth for discussion, full implementation details, and validation.
