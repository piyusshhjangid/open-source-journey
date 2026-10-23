# OSS Contribution #17 — Discord Bot Merge-Time Counting

## Repository

- **Repository:** [codercops/discord-bot](https://github.com/codercops/discord-bot)
- **Issue:** Not listed in the supplied contribution record; verify in the PR Development section.
- **Pull Request:** [#75 — fix: count merged PRs by merge time](https://github.com/codercops/discord-bot/pull/75)
- **Branch:** Not captured in the supplied record.
- **Commit:** Not captured in the supplied record.
- **Merge commit:** Not captured in the supplied record.
- **Status:** Merged, according to the contributor supplied activity list.
- **Label:** Not captured in the supplied record.
- **Date:** Not captured in the supplied record.

## 1. Problem and requirements

Merged pull requests need to be counted according to when they were merged. The PR title identifies merge time as the timestamp basis.

## 2. Implementation

Changed merged-PR counting to use merge time. The supplied activity record does not specify the previous timestamp field, reporting window, or affected commands.

## 3. Validation

Test commands, CI results, and manual checks were not included in the supplied activity list. See the linked PR for its checks and validation evidence.

## 4. Maintainer review

Review comments and approval details were not included in the supplied activity list. See [PR #75](https://github.com/codercops/discord-bot/pull/75) for the review record.

## 5. What I learned

- Activity reports should use the timestamp that matches the event being counted. Tests should cover boundary dates and missing merge timestamps.
- Use the PR diff and conversation as the source of truth for precise implementation and review history.

## 6. Final result

| Item | Result |
|---|---|
| Repository | codercops/discord-bot |
| Issue | Not recorded in supplied activity |
| Pull request | #75 |
| Contribution | Discord Bot Merge-Time Counting |
| Status | Merged |
| Validation and review evidence | Refer to the linked PR |

**Contribution #17 complete.**
