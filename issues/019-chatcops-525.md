# codercops/chatcops Issue #525 — Server: honor HTTP-date Retry-After values for webhooks

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#525 — Server: honor HTTP-date Retry-After values for webhooks](https://github.com/codercops/chatcops/issues/525)
- **Status:** closed (checked 1 November 2026)
- **Created:** 2026-10-31
- **Last updated:** 2026-10-31
- **Closed:** 2026-10-31
- **Labels:** `hacktoberfest`
- **Linked pull request:** [#531 — fix(server): honor HTTP-date Retry-After values](https://github.com/codercops/chatcops/pull/531) (merged)

## Problem

Webhook retries honor numeric `Retry-After` values, but ignore valid HTTP-date values and use the exponential backoff instead. Receivers using date-form values can therefore be retried earlier than requested.

## Expected behavior and scope

Parse both delay-seconds and HTTP-date values. For a date, calculate the delay from the current time and preserve the existing 10-second maximum. Missing or invalid values should continue using the existing exponential backoff.

## Tests or acceptance criteria

- Numeric and HTTP-date values produce the expected delays.
- Past dates, invalid values, and missing headers follow the documented fallback behavior.
- Delays remain capped at 10 seconds.

Document the supported formats and add an appropriate `@chatcops/server` changeset.

## Discussion and current state

The maintainer confirmed HTTP-date parsing and delay-cap requirements, held the issue for me, and said to start after #524. It was completed by merged PR #531.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Server
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
