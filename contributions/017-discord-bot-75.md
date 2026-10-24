# OSS Contribution #17 — Discord Bot Merge-Time Counting

## Repository

- **Repository:** [codercops/discord-bot](https://github.com/codercops/discord-bot)
- **Issue:** [#70 — Merged PR shoutout counts PRs merged after it when the webhook arrives late](https://github.com/codercops/discord-bot/issues/70) (closed as completed)
- **Pull Request:** [#75 — fix: count merged PRs by merge time](https://github.com/codercops/discord-bot/pull/75)
- **Branch:** `fix/70-late-merged-pr-webhook`
- **Commit:** `962040d`
- **Merge commit:** `ca17927`
- **Status:** Merged into `develop`; issue #70 closed as completed
- **Label:** Not recorded in the PR summary.
- **Date:** 22 October 2026

## 1. Problem and requirements

A delayed merged-pull-request webhook could include later merges in the shoutout count and send a qualification message for the wrong merge.

## 2. Implementation

Filtered the author's PRs using parsed `mergedAt` timestamps no later than the current PR's merge time. Kept caching all merged PRs for the leaderboard and added regression tests for both timing scenarios and exactly-once qualification messaging.

## 3. Validation

`npm run typecheck`, `npm test` (317 passed), and `git diff --check` passed. Confirmed the regression tests fail without the fix. Anurag629 confirmed the typecheck and all 317 tests pass on `develop`.

## 4. Maintainer review

Anurag629 approved and confirmed both new tests fail against the old webhook implementation while the leaderboard still caches every merge.

## 5. What I learned

- Event-driven counts should use event time rather than webhook delivery time. Regression tests should cover late delivery and the exact boundary ordering.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/discord-bot` |
| Issue | [#70](https://github.com/codercops/discord-bot/issues/70), closed |
| Pull request | [#75](https://github.com/codercops/discord-bot/pull/75), merged |
| Contribution | Discord Bot Merge-Time Counting |
| Merge target | `discord-bot`:`develop` |
| Merge date | 22 October 2026 |
| Validation | PR and maintainer-reported results summarized above |

**Contribution #17 complete.**
