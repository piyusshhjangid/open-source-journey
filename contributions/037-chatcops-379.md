# OSS Contribution #37 — ChatCops PR #379: feat(widget): add Arabic locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55 — Add built-in translations to the widget](https://github.com/codercops/chatcops/issues/55) (open umbrella issue when checked)
- **Pull request:** [#379 — feat(widget): add Arabic locale](https://github.com/codercops/chatcops/pull/379)
- **Target branch:** `dev`
- **Merge commit:** `b8c5ed6c35c4f41e82827bbc241124119c37c9d0`
- **Status:** Merged
- **Date merged:** 2026-10-27 (UTC)

## 1. Problem and requirements

Issue #55 tracks built-in widget translations. This PR adds Arabic to the locale set, preserving the widget's existing right-to-left behavior and the placeholders used by localized strings.

## 2. Implementation

- Added the Arabic (`ar`) widget locale and translated strings.
- Preserved translation placeholders.
- Added Arabic to the Available Locales documentation.
- Added a patch changeset for `@chatcops/widget`.
- Reused the widget's existing right-to-left direction handling for Arabic.

## 3. Validation

The PR reports:

- `vite build` — passed.
- `vite build -c vite.panel.config.ts` — emitted `dist/locales/ar.js`.
- `vite build -c vite.loader.config.ts` — passed.
- `tsc --emitDeclarationOnly` and `tsc --noEmit` — passed.
- `vitest run --project @chatcops/widget` — 389 tests passed.
- `node scripts/check-doc-samples.mjs` — 113 checked, 1 skipped.
- `git diff --check` — passed.

## 4. Maintainer review

The maintainer approved the PR, confirmed locale tests, lint, documentation checks, and the Arabic locale build passed, and noted that existing widget behavior sets `dir="rtl"` for Arabic. GitHub records the PR as merged.

## 5. What I learned

- Localization needs to preserve interpolation placeholders and should be checked through the actual locale build path.
- Existing directionality support can be reused when adding a right-to-left language, then verified at the widget boundary.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#55](https://github.com/codercops/chatcops/issues/55), open umbrella issue |
| Pull request | [#379](https://github.com/codercops/chatcops/pull/379), merged |
| Merge target | `dev` |
| Merge date | 2026-10-27 |
| Validation | PR-reported locale builds, type checks, 389 widget tests, docs check, and diff check passed |

**Contribution #37 complete.**
