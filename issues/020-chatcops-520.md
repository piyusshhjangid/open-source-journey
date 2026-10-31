# codercops/chatcops Issue #520 — Server: validate webhook signature tolerance

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#520 — Server: validate webhook signature tolerance](https://github.com/codercops/chatcops/issues/520)
- **Status:** closed (checked 1 November 2026)
- **Created:** 2026-10-31
- **Last updated:** 2026-10-31
- **Closed:** 2026-10-31
- **Labels:** `hacktoberfest`
- **Linked pull request:** None currently linked in the issue body or comments.

## Problem

`verifyWebhook()` accepts an optional `toleranceSec`, but does not validate it. With `NaN` or `Infinity`, the timestamp age comparison does not reject stale signatures, effectively disabling the freshness check.

## Expected behavior and scope

Require `toleranceSec` to be a finite, non-negative safe integer in seconds. Reject invalid values with a clear error, while preserving the default of 300 seconds and allowing `0` for callers who want no clock-skew window.

## Tests or acceptance criteria

- Invalid values (`NaN`, `Infinity`, negative values, and fractions) are rejected.
- `0`, a valid custom tolerance, and the default work as documented.
- Expired and future-dated signatures remain rejected outside the configured tolerance.

Update the webhook verification docs and add an appropriate `@chatcops/server` changeset.

## Discussion and current state

I asked to take the issue, but the maintainer assigned it to another contributor because I already had active work. The issue was later closed.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Server
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
