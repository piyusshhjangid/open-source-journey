# OSS Contribution #36 — chatcops PR #377: feat(widget): add Japanese locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open when checked).
- **Pull request:** [#377 — feat(widget): add Japanese locale](https://github.com/codercops/chatcops/pull/377)
- **Target branch:** `dev`
- **Merge commit:** `2c1f49add243a43a13e41478519477f4356d437f`
- **Status:** Merged
- **Date merged:** 2026-10-27 (UTC)

## 1. Problem and requirements

Part of #55

- Add the Japanese (`ja`) widget locale with all current strings translated and placeholders preserved.
- Add Japanese to the widget's Available Locales documentation.
- Add a patch changeset for `@chatcops/widget`.

## 2. Implementation

The contribution was merged into `dev`. The scope and implementation details recorded in the PR description are summarized above. The complete diff and file list remain available on GitHub.

## 3. Validation

- `vite build`
- `vite build -c vite.panel.config.ts` — emits `dist/locales/ja.js`
- `vite build -c vite.loader.config.ts`
- `tsc --emitDeclarationOnly`
- `tsc --noEmit`
- `vitest run --project @chatcops/widget` — 388 tests passed
- `node scripts/check-doc-samples.mjs` — 112 checked, 1 skipped
- `git diff --check`

## 4. Maintainer review

GitHub reports this pull request as merged. This record does not infer approval details beyond that status; use the linked PR for the review discussion and checks.

## 5. What I learned

- Localization changes need placeholder preservation, locale-specific build coverage, and review of wording by fluent speakers.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Pull request | [#377](https://github.com/codercops/chatcops/pull/377), merged |
| Linked issue | #55 (open) |
| Merge target | `dev` |
| Merge date | 2026-10-27 |
| Validation | See the PR-reported results above |

**Contribution #36 complete.**
