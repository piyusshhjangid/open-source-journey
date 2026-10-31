# codercops/chatcops Issue #536 — Widget: ignore invalid data-wait-for-consent values

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#536 — Widget: ignore invalid data-wait-for-consent values](https://github.com/codercops/chatcops/issues/536)
- **Status:** open (checked 1 November 2026)
- **Created:** 2026-10-31
- **Last updated:** 2026-10-31
- **Closed:** Still open
- **Labels:** `hacktoberfest`
- **Linked pull request:** [#539 — fix(widget): ignore invalid consent attributes](https://github.com/codercops/chatcops/pull/539) (open)

## Problem

The script-tag parser treats every `data-wait-for-consent` value except `"false"` as enabled. A typo such as `"flase"` therefore unexpectedly makes the widget wait for consent.

## Expected behavior and scope

- `"true"` enables consent waiting.
- `"false"` disables it.
- A present attribute with an empty value remains a shorthand for enabled.
- Any other non-empty value is ignored, preserving the default behavior.

## Tests or acceptance criteria

Cover `"true"`, `"false"`, an empty attribute, an invalid value, and an omitted attribute.

Update the widget configuration docs to explain the accepted values.

## Discussion and current state

The maintainer clarified consent must fail closed: any value other than false continues waiting for consent, while invalid values should produce a console warning. That feedback is reflected in open PR #539, which has changes requested.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Widget
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
