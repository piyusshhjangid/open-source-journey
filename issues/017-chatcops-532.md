# codercops/chatcops Issue #532 — Widget: validate enum values from script-tag attributes

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#532 — Widget: validate enum values from script-tag attributes](https://github.com/codercops/chatcops/issues/532)
- **Status:** open (checked 1 November 2026)
- **Created:** 2026-10-31
- **Last updated:** 2026-10-31
- **Closed:** Still open
- **Labels:** `hacktoberfest`
- **Linked pull request:** [#538 — fix(widget): validate script enum attributes](https://github.com/codercops/chatcops/pull/538) (open)

## Problem

Some script-tag attributes, including `data-mode`, are cast to union types without checking their runtime values. Invalid values can silently produce confusing widget behavior.

## Expected behavior and scope

Only accept documented values for enum-like script attributes. Ignore invalid values and use the documented default.

## Tests or acceptance criteria

Cover valid and invalid values for `data-mode`, `data-theme-mode`, and `data-position`, including the fallback behavior.

## Discussion and current state

The maintainer confirmed the affected script attributes and assigned the issue to me after earlier work merged. It is addressed by open PR #538.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Widget
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
