# OSS Contribution #44 — chatcops PR #409: feat(widget): add Hebrew locale

## Repository

- **Repository:** [codercops/chatcops](https://github.com/codercops/chatcops)
- **Issue:** [Part of #55](https://github.com/codercops/chatcops/issues/55) (open).
- **Pull request:** [#409 — feat(widget): add Hebrew locale](https://github.com/codercops/chatcops/pull/409)
- **Target branch:** `dev`
- **Merge commit:** `316f625615c2cad758136c6d7eb1ba3c4af11949`
- **Status:** Merged
- **Date merged:** 2026-10-28 (UTC)

## 1. Problem and requirements

Part of #55

Adds the Hebrew (he) widget locale in Hebrew script, lists Hebrew in the Available Locales documentation, and includes a patch changeset for @chatcops/widget. Placeholders are preserved so untranslated future keys can fall back to English.

## 2. Implementation

The contribution merged to `dev`. The summary above follows the PR description; the full diff and file list are available on GitHub.

## 3. Validation

- Widget build, panel build (emits dist/locales/he.js), and loader build passed.
- Type declaration generation and tsc --noEmit passed.
- vitest run --project @chatcops/widget — 396 tests passed.
- git diff --check passed.

## 4. Maintainer review

GitHub reports the pull request as merged. Any specific review notes are available in the linked PR discussion.

## 5. What I learned

- Preserving interpolation placeholders and checking the emitted locale bundle are key parts of a localization change.

## 6. Final result

| Item | Result |
|---|---|
| Repository | `codercops/chatcops` |
| Issue | [#55](https://github.com/codercops/chatcops/issues/55) (open) |
| Pull request | [#409](https://github.com/codercops/chatcops/pull/409), merged |
| Merge target | `dev` |
| Merge date | 2026-10-28 |
| Validation | PR-reported results summarized above |

**Contribution #44 complete.**
