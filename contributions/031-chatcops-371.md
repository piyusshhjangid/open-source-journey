# OSS Contribution #31 — chatcops PR #371: feat(widget): add French locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open when checked).
- **Pull request:** [#371 — feat(widget): add French locale](https://github.com/codercops/chatcops/pull/371)
- **Target branch:** `dev`
- **Merge commit:** `963298883f437a404b01f61b30c067ddac70c8c3`
- **Status:** Merged
- **Date merged:** 2026-10-27 (UTC)

## 1. Problem and requirements

Part of #55

Adds a complete French (fr) widget locale with French accents and punctuation, preserving all placeholders. Adds French to the widget's Available Locales table and includes a patch changeset for @chatcops/widget.

## 2. Implementation

The contribution was merged into `dev`. The scope and implementation details recorded in the PR description are summarized above. The complete diff and file list remain available on GitHub.

## 3. Validation

- vite build
- vite build -c vite.panel.config.ts — builds dist/locales/fr.js
- vite build -c vite.loader.config.ts
- tsc --emitDeclarationOnly
- vitest run — 379 tests passed
- tsc --noEmit
- node scripts/check-doc-samples.mjs — 111 checked, 1 skipped
- git diff --check

## 4. Maintainer review

GitHub reports this pull request as merged. This record does not infer approval details beyond that status; use the linked PR for the review discussion and checks.

## 5. What I learned

- Localization changes need placeholder preservation, locale-specific build coverage, and review of wording by fluent speakers.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Pull request | [#371](https://github.com/codercops/chatcops/pull/371), merged |
| Linked issue | #55 (open) |
| Merge target | `dev` |
| Merge date | 2026-10-27 |
| Validation | See the PR-reported results above |

**Contribution #31 complete.**
