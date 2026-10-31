# OSS Contribution #38 — chatcops PR #384: feat(widget): add Portuguese locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open).
- **Pull request:** [#384 — feat(widget): add Portuguese locale](https://github.com/codercops/chatcops/pull/384)
- **Target branch:** `dev`
- **Merge commit:** `f73ecf87800a76213b1b10dd8e56388e3b38fb10`
- **Status:** Merged
- **Date merged:** 2026-10-28 (UTC)

## 1. Problem and requirements

Adds the Portuguese (`pt`) translation to `@chatcops/widget`, loaded on-demand for visitors using Portuguese.

Part of #55

## Changes Made

- Added `packages/widget/src/locales/pt.ts` translating all `WidgetLocaleStrings` keys into Portuguese with proper accents, punctuation, and placeholder retention (`{name}`, `{label}`, `{seconds}`, `{count}`).
- Added Portuguese (`pt`) to the "Available Locales" table in `website/src/content/docs/widget/i18n.mdx`.
- Added patch changeset for `@chatcops/widget`.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- `pnpm --filter @chatcops/widget build` (built `dist/locales/pt.js`)
- `pnpm --filter @chatcops/widget test` (all 391 tests passed, including `tests/locales.test.ts`)
- `pnpm -r typecheck` (passed with 0 errors)
- `pnpm size` (all bundles well under budget)

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Preserving interpolation placeholders and checking the emitted locale bundle are key parts of a localization change.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#55](https://github.com/codercops/chatcops/issues/55) (open) |
| Pull request | [#384](https://github.com/codercops/chatcops/pull/384), merged |
| Merge target | `dev` |
| Merge date | 2026-10-28 |
| Validation | PR-reported results summarized above |

**Contribution #38 complete.**
