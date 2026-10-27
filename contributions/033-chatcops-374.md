# OSS Contribution #33 — chatcops PR #374: feat(widget): add German locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open when checked).
- **Pull request:** [#374 — feat(widget): add German locale](https://github.com/codercops/chatcops/pull/374)
- **Target branch:** `dev`
- **Merge commit:** `458fb3c222d3a4ac4aa1af2188e84efa7ca31266`
- **Status:** Merged
- **Date merged:** 2026-10-27 (UTC)

## 1. Problem and requirements

Part of #55

- Add the German (`de`) widget locale with preserved placeholders.
- List German in the widget's Available Locales documentation.
- Add a patch changeset for `@chatcops/widget`.

## 2. Implementation

The contribution was merged into `dev`. The scope and implementation details recorded in the PR description are summarized above. The complete diff and file list remain available on GitHub.

## 3. Validation

- `vite build`
- `vite build -c vite.panel.config.ts` — emits `dist/locales/de.js`
- `vite build -c vite.loader.config.ts`
- `tsc --emitDeclarationOnly`
- `vitest run --project @chatcops/widget` — 387 tests passed
- Widget typecheck
- `node scripts/check-doc-samples.mjs` — 111 checked, 1 skipped
- `git diff --check`

## 4. Maintainer review

GitHub reports this pull request as merged. This record does not infer approval details beyond that status; use the linked PR for the review discussion and checks.

## 5. What I learned

- Localization changes need placeholder preservation, locale-specific build coverage, and review of wording by fluent speakers.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Pull request | [#374](https://github.com/codercops/chatcops/pull/374), merged |
| Linked issue | #55 (open) |
| Merge target | `dev` |
| Merge date | 2026-10-27 |
| Validation | See the PR-reported results above |

**Contribution #33 complete.**
