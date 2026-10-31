# OSS Contribution #48 — discord-bot PR #115: fix: prevent duplicate concurrent check-ins

## Repository

- **Repository:** [codercops/discord-bot](https://github.com/codercops/discord-bot)
- **Issue:** [Closes #107](https://github.com/codercops/discord-bot/issues/107) (closed).
- **Pull request:** [#115 — fix: prevent duplicate concurrent check-ins](https://github.com/codercops/discord-bot/pull/115)
- **Target branch:** `develop`
- **Merge commit:** `2f94380aeb61f06559ed2f438a4b413de6d21744`
- **Status:** Merged
- **Date merged:** 2026-10-31 (UTC)

## 1. Problem and requirements

Prevents concurrent `/checkin` requests for the same user and roadmap from recording the same day twice or creating duplicate Discord posts or log threads.

The check-in record is claimed before the Discord request. If Discord rejects the post, the previous record is restored so the learner can retry.

## 2. Implementation

The contribution merged to `develop`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- `npm run typecheck`
- `npm test` — 388 tests passed across 15 files
- `git diff --check`
- Confirmed the concurrency regression test fails without the fix.

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Concurrent requests need a safe state claim and a recovery path if the external side effect fails.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/discord-bot` |
| Issue | [#107](https://github.com/codercops/discord-bot/issues/107) (closed) |
| Pull request | [#115](https://github.com/codercops/discord-bot/pull/115), merged |
| Merge target | `develop` |
| Merge date | 2026-10-31 |
| Validation | PR-reported results summarized above |

**Contribution #48 complete.**
