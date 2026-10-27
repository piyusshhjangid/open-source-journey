# OSS Contribution #27 — chatcops PR #351: feat(widget): add Hindi locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open when checked).
- **Pull request:** [#351 — feat(widget): add Hindi locale](https://github.com/codercops/chatcops/pull/351)
- **Target branch:** `dev`
- **Merge commit:** `fa8df0d6476d6d8efc38466e2b4e3f7bbe8be64a`
- **Status:** Merged
- **Date merged:** 2026-10-26 (UTC)

## 1. Problem and requirements

Part of #55

Adds the complete Hindi (`hi`) widget locale in Devanagari. Hindi is loaded as a separate locale file when selected. Adds checks for non-empty translations, placeholder preservation, and English fallback for unknown locale codes. Updates the widget locale documentation and adds an `@chatcops/widget` patch changeset.

## 2. Implementation

The contribution was merged into `dev`. The scope and implementation details recorded in the PR description are summarized above. The complete diff and file list remain available on GitHub.

## 3. Validation

- `pnpm --filter @chatcops/widget build` — passed
- `pnpm --filter @chatcops/widget test` — passed (345 tests)
- `pnpm --filter @chatcops/widget typecheck` — passed
- `node scripts/check-doc-samples.mjs` — passed (108 checked, 1 skipped)
- `git diff --check` — passed

## 4. Maintainer review

GitHub reports this pull request as merged. This record does not infer approval details beyond that status; use the linked PR for the review discussion and checks.

## 5. What I learned

- Localization changes need placeholder preservation, locale-specific build coverage, and review of wording by fluent speakers.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Pull request | [#351](https://github.com/codercops/chatcops/pull/351), merged |
| Linked issue | #55 (open) |
| Merge target | `dev` |
| Merge date | 2026-10-26 |
| Validation | See the PR-reported results above |

**Contribution #27 complete.**
