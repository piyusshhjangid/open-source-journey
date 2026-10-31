# codercops/chatcops Issue #529 — Widget: validate autoOpen delay values

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#529 — Widget: validate autoOpen delay values](https://github.com/codercops/chatcops/issues/529)
- **Status:** closed (checked 1 November 2026)
- **Created:** 2026-10-31
- **Last updated:** 2026-10-31
- **Closed:** 2026-10-31
- **Labels:** `hacktoberfest`
- **Linked pull request:** [#533 — fix(widget): validate auto-open delay range](https://github.com/codercops/chatcops/pull/533) (merged)

## Problem

`parseAutoOpen()` converts any digit-only `data-auto-open` value to a number. Very large values can exceed JavaScript's supported timer range, causing the widget to open much sooner than the configured delay.

## Expected behavior and scope

Accept `true`, `false`, and valid non-negative integer delays. Ignore or clearly reject values that are not finite or exceed the supported timer range. Keep valid delays in milliseconds.

## Tests or acceptance criteria

- `true`, `false`, and normal delays keep their current behavior.
- Extremely large and non-finite delays are ignored or rejected predictably.

## Discussion and current state

I requested assignment; the issue was completed by merged PR #533.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Widget
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
