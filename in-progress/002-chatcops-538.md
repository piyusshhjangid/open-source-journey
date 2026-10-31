# In-Progress PR — codercops/chatcops #538: fix(widget): validate script enum attributes

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [#532 — linked issue](https://github.com/codercops/chatcops/issues/532)
- **Pull request:** [#538 — fix(widget): validate script enum attributes](https://github.com/codercops/chatcops/pull/538)
- **Target branch:** `dev`
- **Status:** Open
- **Last checked:** 1 November 2026
- **Review state:** No review submitted

## 1. Problem and requirements

- Validate `data-mode`, `data-theme-mode`, and `data-position` against their documented values.
- Ignore invalid enum values so the widget’s existing defaults apply.
- Add tests for valid values, invalid values, and fallback behavior.
- Document accepted values and defaults, and add a patch changeset for `@chatcops/widget`.

## 2. Implementation

The PR description and current GitHub diff contain the detailed implementation. This record summarizes the authored PR and live review state without treating unmerged work as a completed contribution.

## 3. Validation

- `pnpm --filter @chatcops/widget test -- tests/script-config.test.ts`
- `pnpm --filter @chatcops/widget typecheck`
- `pnpm exec biome check packages/widget/src/script-config.ts packages/widget/tests/script-config.test.ts`
- `git diff --check`

## 4. Maintainer review

No review submitted yet. The PR checks/implementation are described in its current body; issue #532 discussion confirms the unsafe enum casts and that the issue was assigned to you.

## 5. What remains

Wait for review, respond to requested changes, and keep #532 linked.

## 6. Current result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#532](https://github.com/codercops/chatcops/issues/532) |
| Pull request | [#538](https://github.com/codercops/chatcops/pull/538), open |
| Review state | Awaiting review |
| Next action | Wait for review, respond to requested changes, and keep #532 linked. |

This PR is not included in the merged contribution total.
