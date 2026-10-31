# OSS Contribution #51 — chatcops PR #531: fix(server): honor HTTP-date Retry-After values

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Closes #525](https://github.com/codercops/chatcops/issues/525) (closed).
- **Pull request:** [#531 — fix(server): honor HTTP-date Retry-After values](https://github.com/codercops/chatcops/pull/531)
- **Target branch:** `dev`
- **Merge commit:** `5610d2d2c3707b17a710c0a6ac5753f17c851606`
- **Status:** Merged
- **Date merged:** 2026-10-31 (UTC)

## 1. Problem and requirements

- Parse numeric delay-seconds and HTTP-date values from webhook `Retry-After` headers.
- Calculate date-based delays from the current time, retry immediately for past dates, and cap delays at 10 seconds.
- Keep exponential backoff when the header is missing or invalid.
- Add tests, update the webhook documentation, and include a patch changeset for `@chatcops/server`.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- Added focused tests for numeric, HTTP-date, past-date, invalid, missing, and capped retry delays.
- Local tests were not run; CI checks should verify this branch.

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Retry behavior must preserve existing defaults while handling timing, limits, and failure cases deterministically.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#525](https://github.com/codercops/chatcops/issues/525) (closed) |
| Pull request | [#531](https://github.com/codercops/chatcops/pull/531), merged |
| Merge target | `dev` |
| Merge date | 2026-10-31 |
| Validation | PR-reported results summarized above |

**Contribution #51 complete.**
