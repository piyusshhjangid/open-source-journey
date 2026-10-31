# codercops/chatcops Issue #477 — Widget: copy a completed assistant reply

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#477 — Widget: copy a completed assistant reply](https://github.com/codercops/chatcops/issues/477)
- **Status:** closed (checked 1 November 2026)
- **Created:** 2026-10-30
- **Last updated:** 2026-10-31
- **Closed:** 2026-10-31
- **Labels:** `hacktoberfest`
- **Linked pull request:** [#504 — feat(widget): add copy action to completed replies](https://github.com/codercops/chatcops/pull/504) (merged)

## Problem

Visitors often need to reuse an answer outside the chat. Selecting a long rendered reply is awkward on phones and can be error-prone around formatted text and code blocks.

## Expected behavior and scope

Add a copy action to completed assistant replies. Copy the reply as readable plain text, preserving code block contents and line breaks without copying Markdown syntax. Keep the action out of the streaming state, make it keyboard accessible, and announce success or failure without disrupting the existing reply announcement.

## Tests or acceptance criteria

- A copy button is available for a completed assistant reply and is not shown while that reply is streaming.
- Clipboard failures are handled without an uncaught error, including when the Clipboard API is unavailable.
- The control has a localized accessible name, a visible focus indicator, and an accessible confirmation of the result.
- Tests cover copying formatted content, streaming replies, and clipboard failure.
- Add a widget changeset; keep the gzipped bundle within the configured size budget.

## Discussion and current state

The maintainer assigned this issue to me and suggested reusing the existing reply action and live-region patterns. It was completed by merged PR #504.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Widget
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
