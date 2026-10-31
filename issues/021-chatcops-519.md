# codercops/chatcops Issue #519 — Server: make webhook timeout and retry limits configurable

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#519 — Server: make webhook timeout and retry limits configurable](https://github.com/codercops/chatcops/issues/519)
- **Status:** closed (checked 1 November 2026)
- **Created:** 2026-10-31
- **Last updated:** 2026-10-31
- **Closed:** 2026-10-31
- **Labels:** `hacktoberfest`
- **Linked pull request:** [#524 — feat(server): configure webhook delivery retries](https://github.com/codercops/chatcops/pull/524) (merged)

## Problem

The issue description does not use a separate problem heading; see the scope below.

## Expected behavior and scope

See the issue body for complete scope.

## Tests or acceptance criteria

Add or update tests to cover:

- Existing defaults when the options are omitted.
- Different timeout and attempt limits for separate webhooks.
- The configured timeout applying to each delivery attempt.
- Retry stopping at the configured attempt limit.
- Existing retry rules and delays remaining unchanged.
- Invalid option values being rejected with clear errors.

## Discussion and current state

The maintainer assigned this issue to me and specified compatible option names, defaults, validation, tests, and docs. It was completed by merged PR #524.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Server
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
