# OSS Contribution #40 — chatcops PR #390: feat(widget): add Italian locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open).
- **Pull request:** [#390 — feat(widget): add Italian locale](https://github.com/codercops/chatcops/pull/390)
- **Target branch:** `dev`
- **Merge commit:** `26a4086ba56fded32e692544311fce9c81c6fb46`
- **Status:** Merged
- **Date merged:** 2026-10-28 (UTC)

## 1. Problem and requirements

Part of #55

- Add the Italian (`it`) widget locale with placeholders preserved.
- Add Italian to the widget's Available Locales documentation.
- Add a patch changeset for `@chatcops/widget`.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- `vite build`
- `vite build -c vite.panel.config.ts` — emits `dist/locales/it.js`
- `vite build -c vite.loader.config.ts`
- `tsc --emitDeclarationOnly`
- `tsc --noEmit`
- `vitest run --project @chatcops/widget` — 391 tests passed
- `git diff --check`

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Preserving interpolation placeholders and checking the emitted locale bundle are key parts of a localization change.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#55](https://github.com/codercops/chatcops/issues/55) (open) |
| Pull request | [#390](https://github.com/codercops/chatcops/pull/390), merged |
| Merge target | `dev` |
| Merge date | 2026-10-28 |
| Validation | PR-reported results summarized above |

**Contribution #40 complete.**
