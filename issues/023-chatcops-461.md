# codercops/chatcops Issue #461 — Widget: fetch signed-in visitor tokens when a session is requested

## GitHub record

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#461 — Widget: fetch signed-in visitor tokens when a session is requested](https://github.com/codercops/chatcops/issues/461)
- **Status:** closed (checked 1 November 2026)
- **Created:** 2026-10-29
- **Last updated:** 2026-10-30
- **Closed:** 2026-10-30
- **Labels:** `enhancement`, `hacktoberfest`
- **Linked pull request:** None currently linked in the issue body or comments.

## Problem

The widget accepts `userToken` as a fixed string and sends it when requesting a session. A page can stay open for a long time before the visitor opens the chat, so a short-lived signed token may expire before the first `/session` request. The server correctly rejects expired identity tokens, but the host page currently has no way to provide a fresh one at that point.

## Expected behavior and scope

Add an optional async token provider (or equivalent callback) that the widget calls when it is about to request `/session`, so the host can return a current signed token. Keep the existing string `userToken` behavior backwards compatible, send the resolved token only to the configured ChatCops API, and document that signing secrets must remain on the host server. Add tests for fresh tokens, provider failures, and the existing static-token option.

## Tests or acceptance criteria

No explicit test checklist in the issue body.

## Discussion and current state

The maintainer discussed an async token-provider design, but assigned the issue to another contributor due to the project's active-issue limit. It was later closed.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Widget
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
