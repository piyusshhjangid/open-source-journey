# OSS Contribution #50 — chatcops PR #524: feat(server): configure webhook delivery retries

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Closes #519](https://github.com/codercops/chatcops/issues/519) (closed).
- **Pull request:** [#524 — feat(server): configure webhook delivery retries](https://github.com/codercops/chatcops/pull/524)
- **Target branch:** `dev`
- **Merge commit:** `b8a3f9e72d8689d3822e77442b38f606b2e09e3b`
- **Status:** Merged
- **Date merged:** 2026-10-31 (UTC)

## 1. Problem and requirements

- Add per-webhook `timeoutMs` and `maxAttempts` options.
- Preserve the existing defaults: 5,000 ms per attempt and 3 total attempts.
- Apply the timeout separately to each attempt and stop at each webhook’s configured attempt limit.
- Keep the existing retry rules, `Retry-After` handling, and backoff delays.
- Validate the options and document their units, valid ranges, and defaults.
- Add delivery tests, update the core API snapshot, and include a minor changeset for `@chatcops/core` and `@chatcops/server`.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- Core and server builds — passed.
- Core and server typechecks — passed.
- Focused webhook tests — 45 passed.
- `git diff --check` — passed.
- Biome check — completed with one existing warning about a non-null assertion in the webhook test helper.

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Retry behavior must preserve existing defaults while handling timing, limits, and failure cases deterministically.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#519](https://github.com/codercops/chatcops/issues/519) (closed) |
| Pull request | [#524](https://github.com/codercops/chatcops/pull/524), merged |
| Merge target | `dev` |
| Merge date | 2026-10-31 |
| Validation | PR-reported results summarized above |

**Contribution #50 complete.**
