# OSS Contribution #52 — chatcops PR #533: fix(widget): validate auto-open delay range

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Closes #529](https://github.com/codercops/chatcops/issues/529) (closed).
- **Pull request:** [#533 — fix(widget): validate auto-open delay range](https://github.com/codercops/chatcops/pull/533)
- **Target branch:** `dev`
- **Merge commit:** `1694df28127c0ee8bdbec2508ac32dbf54ad3d41`
- **Status:** Merged
- **Date merged:** 2026-10-31 (UTC)

## 1. Problem and requirements

- Accept `true`, `false`, and non-negative integer auto-open delays in milliseconds.
- Ignore delays above JavaScript’s maximum supported timer value (`2147483647`) and other invalid values.
- Document the accepted range and add a patch changeset for `@chatcops/widget`.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- Widget script config tests — 19 passed.
- Widget TypeScript check — passed.
- Biome check for changed files — passed.
- `git diff --check` — passed.

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- The issue-specific regression test is most useful when it reproduces the failure before the fix and verifies the repaired boundary.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#529](https://github.com/codercops/chatcops/issues/529) (closed) |
| Pull request | [#533](https://github.com/codercops/chatcops/pull/533), merged |
| Merge target | `dev` |
| Merge date | 2026-10-31 |
| Validation | PR-reported results summarized above |

**Contribution #52 complete.**
