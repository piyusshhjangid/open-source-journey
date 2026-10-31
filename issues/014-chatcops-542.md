# codercops/chatcops Issue #542 — Widget: validate data-history-ttl-days values

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#542 — Widget: validate data-history-ttl-days values](https://github.com/codercops/chatcops/issues/542)
- **Status:** open (checked 1 November 2026)
- **Created:** 2026-10-31
- **Last updated:** 2026-10-31
- **Closed:** Still open
- **Labels:** None
- **Linked pull request:** None currently linked in the issue body or comments.

## Problem

The script-tag parser converts any digit-only `data-history-ttl-days` value to a number. An extremely large value can overflow when converted to milliseconds, making conversation expiry unreliable.

## Expected behavior and scope

- Accept non-negative integer values within a documented, safely supported range.
- Ignore values outside that range so the widget uses its 30-day default.
- Keep `0` valid for callers who want saved conversations to expire immediately.

## Tests or acceptance criteria

Cover a normal value, `0`, an oversized value, and a value that would overflow when converted to milliseconds.

Update the widget configuration docs with the accepted range and fallback behavior.

## Discussion and current state

I commented that I would like to work on this after either current PR #539 or #538 merges; another contributor also expressed interest. It remains open.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Widget
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
