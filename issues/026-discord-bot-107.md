# codercops/discord-bot Issue #107 — Concurrent /checkin requests can create duplicate log posts and lose progress

## GitHub record

- **Repository:** [codercops/discord-bot](https://github.com/codercops/discord-bot)
- **Issue:** [#107 — Concurrent /checkin requests can create duplicate log posts and lose progress](https://github.com/codercops/discord-bot/issues/107)
- **Status:** closed (checked 1 November 2026)
- **Created:** 2026-10-29
- **Last updated:** 2026-10-31
- **Closed:** 2026-10-31
- **Labels:** `bug`, `hacktoberfest`
- **Linked pull request:** [#115 — fix: prevent duplicate concurrent check-ins](https://github.com/codercops/discord-bot/pull/115) (merged)

## Problem

The issue description does not use a separate problem heading; see the scope below.

## Expected behavior and scope

At most one concurrent request should record and post a check-in for a user and roadmap on a given day. The other should report that today's check-in is already recorded, without creating another post or thread.

## Tests or acceptance criteria

No explicit test checklist in the issue body.

## Discussion and current state

The maintainer confirmed the race condition and explained a claim-before-post approach with rollback on failure. It was completed by merged PR #115.

This record reflects the issue's current state and discussion. It does not claim completed implementation unless an authored merged PR is linked above.

## Contribution notes

- **Work area:** Concurrent /checkin requests can create duplicate log posts and lose progress
- **Record update:** Recheck this file when assignment changes, a related PR opens, maintainer direction changes, or the issue closes.
- **Source:** Current GitHub issue description and comments checked on 1 November 2026.
