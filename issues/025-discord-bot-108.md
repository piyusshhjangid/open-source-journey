# codercops/discord-bot Issue #108 — Merged PR role count can double-count when the current PR is outside the first search page

## GitHub record

- **Repository:** [codercops/discord-bot](https://github.com/codercops/discord-bot)
- **Issue:** [#108 — Merged PR role count can double-count when the current PR is outside the first search page](https://github.com/codercops/discord-bot/issues/108)
- **Status:** open (checked 1 November 2026)
- **Created:** 2026-10-29
- **Last updated:** 2026-10-29
- **Closed:** Still open
- **Labels:** None
- **Linked pull request:** None currently linked in the issue body or comments.

## Problem

The issue description does not use a separate problem heading; see the scope below.

## Expected behavior and scope

The webhook's earlier-PR count should exclude the current PR even when it is not on the first search page, so role thresholds are evaluated against an accurate count.

## Tests or acceptance criteria

No explicit test checklist in the issue body.

## Discussion and current state

The maintainer left this open as a note, explaining that the bug would not affect current role thresholds under configured tiers. No implementation PR is linked.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Merged PR role count can double-count when the current PR is outside the first search page
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
